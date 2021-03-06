---
title: Просмотр и изменение настроек параметров набора данных в службе Power BI
description: Параметры запроса создаются в Power BI Desktop, однако их можно просматривать и изменять в службе Power BI.
author: mihart
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 06/26/2018
ms.author: mihart
LocalizationGroup: Create reports
ms.openlocfilehash: ac271e8013bce5824931153351a651644a716a2f
ms.sourcegitcommit: 5eb8632f653b9ea4f33a780fd360e75bbdf53b13
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2018
ms.locfileid: "36965166"
---
# <a name="what-is-a-query-parameter"></a>Что такое параметр запроса?
Параметры запросов добавляются в Power BI Desktop авторами отчетов. Параметры позволяют создавать части отчетов в зависимости от *значений* одного или нескольких параметров. Например, автор отчета может создать параметр, который ограничивает данные одной страной или регионом, или параметр, который определяет число допустимых форматов для таких полей, как поле даты, времени и текста.

![Вкладка "Главная" с пунктом "Управление параметрами" в Desktop](media/service-parameters/power-bi-manage-parameters.png)


## <a name="review-and-edit-parameters-in-power-bi-service"></a>Просмотр и изменение параметров в службе Power BI

После определения параметров в Desktop при [публикации отчета в службе Power BI](desktop-upload-desktop-files.md) настройки параметров и выбранные варианты передаются вместе с этим отчетом. Некоторые настройки параметров можно просмотреть и изменить в службе Power BI, но не параметры, ограничивающие доступные данные, а параметры, которые определяют и описывают допустимые значения.

1. В службе Power BI щелкните значок шестеренки ![значок шестеренки](media/service-parameters/power-bi-cog.png), чтобы открыть окно **Параметры**.

2. Выберите вкладку **Наборы данных** и выделите набор данных в списке. 
    
    ![Окно "Параметры" с выбранной вкладкой "Наборы данных"](media/service-parameters/power-bi-select-dataset2.png)

3. Разверните узел **Параметры**.  Если выбранный набор данных не содержит параметры, вы увидите сообщение со ссылкой для получения дополнительных сведений о параметрах запроса. Однако если набор данных содержит параметры, развернув заголовок **Параметры**, вы увидите эти параметры. 

    ![Окно "Параметры" с развернутым разделом параметров](media/service-parameters/power-bi-settings.png)

    Просмотрите настройки параметров и при необходимости внесите изменения. Неактивные поля недоступны для редактирования. 


## <a name="next-steps"></a>Дальнейшие действия
Ситуативный способ добавления простых параметров путем [изменения URL-адреса](service-url-filters.md).