---
title: Руководство. Объединение данных из Excel и веб-канала OData в Power BI Desktop
description: Руководство. Объединение данных из Excel и веб-канала OData
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: tutorial
ms.date: 05/21/2018
ms.author: v-thepet
LocalizationGroup: Learn more
ms.openlocfilehash: 0ec22bd142f7509935691ff7bfcd38cb51a04fb2
ms.sourcegitcommit: fbb7924603f8915d07b5e6fc8f4d0c7f70c1a1e1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2018
ms.locfileid: "39280117"
---
# <a name="tutorial-combine-sales-data-from-excel-and-an-odata-feed"></a>Руководство. Объединение данных о продажах из Excel и веб-канала OData

Часто данные распределены по нескольким источникам, например сведения о товарах находятся в одной базе данных, а данные о продажах — в другой. Используя **Power BI Desktop**, вы можете объединить данные из нескольких источников и создать интересные аналитические данные и яркие визуализации. 

Из этого руководства вы узнаете, как объединить данные из двух источников данных: из книги Excel с данными о товарах и веб-канала OData с данными о заказах. Импортировав оба набора данных и применив к ним преобразование и статистическую обработку, вы сможете на их основе создать отчет с анализом продаж и интерактивными визуализациями. Эти же методы можно применить к запросам SQL Server, файлам CSV и любым другим источникам данных в Power BI Desktop.

>[!NOTE]
>В Power BI Desktop одну и ту же задачу можно выполнить разными способами. Например, многие элементы ленты доступны в контекстном меню или меню **Дополнительные параметры** для столбца или ячейки. В процедурах ниже описаны несколько разных способов. 

## <a name="import-the-product-data-from-excel"></a>Импорт данных о товарах из Excel

Сначала импортируйте данные из книги Excel Products.xlsx в Power BI Desktop.

1. [Скачайте книгу Excel Products.xlsx](http://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Products.xlsx) и сохраните ее с именем **Products.xlsx**.
   
2. Щелкните стрелку раскрывающегося списка рядом с элементом **Получить данные** на вкладке **Главная** ленты Power BI Desktop, а затем выберите **Excel** из раскрывающегося списка **Самые распространенные**. 
   
   ![Получать данные](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_1.png)
   
   >[!NOTE]
   >Можно также выбрать сам элемент **Получить данные** или элемент **Получить данные** в диалоговом окне Power BI **Начало работы**. После этого выберите **Excel** или **Файл** > **Excel** в диалоговом окне **Получение данных** и щелкните **Подключить**.
   
3. В диалоговом окне **Открыть** найдите и выберите файл **Products.xlsx**, а затем нажмите кнопку **Открыть**.
   
4. В области **Навигатор** выберите таблицу **Products** , а затем нажмите кнопку **Изменить**.
   
   ![Панель навигатора для Excel](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_2.png)
   
В **редакторе Power Query** откроется окно предварительного просмотра таблицы, где вы можете применить преобразования для очистки данных. 
   
![Редактор Power Query](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_3.png)
   
>[!NOTE]
>Также **редактор Power Query** можно открыть, выбрав **Изменить запросы** > **Изменить запросы** на ленте **Главная** в Power BI Desktop. Еще вы можете щелкнуть правой кнопкой мыши или выбрать **Дополнительные параметры** рядом с любым запросом в **представлении отчета**, а затем выбрать **Изменить запрос**.

## <a name="clean-up-the-products-columns"></a>Очистка столбцов в таблице товаров

Объединенный отчет будет использовать только столбцы **ProductID**, **ProductName**, **QuantityPerUnit** и **UnitsInStock** из этой книги Excel, а значит все остальные столбцы можно удалить. 

1. В **редакторе Power Query** выберите столбцы **ProductID**, **ProductName**, **QuantityPerUnit** и **UnitsInStock** (используйте сочетание **CTRL**+**щелчок**, чтобы выбрать несколько столбцов, или **SHIFT**+**щелчок**, чтобы выбрать несколько расположенных рядом столбцов).
   
2. Щелкните правой кнопкой мыши любой выбранный заголовок и выберите действие **Удалить другие столбцы** из раскрывающегося списка, чтобы удалить все столбцы, кроме выбранных. 
   Можно также выбрать **Удалить столбцы** > **Удалить другие столбцы** в группе **Управление столбцами** на вкладке ленты **Главная**. 
   
   ![Удаление других столбцов](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/analyzingsalesdata_removeothercolumns.png)

## <a name="import-the-order-data-from-an-odata-feed"></a>Импорт данных о заказах из веб-канала OData

Теперь следует импортировать данные о заказах из тестового веб-канала OData для торговой системы Northwind. 

1. В **редакторе Power Query** выберите **Создать источник**, а затем **Веб-канал OData** из раскрывающегося списка **Самые распространенные**. 
   
   ![Получение канала OData](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/get_odata.png)
   
2. В диалоговом окне **Веб-канал OData** вставьте URL-адрес веб-канала OData Northwind (`http://services.odata.org/V3/Northwind/Northwind.svc/`) и нажмите кнопку **ОК**.
   
   ![Диалоговое окно "Веб-канал OData"](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/get_odata2.png)
   
3. На панели **Навигатор** выберите таблицу **Orders**, а затем нажмите кнопку **ОК**, чтобы загрузить данные в **редактор Power Query**.
   
   ![Область навигатора для OData](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/analyzingsalesdata_odatafeed.png)
   
   >[!NOTE]
   >В области **Навигатор** вы можете открыть предварительный просмотр таблицы, щелкнув ее имя в любом месте, кроме флажка.

## <a name="expand-the-order-data"></a>Развертывание данных о заказах

Подключившись к источнику данных с несколькими таблицами, например к реляционным базам данных или к веб-каналу OData Northwind, вы можете использовать связи между таблицами для построения запросов. Таблица **Orders** содержит связи с несколькими таблицами. Вы можете добавить столбцы **ProductID**, **UnitPrice** и **Quantity** из связанной таблицы **Order_Details** в основную таблицу (**Orders**) с помощью операции **развертывания**. 

1. Прокрутите вправо таблицу **Orders** до столбца **Order_Details**. Обратите внимание, что он содержит не данные, а ссылки на другую таблицу.
   
   ![Столбец Order_Details](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/7.png)
   
2. Выберите значок **Развернуть** (![значок развертывания](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/expand.png)) в заголовке столбца **Order_Details**. 
   
3. В раскрывающемся списке **Развернуть** :
   
   1. Щелкните **(Выбрать все столбцы)** , чтобы отменить выбор всех столбцов.
      
   2. Выберите **ProductID**, **UnitPrice** и **Quantity**, в затем щелкните **ОК**.
      
      ![Диалоговое окно развертывания](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/8.png)

После развертывания таблицы **Order_Details** столбец **Order_Details** в ней заменяется тремя новыми столбцами из вложенной таблицы, и в таблицу добавляются новые строки с данными о каждом заказе. 

![Развернутые столбцы](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/9.png)

## <a name="create-a-custom-calculated-column"></a>Создание пользовательского вычисляемого столбца

Редактор Power Query позволяет создавать вычисления и настраиваемые поля для обогащения данных. В нашем примере вы создадите настраиваемый столбец, который вычисляет общую стоимость каждого элемента в заказе, умножая цену товара на количество единиц.

1. На вкладке ленты **Добавление столбца** в редакторе Power Query выберите **Настраиваемый столбец**.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/10.png)
   
2. В диалоговом окне **Настраиваемый столбец** введите значение **LineTotal** для поля **Имя нового столбца**.

3. В поле **Пользовательская формула столбца** после **=** введите формулу **[Order_Details.UnitPrice]** \* **[Order_Details.Quantity]**. (Можно не вводить имена полей, а выбрать их в области **Доступные столбцы** с ползунком полосы прокрутки и нажать кнопку **<< Вставить**.) 
3. Нажмите кнопку **ОК**.
   
   ![Диалоговое окно пользовательского столбца](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/11.png)

Новое поле с именем **LineTotal** появится в виде последнего столбца в таблице **Orders**.

## <a name="set-the-data-type-for-the-new-field"></a>Выбор типа данных для нового поля

Когда редактор Power Query подключается к источнику данных, он автоматические определяет наиболее подходящий тип данных для каждого поля и отображает данные соответствующим образом. Вы можете проверить назначенные полям типы по значкам в заголовках или просмотреть в разделе **Тип данных** группы **Преобразование** на вкладке ленты **Главная**. 

Новый столбец **LineTotal** имеет тип данных **Любой**, но фактически будет содержать значения валюты. Чтобы назначить ему тип данных, щелкните правой кнопкой мыши заголовок столбца **LineTotal** и выберите из раскрывающегося списка действие **Изменить тип данных**, а затем щелкните **Десятичное число с фиксированной запятой**. 

![Изменение типа данных](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/12.png)

>[!NOTE]
>Вы также можете сначала выбрать столбец **LineTotal**, а затем щелкнуть стрелку раскрывающегося списка рядом с элементом **Тип данных** в области **Преобразование** на вкладке ленты **Главная**, чтобы выбрать тип **Десятичное число с фиксированной запятой**.

## <a name="clean-up-the-orders-columns"></a>Очистка столбцов с данными о заказах

Чтобы модель было проще применять в отчетах, есть возможность удалить, переименовать и поменять местами некоторые столбцы.

Для отчета вам понадобятся только столбцы **OrderDate**, **ShipCity**, **ShipCountry**, **Order_Details.ProductID**, **Order_Details.UnitPrice** и **Order_Details.Quantity**. Вы можете выбрать нужные столбцы и использовать функцию **Удалить другие столбцы**, как мы уже делали с данными Excel, или выбрать все столбцы, кроме перечисленных, затем щелкнуть любой из выбранных столбцов правой кнопкой мыши и выбрать действие **Удалить столбцы**, чтобы удалить их все. 

Чтобы столбцы **Order_Details.ProductID**, **Order_Details.UnitPrice** и **Order_Details.Quantity** было проще идентифицировать, можно удалить префиксы *Order_Details.* из имен этих столбцов. Переименуйте эти столбцы в **ProductID**, **UnitPrice** и **Quantity** соответственно, выполнив следующие действия:

1. Дважды щелкните, коснитесь и удерживайте или щелкните правой кнопкой мыши заголовок каждого столбца и выберите из раскрывающегося списка действие **Переименовать**. 
2. Удалите префикс *Order_Details.* из каждого имени, затем нажмите клавишу **ВВОД**.

И наконец, чтобы упростить доступ к столбцу **LineTotal**, перетащите его влево и отпустите сразу за столбцом **ShipCountry**.

![Очищенная таблица](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/14.png)

## <a name="review-the-query-steps"></a>Просмотр шагов запроса

По мере того, как вы обрабатывали и преобразовывали данные в редакторе Power Query, каждый шаг сохранялся в область **Примененные шаги** на панели **Параметры запроса** в правой части окна редактора Power Query. Вы можете вернуться к области "Примененные шаги", чтобы просмотреть внесенные изменения и при необходимости изменить, удалить или переупорядочить их. Но это может быть небезопасно, так как изменение предыдущих шагов может испортить последующие действия. 

Поочередно выберите каждый из запросов в списке **Запросы** в левой части редактора Power Query и просмотрите область **Примененные действия** в разделе **Параметры запроса**. После применения всех предыдущих преобразований данных область "Примененные шаги" для двух запросов будет выглядеть примерно так:

![Примененные действия для запроса по таблице Products](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/15.png) &nbsp;&nbsp; ![Примененные действия для запроса по таблице Orders](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/17.png)

>[!TIP]
>В основе примененных действий — формулы, написанные на **языке Power Query**, который также известен как язык **M**. Чтобы просмотреть и изменить формулы, выберите **Расширенный редактор** в группе **Запрос** на вкладке "Главная" на ленте. 

## <a name="import-the-transformed-queries"></a>Импорт преобразованных запросов

Когда формат данных будет вас полностью устраивать, последовательно выберите **Закрыть и применить** > **Закрыть и применить** в группе **Закрыть** на вкладке ленты **Главная**, чтобы импортировать данные в Power BI Desktop. 

![Закрыть и применить](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_4.png)

После загрузки данных запросы появятся в списке **Поля** в представлении отчета Power BI Desktop.

![Запросы в списке "Поля"](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/18.png)

## <a name="manage-the-relationship-between-the-datasets"></a>Управление связями между наборами данных

Power BI Desktop не требует объединения запросов для формирования отчетов для них. Но вы можете применить связи между наборами данных, основанные на общих полях, для расширения и обогащения возможностей по созданию отчетов. Вы можете позволить Power BI Desktop автоматически обнаружить связи или можно создать нужные связи с помощью диалогового окна **Управление связями** в Power BI Desktop. Дополнительные сведения о связях в Power BI Desktop см. в статье [о создании связей и управлении ими](desktop-create-and-manage-relationships.md).

Наборы данных Orders и Products в нашем руководстве имеют общее поле *ProductID*, а значит между ними существует связь по значениям этого столбца. 

1. В представлении отчетов Power BI Desktop выберите **Управление связями** в области **Связи** на вкладке ленты **Главная**.
   
   ![Лента управления связями](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_5.png)
   
2. В диалоговом окне **Управление связями** можно заметить, что приложение Power BI Desktop уже обнаружило связь между таблицами Products и Orders и отобразило ее в списке. Чтобы просмотреть эту связь, выберите действие **Изменить**. 
   
   ![Диалоговое окно управления связями](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_6.png)
   
   Откроется диалоговое окно **Изменение связи** с информацией об этой связи.  
   
   ![Диалоговое окно изменения связи](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_7.png)
   
3. В Power BI Desktop правильно обнаружена связь, а значит вы можете просто закрыть это диалоговое окно, поочередно выбрав действия **Отменить** и **Закрыть**.

Также можно просматривать и администрировать связи между запросами с помощью представления **Связь** в левой части окна Power BI Desktop. Дважды щелкните стрелку на линии, соединяющей два запроса, чтобы открыть диалоговое окно **Изменение связи**, где вы можете просмотреть или изменить эту связь. 

![Представление связи](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_8.png)

Чтобы вернуться в представление отчета из представления связей, щелкните значок **Представление отчета**. 

![Значок представления отчетов](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_9.png)

## <a name="create-visualizations-using-your-data"></a>Создание визуализаций на основе данных

Представление отчета Power BI Desktop позволяет создавать различные визуализации для получения полезных сведений на основе собранных данных. Вы можете создавать отчеты из нескольких страниц, разместив на каждой из них несколько визуальных элементов. Вы и другие пользователи смогут взаимодействовать с этими визуализациями, чтобы оценивать и анализировать данные. Дополнительные сведения о просмотре и изменении отчетов в локальной службе Power BI см. в статье [о редактировании отчетов](service-interact-with-a-report-in-editing-view.md).

Вы можете использовать свои наборы данных и связь между ними, чтобы визуализировать и анализировать данные о продажах. 

Сначала создайте гистограмму с накоплением, в которой отображаются сведения о количестве заказов по каждому товару на основе данных из обоих запросов. 

1. Выберите поле **Quantity** из таблицы **Orders** на панели **Поля** справа или перетащите его на пустое место на холсте. Это действие создает гистограмму с накоплением, на которой отображается общее количество заказанных товаров. 
   
2. Теперь выберите **ProductName** из таблицы **Products** в области **Поля** или перетащите его на диаграмму, чтобы разбить данные о количестве по отдельным товарам. 
   
3. Теперь отсортируйте продукты по объему заказов от большего к меньшему, нажав кнопку **Дополнительные параметры** с символом многоточия (**...**) в верхнем правом углу визуализации, а затем выбрав действие **Сортировка по количеству**.
   
4. С помощью маркеров в углах диаграммы увеличьте ее размер, чтобы на ней отобразилось больше названий товаров. 
   
   ![Линейчатая диаграмма количества с разбивкой по полю ProductName](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/19.png)

Теперь создайте диаграмму, отображающую объем заказов в валюте (**LineTotal**) с распределением по времени (**OrderDate**). 

1. Убедитесь, что на холсте не выбраны элементы, и выберите **LineTotal** из таблицы **Orders** в области **Поля** или перетащите его на любое пустое место на холсте. Отобразится гистограмма с накоплением, на которой показан общий объем всех заказов в валютном выражении. 
   
2. Выберите эту диаграмму, а затем поле **OrderDate** из таблицы **Orders** или перетащите его на диаграмму. Теперь на диаграмме отображаются итоговые суммы по каждой дате, на которую существуют заказы. 
   
3. Измените размер визуализации, перетащив ее углы, чтобы увидеть больше данных. 
   
   ![График зависимости LineTotals от OrderDate](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/20.png)
   
   >[!TIP]
   >Если на диаграмме будут видны только годы (всего три точки данных), разверните раскрывающийся список рядом с элементом **OrderDate** в поле **Ось** на панели **Визуализация** и выберите **OrderDate** вместо **Иерархия дат**. 

Наконец, создайте визуализацию карты с отображением сумм по каждой стране. 

1. Убедитесь, что на холсте не выбраны элементы, и выберите **ShipCountry** из таблицы **Orders** в области **Поля** или перетащите его на любое пустое место на холсте. Power BI Desktop определит эти данные как названия стран и автоматически создаст визуализацию карты, обозначив точками данных все страны, для которых существуют заказы. 
   
2. Чтобы размер каждой точки данных соответствовал объему заказов для этой страны, перетащите на схему поле **LineTotal** (или перетащите его в область **Перетащите сюда поля с данными** под полем **Размер** в нижней части панели **Визуализация**). Теперь размеры кругов на карте будут отражать суммы заказов по соответствующим странам. 
   
   ![Визуализация карты для LineTotals с разбивкой по ShipCountry](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/21.png)

## <a name="interact-with-your-report-visuals-to-analyze-further"></a>Взаимодействие с визуальными элементами отчета для дальнейшего анализа

Power BI Desktop позволяет выявлять тенденции в данных, взаимодействуя с визуальными элементами, для которых реализованы перекрестное выделение и перекрестная фильтрация. Дополнительные сведения см. в статье [о фильтрации и выделении в отчетах](power-bi-reports-filters-and-highlighting.md). 

Связь между запросами позволяет изменять все визуализации на странице при взаимодействии с любой из них. 

Выберите на визуализации карты круг, расположенный в **Канаде**. Обратите внимание, что на двух других визуализациях данные о количестве строк и сумме заказов сразу отфильтровались по Канаде.

![Данные продаж, отфильтрованные по Канаде](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/22.png)

Если вы выберете любой из товаров на диаграмме **Quantity с разбивкой по ProductName**, на карте и на схеме с датами будут отобраны данные только по выбранному товару. Если вы выберете любую из дат на диаграмме **LineTotal с разбивкой по OrderDate**, на карте и диаграмме товаров будут отображаться данные только за выбранную дату. 
>[!TIP]
>Чтобы отменить выделение, щелкните выделенный элемент еще раз или выберите любую другую визуализацию. 

## <a name="complete-the-sales-analysis-report"></a>Завершение отчета об анализе продаж

В готовом отчете объединяются данные из файла Excel Products.xlsx и веб-канала OData Northwind и отображаются в визуальных элементах, которые позволяют анализировать сведения о заказах для разных стран, периодов и товаров. Готовый отчет можно [отправить в службу Power BI](desktop-upload-desktop-files.md), чтобы другие пользователи Power BI также могли его использовать.

## <a name="next-steps"></a>Дальнейшие действия
* [Прочитайте другие руководства по Power BI Desktop.](http://go.microsoft.com/fwlink/?LinkID=521937)
* [Посмотрите видеоматериалы по Power BI Desktop.](http://go.microsoft.com/fwlink/?LinkID=519322)
* [Посетите форум Power BI.](http://go.microsoft.com/fwlink/?LinkID=519326)
* [Прочитайте блог, посвященный Power BI.](http://go.microsoft.com/fwlink/?LinkID=519327)