---
title: 'Пример "Рентабельность клиента" для Power BI: обзор'
description: 'Пример "Рентабельность клиента" для Power BI: обзор'
author: amandacofsky
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 06/23/2018
ms.author: mihart
LocalizationGroup: Samples
ms.openlocfilehash: fb06b83ca2fe949751337347c91b3947e115286d
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2018
ms.locfileid: "36944728"
---
# <a name="customer-profitability-sample-for-power-bi-take-a-tour"></a>Пример "Рентабельность клиента" для Power BI: обзор

## <a name="overview-of-the-customer-profitability-sample"></a>Обзор примера "Рентабельность клиента"
Пакет содержимого "Рентабельность клиента — пример" содержит панель мониторинга, отчет и набор данных для компании, производящей маркетинговые материалы. Эта панель мониторинга была создана финансовым директором для просмотра основных метрик о пяти руководителях подразделения, продуктах, клиентах и валовой прибыли. Здесь можно легко увидеть факторы, влияющие на прибыль.

![Панель мониторинга Power BI](media/sample-customer-profitability/power-bi-dash.png)

Этот образец входит в серию, демонстрирующую, как можно использовать Power BI с бизнес-данными, отчетами и информационными панелями. Это реальные данные из obviEnce ([www.obvience.com](http://www.obvience.com/)), которые были обезличены. Данные доступны в нескольких форматах: приложение или пакет содержимого, книга Excel или PBIX-файл (Power BI Desktop). См. статью [Примеры данных, доступные для использования в службе Power BI](sample-datasets.md).

## <a name="prerequisites"></a>Предварительные требования
Хотите попробовать? В этом руководстве используется служба Power BI и пример пакета содержимого "Рентабельность клиента".  Так как возможности отчетов очень похожи, вы также можете использовать Power BI Desktop и пример PBIX-файла. Инструкции по подключению к пакету содержимого и PBIX-файлу приведены ниже.

### <a name="get-the-content-pack-for-this-sample"></a>Получение пакета содержимого для этого примера

1. Откройте службу Power BI (app.powerbi.com) и войдите в систему.
2. В левом нижнем углу выберите **Получить данные**.

    ![получение данных](media/sample-datasets/power-bi-get-data.png)
3. На странице "Получение данных" щелкните значок **Примеры**.

   ![Значок примера](media/sample-datasets/power-bi-samples-icon.png)
4. Выберите **Рентабельность клиента — пример**, затем выберите **Подключиться**.  

   ![Получить данные](media/sample-customer-profitability/get-supplier-sample.png)
5. Power BI импортирует пакет содержимого и добавляет новую информационную панель, отчет и набор данных в текущую рабочую область. Новое содержимое отмечено желтой звездочкой. Используйте примеры для тестового запуска Power BI.  

   ![Звездочка](media/sample-customer-profitability/supplier-sample-asterisk.png)

### <a name="get-the-pbix-file-for-this-sample"></a>Получение PBIX-файла для этого примера

Также вы можете загрузить пример в виде PBIX-файла, который предназначен для работы с Power BI Desktop.
[Рентабельность клиента — пример](http://download.microsoft.com/download/6/A/9/6A93FD6E-CBA5-40BD-B42E-4DCAE8CDD059/Customer%20Profitability%20Sample%20PBIX.pbix)

### <a name="get-the-excel-workbook-for-this-sample"></a>Получение книги Excel для этого примера

При необходимости вы также можете просмотреть источник данных для этого примера, который доступен в виде[книги Excel](http://go.microsoft.com/fwlink/?LinkId=529781). Книга содержит листы Power View, которые можно просматривать и изменять. Чтобы просмотреть необработанные данные выберите элементы **Power Pivot > Управление**.


## <a name="what-is-our-dashboard-telling-us"></a>Какие данные отображаются на информационной панели?

В разделе **Моя рабочая область** найдите панель мониторинга для примера "Рентабельность клиента":

![Панель мониторинга для примера "Рентабельность клиента"](media/sample-customer-profitability/power-bi-dash.png)

### <a name="company-wide-dashboard-tiles"></a>Плитки панели мониторинга, охватывающей всю компанию
1. Откройте панель мониторинга в службе Power BI. Плитки панелей мониторинга позволяют нашему финансовому директору отслеживать важные метрики на уровне всей компании.  Когда она видит что-либо интересное, она выбирает плитку, чтобы проанализировать данные более подробно.

2. Просмотрите плитки слева на панели мониторинга.

    ![Плитки для руководителей](media/sample-customer-profitability/power-bi-manager.png)

- Валовая прибыль нашей компании составляет 42,5 %.
- У нас 80 клиентов.
- Мы продаем 5 разных продуктов.
- В феврале у нас наблюдалось наименьшее расхождение дохода с бюджетом, а в марте — наибольшее.
- Основная часть нашего дохода поступает из восточного (East) и северного (North) регионов. Валовая прибыль никогда не выходила за пределы бюджета, ER-0 и MA-0 требуется изучить более подробно.
- Итоговый доход за этот год приближается к бюджету.


### <a name="manager-specific-dashboard-tiles"></a>Плитки панели мониторинга по отдельным руководителям
Плитки в правой части панели мониторинга содержат показатели команды. Финансовому директору нужно следить за работой своих руководителей, а эти плитки дают общее представление о доходах с использованием доли валовой прибыли (GM%). Если для любого из руководителей возникает неожиданная тенденция по доле валовой прибыли, директор может подробнее изучить данный вопрос.

![GM% для руководителей](media/sample-customer-profitability/power-bi-manager2.png)

- Все руководители, за исключением Карлоса, превысили показатели целевых продаж. Но у него самый высокий показатель фактических продаж.
- Руководитель Annelie имеет самую низкую долю валовой прибыли, но с марта этот показатель стабильно увеличивается.
- С другой стороны, у Valery наблюдается значительное снижение показателя GM%.
- У Andrew наблюдается переменный успех.

## <a name="explore-the-dashboards-underlying-data"></a>Просмотр базовых данных панели мониторинга
На этой панели мониторинга содержатся плитки со ссылками на отчет и книгу Excel.

### <a name="open-the-excel-online-data-source"></a>Открытие источника данных в Excel Online
На этой панели мониторинга закреплены две плитки из книги Excel: Target vs Actual (Целевые и фактические продажи) и Year Over Year Revenue Growth (Рост дохода в годовом исчислении). Поэтому если вы щелкните любую из этих плиток, Power BI откроет источник данных. В этом случае это Excel Online.

![Excel Online](media/sample-customer-profitability/power-bi-excel-online.png)

1. Выберите одну из плиток, закрепленных из Excel. Excel Online откроется в службе Power BI.
2. Обратите внимание, что книга содержит три вкладки с собранными данными. Откройте вкладку "Revenue" (Доход).
3. Давайте узнаем, почему Карлос еще не достиг этих показателей.  
    а. В области ползунка "Executive" (Руководитель) выберите **Carlos Grilo**.   
    б. На первой сводной таблице показано, что доход Карлоса за его основной продукт (Primus) снизился на 152 % по сравнению с прошлым годом. На диаграмме роста дохода в годовом исчислении показано, что для большинства месяцев эти показатели ниже суммы, заложенной в бюджете.  

    ![Сводная таблица](media/sample-customer-profitability/power-bi-pivotchart.png)

    ![Результаты для Карлоса](media/sample-customer-profitability/power-bi-carlos.png)

4. Продолжайте просмотр. Если вы найдете что-то интересное, выберите **Закрепить**![Значок закрепления](media/sample-customer-profitability/power-bi-excel-pin.png) в правом верхнем углу, чтобы [закрепить элемент на панели мониторинга](service-dashboard-pin-tile-from-excel.md).

5. Чтобы вернуться на панель мониторинга, нажмите кнопку со стрелкой назад в браузере.

### <a name="open-the-underlying-power-bi-report"></a>Открытие основного отчета Power BI
Большинство плиток на панели мониторинга примера "Рентабельность клиента" закреплены из соответствующего базового примера отчета.

1. Выберите одну из этих плиток, чтобы открыть отчет в режиме чтения.

2. Отчет содержит 3 страницы. Каждая вкладка в нижней части отчета представляет страницу.

    ![Три вкладки внизу](media/sample-customer-profitability/power-bi-report-tabs.png)

    * Team Scorecard (Командная система показателей) содержит сведения о работе и показателях 5 руководителей.
    * Industry Margin Analysis (Анализ прибыльности по отрасли) позволяет проанализировать нашу рентабельность с учетом состояния дел в отрасли.
    * Executive Scorecard (Система показателей руководства) позволяет просмотреть данные для каждого из руководителей в формате, доступном для Кортаны.

### <a name="team-scorecard-page"></a>Страница Team Scorecard (Командная система показателей)
![Командная система показателей отчета](media/sample-customer-profitability/customer2.png)

Рассмотрим подробнее двух членов команды и разберемся, какие именно сведения можно получить. В срезе слева выберите имя Andrew, чтобы отфильтровать страницу отчета и отобразить только сведения об Andrew.

* Для быстрого определения ключевого показателя эффективности посмотрите на поле **Revenue Status** (Состояние дохода) Andrew — оно зеленое. Этот руководитель работает хорошо.
* Диаграмма с областями Revenue Var % to Budget by Month (Отклонение дохода от бюджета по месяцам) показывает, что за исключением отставания в феврале Andrew в целом обеспечивает приемлемые показатели. Он в основном работает в восточном регионе и обрабатывает 49 клиентов и 5 (из 7) продуктов. Его показатель GM% не является самым высоким или самым низким.
* RevenueTY and Revenue Var % to Budget by Month (Доход за этот год и отклонение дохода от бюджета по месяцам) показывает, что уровень доходов неуклонно растет. Но если щелкнуть квадрат для центрального региона (**Central**) на диаграмме "дерево", выясняется, что Andrew имеет доход только в марте и только в Индиане. Это запланированное поведение, или стоит разобраться в этом подробнее?

Теперь перейдем к Valery. В срезе выберите имя Valery, чтобы отфильтровать страницу отчета и отобразить только данные об этом руководителе.  
![Срез с данными руководителя для Valery Ushalov](media/sample-customer-profitability/customer3.png)

* Обратите внимание на красный ключевой показатель эффективности для **RevenueTY Status**(Состояние дохода за этот год). Это определенно требует более подробного рассмотрения.
* У этого руководителя наблюдаются проблемы и с отклонением дохода, так как установленные границы доходности не соблюдаются.
* Valery имеет всего 9 клиентов, обрабатывает только 2 продукта и работает практически только с клиентами в северном регионе. Такая специализация может объяснять широкие колебания метрик этого руководителя.
* При выборе квадрата **North** (север) на диаграмме-дереве становится видно, что валовая прибыль Valery в северном регионе согласуется с общим уровнем прибыли.
* Выбирая другие квадраты **Region** (Регион), можно узнать о сложившейся ситуации: у этого руководителя показатель GM% колеблется в пределах от 23 % до 79 %, а показатели доходов во всех регионах, за исключением северного, имеют четко выраженный сезонный характер.

Продолжайте анализировать данные, чтобы узнать о причинах низкой производительности Valery. Просмотрите регионы, другие подразделения, а также следующую страницу отчета — Industry Margin Analysis (Маржинальный анализ по отрасли).

### <a name="industry-margin-analysis"></a>Industry Margin Analysis (Маржинальный анализ по отрасли)
Эта страница отчета содержит другой срез данных. На ней рассматривается валовая прибыль для всей отрасли, разделенной на сегменты. Финансовый директор использует эту страницу для сравнения метрик компании и подразделений с метриками всей отрасли, чтобы выявлять и обеспечивать рентабельность. Вы можете спросить, почему на этой странице приведена диаграмма с областями Gross margin by Month and Executive Name (Валовая прибыль по месяцу и имени руководителя), хотя она относится к конкретной команде. Ее наличие позволяет отфильтровать страницу по руководителю подразделения.  
![Страница отчета "Маржинальный анализ по отрасли"](media/sample-customer-profitability/customer6.png)

Как рентабельность зависит от отрасли? Как распределяются продукты и клиенты в зависимости от отрасли? Выберите одну или несколько отраслей в верхней левой части. (Начните с отрасли CPG) Чтобы очистить фильтр, выберите значок очистки.

На пузырьковой диаграмме финансовый директор ищет самые крупные пузырьки, так как именно они оказывают наибольшее влияние на прибыль. Поскольку данные на странице можно отфильтровать по руководителю, щелкнув его имя на диаграмме с областями, это позволяет легко определить влияние каждого руководителя с учетом отраслевого сегмента.

* У руководителя Andrew область влияния распространяется на множество разных отраслевых сегментов, а показатели GM% и Var% изменяются в широких пределах, причем первый больше изменяется в положительную сторону.
* Annelie имеет аналогичную диаграмму, однако данный руководитель работает лишь с несколькими отраслевыми сегментами, специализируясь на федеральном сегменте и продукте Gladius.
* Carlos специализируется на сегменте служб и получает хороший доход. Он значительно улучшил отклонение по высокотехнологичному сегменту, а также продемонстрировал крайне высокие показатели относительно бюджета в новом для себя сегменте — промышленном.
* Tina работает с небольшим количеством сегментов и имеет наибольший показатель GM%, однако небольшой размер пузырьков показывает, что данный руководитель оказывает минимальное влияние на доходы компании.
* Valery, который отвечает только за один продукт, работает всего в 5 отраслевых сегментах. Влияние этого руководителя носит сезонный характер, но всегда дает крупные пузырьки, указывая на ощутимый вклад в доходы компании. Объясняется ли низкая производительность этого руководителя особенностями отрасли?

### <a name="executive-scorecard"></a>Executive Scorecard (Система показателей руководства)
Эта страница имеет формат карты ответов Кортаны. Дополнительные сведения см. в разделе [Создание карты ответов, предназначенной для Кортаны](service-cortana-answer-cards.md).

## <a name="dig-into-the-data-by-asking-questions-with-qa"></a>Углубленное изучение данных с помощью задания вопросов в поле вопросов и ответов
Для нашего анализа было бы полезно определить, из какой отрасли Valery получает наибольший доход. Давайте воспользуемся вопросами и ответами.

1. Откройте отчет в режиме правки, выбрав пункт **Изменить отчет**. Режим правки доступен только владельцу отчета. Также этот режим иногда называют режимом **автора**. Если же к этому отчету вам предоставлен общий доступ, вы не сможете открыть его в режиме правки.

2.  В верхней строке меню выберите **Задать вопрос**, чтобы открыть поле вопросов и ответов.

    ![Задать вопрос о своих данных](media/sample-customer-profitability/power-bi-ask-question.png)

3. Введите **total revenue by industry for Valery**(Общий доход по отрасли для Valery). Обратите внимание на обновление визуализации по мере ввода вопроса.

    ![Введите вопрос в поле для вопросов](media/sample-customer-profitability/power-bi-qna.png)

   Основной областью доходов Valery является распространение.

### <a name="dig-deeper-by-adding-filters"></a>Углубленное изучение с помощью фильтров
Давайте рассмотрим отрасль *распространения* .  

1. Откройте страницу отчета Industry Margin Analysis (Маржинальный анализ по отрасли).
2. Не выбирая визуализации на странице отчета, разверните область фильтров справа, если она еще не развернута. В области "Фильтры" должны отобразиться только фильтры уровня страницы.  

   ![Фильтры уровня страницы](media/sample-customer-profitability/power-bi-filters.png)
3. Найдите фильтр для **отрасли** и щелкните стрелку, чтобы развернуть список. Теперь добавим фильтр страницы для отрасли распространения. Сначала очистите все выделения, сняв флажок **Выделить все**. Затем установите только флажок **Распределение**.  

   ![Фильтры для сбыта](media/sample-customer-profitability/customer7.png)
4. На диаграмме с областями Gross margin by Month and Executive Name (Валовая прибыль по месяцу и имени руководителя) видно, что клиенты из данной отрасли есть только у Valery и Tina, а Valery работает с этой отраслью только с июня по ноябрь.   
5. Выберите **Tina**, а затем **Valery** в условных обозначениях диаграммы с областями "Gross margin by Month and Executive" (Валовая прибыль по месяцу и имени руководителя). Обратите внимание, что доля Total Revenue by Product (Общий доход по продукту) у Tina гораздо меньше, чем у Valery.
6. Чтобы просмотреть фактический доход, воспользуйтесь полем вопросов и ответов и задайте вопрос об **общем доходе от распространения по сценарию и руководителю**.  

     ![Введите вопрос в поле для вопросов, чтобы просмотреть линейчатую диаграмму](media/sample-customer-profitability/power-bi-qna2.png)

    Аналогичным образом можно изучить другие отрасли и даже добавить клиентов в визуальные элементы, чтобы понять причины такого уровня производительности Valery.

В такой безопасной среде можно работать. Отказаться от сохранения изменений можно в любой момент. Однако если изменения сохраняются, всегда можно выбрать функцию **Получить данные** для получения новой копии этого образца.

Вы также можете [скачать только набор данных (книга Excel) для этого примера](http://go.microsoft.com/fwlink/?LinkId=529781).

## <a name="next-steps-connect-to-your-data"></a>Дальнейшие действия: подключение к данным
Мы надеемся, что в этом обзоре вы узнали, каким образом с помощью информационных панелей, вопросов и ответов и отчетов можно получить представление о данных по клиентам. Теперь ваша очередь — выполните подключение к собственным данным. С помощью Power BI можно подключаться ко многим типам источников данных. Узнайте больше о [начале работы с Power BI](service-get-started.md).

[Назад к примерам в Power BI](sample-datasets.md)  
