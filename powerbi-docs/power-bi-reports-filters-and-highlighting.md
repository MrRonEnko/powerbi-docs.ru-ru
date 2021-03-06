---
title: О фильтрах и выделении в отчетах Power BI
description: О фильтрах и выделении в отчетах Power BI
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 05/26/2018
ms.author: maggies
LocalizationGroup: Reports
ms.openlocfilehash: de4fc463b02e8cae59f20216b5b1d30be431ae98
ms.sourcegitcommit: fb1885da7cf11367660edbf7b7346dc039ee9b5d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "47187175"
---
# <a name="about-filters-and-highlighting-in-power-bi-reports"></a>О фильтрах и выделении в отчетах Power BI
***Фильтры*** удаляют все данные, кроме необходимых.  ***Выделение*** не является фильтрацией, так как оно не удаляет данные, а выделяет подмножество отображаемых данных. Невыделенные данные остаются видимыми и имеют серый цвет.

Есть много способов фильтровать и выделять отчеты в Power BI. Если описать их все в одной статье, вы запутаетесь. Поэтому мы разбили информацию на следующие блоки.

* Общие сведения о фильтрах и выделении (статья, которую вы читаете сейчас).
* Способы, с помощью которых вы можете [создавать и использовать фильтры и выделение в режиме правки или в своих отчетах](power-bi-report-add-filter.md). Если у вас есть разрешение править отчеты, вы можете создавать, изменять и удалять фильтры и выделения в отчетах.
* Способы, с помощью которых вы можете [использовать фильтры и выделения в отчетах, которыми с вами поделились, или в режиме чтения](consumer/end-user-reading-view.md). Хоть возможности и ограничены, в Power BI все равно доступны разные средства фильтрации и выделения.  
* [Подробная информация об элементах управления фильтрацией и выделением, которые доступны в режиме правки](consumer/end-user-report-filter.md), в том числе подробная информация о типах фильтров (включая фильтры по дате и времени, числовые и текстовые фильтры) и о разнице между основными и расширенными параметрами.
* Узнав, как по умолчанию работают фильтры и выделение, [научитесь изменять способы, с помощью которых визуализации на странице фильтруют и выделяют друг друга](consumer/end-user-interactions.md).

> [!TIP]
> Как служба Power BI определяет, что данные связаны между собой?  Power BI использует связи между таблицами и полями в базовой [модели данных](https://support.office.com/article/Create-a-Data-Model-in-Excel-87e7a54c-87dc-488e-9410-5c75dbcb0f7b?ui=en-US&rs=en-US&ad=US), чтобы элементы на странице отчета могли взаимодействовать друг с другом.
> 
> 

## <a name="introduction-to-filters-and-highlighting-in-reports-using-the-filters-pane"></a>Основные сведения о том, как с помощью панели "Фильтры" выполнять фильтрацию и выделение в отчетах
 Эта статья описывает фильтрацию и выделение данных в службе Power BI.  Однако в Power BI Desktop применяется практически такая же процедура.  

![](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-reading-view.png)

Фильтры и выделение можно применять с помощью панели **Фильтры**. Также для этого можно выбрать нужные элементы непосредственно в отчете (ad-hoc-отчет, см. внизу страницы). На панели "Фильтры" отображаются таблицы и поля, используемые в отчете, а также примененные фильтры, если таковые есть. Есть такие категории фильтров: **фильтры уровня страницы**, **детализация**, **фильтры уровня отчета** и **фильтры уровня визуальных элементов**.  Фильтры уровня визуальных элементов отображаются, только если вы выбрали визуализацию на холсте отчета.

> [!TIP]
> Если напротив фильтра отображается слово **Все**, это значит, что в качестве фильтра используется все поле.  Например, поле **Chain(All)**, изображенное на снимке экрана ниже, означает, что эта страница отчета включает данные обо всех сетях магазинов.  С другой стороны, фильтр уровня отчета **FiscalYear is 2013 or 2014** означает, что в отчет включены только данные за финансовые года 2013 и 2014.
> 
> 

## <a name="filters-in-reading-view-versus-editing-view"></a>Сравнение фильтров в режиме чтения и правки
Есть два режима взаимодействия с отчетами: [режим чтения и режим правки](consumer/end-user-reading-view.md).  Доступные возможности фильтрации зависят от используемого в настоящий момент режима.

* В режиме правки можно добавлять фильтры страниц, отчетов, детализаций и визуальных элементов. При сохранении отчета фильтры сохраняются вместе с ним, даже если он открыт в мобильном приложении. Пользователи, просматривающие отчет в режиме чтения, могут работать с добавленными вами фильтрами, но не могут добавлять новые фильтры.
* В режиме чтения можно взаимодействовать с любыми уже существующими в отчете фильтрами, а также сохранять выбранные элементы.  Однако вы не можете добавлять новые фильтры.

### <a name="the-filters-pane-in-reading-view"></a>Панель "Фильтры" в режиме чтения
Если у вас есть доступ к отчетам только в режиме чтения, панель "Фильтры" выглядит так:

![](media/power-bi-reports-filters-and-highlighting/power-bi-filter-reading-view.png)

Эта страница отчета содержит шесть фильтров уровня страницы и один фильтр уровня отчета.

Чтобы узнать, есть ли фильтры визуализаций, выберите визуализацию. На изображении ниже к пузырьковой диаграмме применены шесть фильтров.

![](media/power-bi-reports-filters-and-highlighting/power-bi-filter-visual-level.png)

Просмотрите данные в режиме чтения, изменяя существующие фильтры. Вносимые изменения сохраняются вместе с отчетом, даже если он открыт в мобильном приложении. Дополнительные сведения см. в статье [Режимы чтения и правки в службе Power BI](consumer/end-user-reading-view.md).

### <a name="the-filters-pane-in-editing-view"></a>Панель "Фильтры" в режиме правки
Если у вас есть разрешения владельца и вы открываете отчет в режиме правки, доступна не только панель **Фильтры**, но и несколько других панелей правки.

![](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-editing-view.png)

Видно, что эта страница отчета, как и страница, открытая в режиме чтения (выше), содержит шесть фильтров уровня страницы и один фильтр уровня отчета. Если выберем пузырьковую диаграмму, мы увидим, что к ней применены шесть фильтров уровня визуальных элементов.

При этом в режиме правки доступны и другие возможности, связанные с фильтрацией и выделением. Основная разница в том, что можно добавлять новые фильтры. О том, как делать это и многое другое, см. в статье [Добавление фильтра в отчет в Power BI](power-bi-report-add-filter.md).

## <a name="ad-hoc-filtering-and-highlighting"></a>Фильтрация и выделение в ad-hoc-отчете
Выберите поле на холсте отчета, который нужно отфильтровать, и выделите оставшуюся часть страницы. В этой же визуализации выберите пустое место, чтобы удалить его. Этот тип фильтрации и выделения позволяет быстро изучить влияние данных. Чтобы настроить этот тип фильтрации и выделения, см. статью [Взаимодействие визуальных элементов](consumer/end-user-interactions.md).

![](media/power-bi-reports-filters-and-highlighting/power-bi-adhoc-filter.gif)

При выходе из отчета ваши изменения сохраняются. Чтобы отменить настройки фильтрации и вернуться к настройкам фильтрации, срезов, детализации и сортировки по умолчанию, заданным автором отчета, в верхней строке меню выберите **Вернуться к значениям по умолчанию**.

![](media/power-bi-reports-filters-and-highlighting/power-bi-reset-to-default.png)

## <a name="next-steps"></a>Дальнейшие действия
[Взаимодействие с фильтрами и выделение (в режиме чтения)](consumer/end-user-reading-view.md)

[Добавление фильтра в отчет (в режиме правки)](power-bi-report-add-filter.md)

[Ознакомление с фильтрами отчетов](consumer/end-user-report-filter.md)

[Взаимодействие с визуализациями в отчете Power BI](consumer/end-user-interactions.md)

Дополнительные сведения об [отчетах в Power BI](consumer/end-user-reports.md)

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)

