---
title: Кольцевые диаграммы в Power BI
description: Кольцевые диаграммы в Power BI
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 09/24/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: ab292964bb1b6b1f4218d41c46eb2c28c82a034c
ms.sourcegitcommit: ce8332a71d4d205a1f005b703da4a390d79c98b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47416758"
---
# <a name="doughnut-charts-in-power-bi"></a>Кольцевые диаграммы в Power BI
Кольцевая диаграмма похожа на круговую диаграмму в том, что она показывает отношение между целым и частями. Единственное отличие в том, что центр диаграммы пуст и в него можно добавить подпись или значок.

## <a name="create-a-doughnut-chart"></a>Создание кольцевой диаграммы
В этих инструкциях используется набор данных "Анализ розничной торговли — прием" для создания кольцевой диаграммы, в которой отображаются продажи за этот год по категориям. Чтобы продолжить работу, [скачайте пример](../sample-datasets.md) для службы Power BI или Power BI Desktop.

1. Начните с [пустой страницы отчета](../power-bi-report-add-page.md). Если вы используете службу Power BI, нужно открыть отчет в [режиме правки](../service-interact-with-a-report-in-editing-view.md).

2. В области "Поля" выберите **Продажи**\>**Продажи за прошлый год**.  
   
3. В области "Визуализации" щелкните значок кольцевой диаграммы ![значок кольцевой диаграммы](media/power-bi-visualization-doughnut-charts/power-bi-icon.png), чтобы преобразовать линейчатую диаграмму в кольцевую. Если поля **Продажи за прошлый год** нет в области **Значения**, перетащите его туда.
     
   ![Панель визуализации с выбранным значком кольцевой диаграммы](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-chart.png)

4. Выберите **Элемент** \> **Категория**, чтобы добавить его в область **Условные обозначения**. 
     
    ![кольцевая диаграмма рядом с областью полей](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-done.png)

5. При необходимости [настройте размер и цвет текста диаграммы](power-bi-visualization-customize-title-background-and-legend.md). 

## <a name="considerations-and-troubleshooting"></a>Рекомендации и устранение неполадок
* Сумма значений кольцевой диаграммы должна составлять 100 %.
* Слишком большое число категорий затрудняет чтение и понимание.
* Кольцевые диаграммы лучше подходят для сравнения определенной части с целым, а не отдельных частей друг с другом. 

## <a name="next-steps"></a>Дальнейшие действия
[Воронкообразные диаграммы в Power BI](power-bi-visualization-funnel-charts.md)

[Типы визуализаций в Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)


