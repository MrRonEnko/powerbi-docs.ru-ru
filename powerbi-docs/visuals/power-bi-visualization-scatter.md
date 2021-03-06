---
title: Точечные диаграммы в Power BI
description: Точечные диаграммы в Power BI
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: PVcfPoVE3Ys
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 09/28/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: bd09adf21292b16ee27f111ac92bbd8c83c384d8
ms.sourcegitcommit: 769ef3c8cbafd9ad5979eb4023a394ac7dba8d02
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2018
ms.locfileid: "47448852"
---
# <a name="scatter-charts-and-bubble-charts-in-power-bi"></a>Точечные и пузырьковые диаграммы в Power BI
Точечная диаграмма всегда включает две оси значений: вдоль горизонтальной оси отображается один набор числовых данных, а вдоль вертикальной — другой. На диаграмме отображаются точки пересечения числовых значений X и Y, объединяя их в отдельные точки данных. Точки данных могут распределяться вдоль горизонтальной оси равномерно или неравномерно в зависимости от данных.

В пузырьковой диаграмме точки данных заменяются пузырьками, *размер* которых представляет собой дополнительное измерение данных.

![Пример пузырьковой диаграммы](media/power-bi-visualization-scatter/power-bi-bubble-chart.png)

Вы можете задать количество точек данных (не более 10 000).  

## <a name="when-to-use-a-scatter-chart-or-bubble-chart"></a>Выбор точечной или пузырьковой диаграммы
### <a name="scatter-charts-are-a-great-choice"></a>Точечную диаграмму следует использовать:
* для демонстрации отношений между двумя (точечная диаграмма) или тремя (пузырьковая диаграмма) **числовыми** значениями;
* для отображения на диаграмме двух групп чисел в одном пространстве координат XY;
* вместо графика, если вам нужно изменить масштаб горизонтальной оси;    
* для включения горизонтальной оси в логарифмическую шкалу;
* для отображения данных листа, содержащих пары или сгруппированные наборы значений. На точечной диаграмме можно изменять масштабы осей и, таким образом, открывать дополнительную информацию о сгруппированных значениях;
* для отображения повторяющихся комбинаций в больших наборах данных, например в виде линейных или нелинейных тенденций, кластеров и выбросов;
* для сравнения больших количеств точек данных без учета времени.  Чем больше данных вы включите в точечную диаграмму, тем точнее будет сравнение.

### <a name="bubble-charts-are-a-great-choice"></a>Пузырьковую диаграмму следует использовать:
* если данные имеют три временных ряда, каждый из которых содержит набор значений;
* для представления финансовых данных.  Разный размер пузырьков привлекает внимание к определенным значениям;
* для использования с квадрантами.

## <a name="create-a-scatter-chart"></a>Создание точечной диаграммы
Просмотрите это видео, в котором Уилл создает точечную диаграмму, а затем выполните следующие действия, чтобы создать ее.

<iframe width="560" height="315" src="https://www.youtube.com/embed/PVcfPoVE3Ys?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>


Здесь используется пример "Анализ розничной торговли". Чтобы продолжить работу, [скачайте пример](../sample-datasets.md) для службы Power BI (app.powerbi.com) или Power BI Desktop.   

1. Откройте отчет в режиме редактирования и щелкните желтый значок "плюс", чтобы создать [пустую страницу отчета](../power-bi-report-add-page.md).
 
2. На панели Fields (Поля) выберите следующие поля:
   - **Sales** > **Sales Per Sq Ft** (Продажи > Продажи на кв. фут)
   - **Sales** > **Total Sales Variance %** (Продажи > Суммарное отклонение продаж, %)
   - **District** > **District** (Округ > Округ)

     ![](media/power-bi-visualization-scatter/power-bi-bar-chart.png)

     Если вы используете службу Power BI, нужно открыть отчет в [режиме правки](../service-interact-with-a-report-in-editing-view.md).

3. Преобразуйте данные в точечную диаграмму. На панели «Визуализации» щелкните значок точечной диаграммы.

   ![](media/power-bi-visualization-scatter/pbi_scatter_chart_icon.png).

4. Перетащите поле **District** (Округ) из раздела **Сведения** в раздел **Условные обозначения**. Мы получили точечную диаграмму, в которой по оси Y показывается **суммарное отклонение продаж в %**, а по оси X — **продажи на кв. фут**. Цвета точек данных указывают регионы.

    ![](media/power-bi-visualization-scatter/power-bi-scatter.png)

Теперь добавим третье измерение.

## <a name="create-a-bubble-chart"></a>Создание пузырьковой диаграммы

1. Из области **Fields** (Поля) перетащите **Sales** > **This Year Sales** > **Value** (Продажи > Продажи за этот год > Значение) в область **Size** (Размер). Размеры точек данных увеличатся пропорционально соответствующим значениям продаж.
   
   ![](media/power-bi-visualization-scatter/power-bi-bubble.png)

2. Наведите указатель мыши на пузырек. Размер пузырька отражает значение параметра **Продажи за этот год**.
   
    ![](media/power-bi-visualization-scatter/pbi_scatter_chart_hover.png)

3. Чтобы установить число точек данных, отображаемых на пузырьковой диаграмме, откройте раздел **Форматирование** на панели **Визуализации**, разверните карточку **Общие** и установите значение **Объем данных**. В качестве максимального объема данных можно установить любое число вплоть до 10 000. При использовании больших значений рекомендуется предварительно провести тестирование, чтобы обеспечить достаточную производительность. 

    ![Объем данных](media/power-bi-visualization-scatter/pbi_scatter_data_volume.png) 

   > [!NOTE]
   > Чем больше точек данных, тем дольше будет выполняться загрузка. Если вы решите опубликовать отчет с высокими значениями ограничений, обязательно проверьте его работу через Интернет и на мобильных устройствах. Так вы убедитесь в том, что производительность соответствует ожиданиям пользователей. Обратите внимание, что для большого количества точек данных следует выполнить тестирование результатов в различных форм-факторах для обеспечения оптимальной производительности.

4. Вы можете [форматировать цвета, метки, заголовки, фон и другие параметры визуализации](service-getting-started-with-color-formatting-and-axis-properties.md). Для [улучшения доступности](../desktop-accessibility.md) рассмотрите возможность добавления меток в каждую линию. Благодаря использованию разных форм меток для каждой линии пользователям отчетов легче различать линии (или области). Чтобы выбрать форму метки, разверните карточку **Shapes** (Фигуры) и выберите нужную форму.

      ![Форма маркера](media/power-bi-visualization-scatter/pbi_scatter_marker.png)

   Можно также изменить форму маркера: ромб, треугольник или квадрат.

   ![Квадратный маркер](media/power-bi-visualization-scatter/pbi_scatter_chart_hover_square.png)


## <a name="considerations-and-troubleshooting"></a>Рекомендации и устранение неполадок

### <a name="your-scatter-chart-has-only-one-data-point"></a>**Точечная диаграмма содержит только одну точку данных**
Ваша точечная диаграмма содержит только одну точку данных, представляющую сумму всех значений на осях X и Y?  А может быть, эта точка представляет собой сумму всех значений только по горизонтальной или по вертикальной оси?

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot1.png)

Добавьте поле в область **Сведения** , чтобы сообщить Power BI, каким образом нужно группировать значения. Поле должно быть уникальным для каждой точки, которую нужно отобразить. Это может быть просто номер строки или поле идентификатора.

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot.png)

Если ваши данные не содержат таких значений, создайте поле, которое объединяет значения X и Y в уникальный атрибут точки:

![](media/power-bi-visualization-scatter/pbi_scatter_tshoot2.png)

Для создания нового поля [используйте редактор запросов Power BI Desktop, чтобы добавить столбец индекса](../desktop-add-custom-column.md) в свой набор данных.  Затем добавьте этот столбец в область **Сведения** визуализации.

## <a name="next-steps"></a>Дальнейшие действия

[Точечные диаграммы с высокой плотностью](desktop-high-density-scatter-charts.md)

[Типы визуализаций в Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)

