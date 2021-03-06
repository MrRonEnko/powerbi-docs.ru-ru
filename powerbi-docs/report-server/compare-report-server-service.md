---
title: Сравнение решения "Сервер отчетов Power BI" и службы Power BI
description: В этой статье сравниваются возможности решения "Сервер отчетов Power BI" и службы Power BI.
keywords: ''
author: maggiesMSFT
ms.author: maggies
ms.date: 05/07/2018
ms.topic: overview
ms.service: powerbi
ms.component: powerbi-report-server
manager: kfile
ms.custom: mvc
ms.openlocfilehash: f78638097ea33f9954f3db78c117f1935a68530b
ms.sourcegitcommit: 52ac456bf2ac025b22ea634c28482f22e1cc19ac
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2018
ms.locfileid: "48908538"
---
# <a name="comparing-power-bi-report-server-and-the-power-bi-service"></a>Сравнение решения "Сервер отчетов Power BI" и службы Power BI

Решение "Сервер отчетов Power BI" и служба Power BI имеют много похожих характеристик, но и ряд важных различий. В следующей таблице перечислены и те, и другие.

| Функции | Power BI Report Server | Служба Power BI | Примечания
|---------|---------|---------|---------|
| Развертывание | Локально или в размещенном облаке | В облаке | Решение "Сервер отчетов Power BI" можно развернуть на виртуальных машинах Azure (размещенное облако), если используется лицензия Power BI Premium
| Исходные данные | Облачные и (или) локальные | Облачные и (или) локальные |  
| Лицензия | Power BI Premium или SQL Server ЕЕ с правами системного администратора | Power BI Pro и (или) Power BI Premium |  
| Жизненный цикл | Современная политика жизненного цикла | Полностью управляемая служба |  
| Цикл выпуска | Каждые 4 месяца | Один раз в месяц | Новейшие функции и исправления сначала появляются в службе Power BI. Основные обновления функций попадают в решение "Сервер отчетов Power BI" в ближайшие несколько выпусков, но некоторые обновления предназначены только для службы Power BI.
| Создание отчетов Power BI в Power BI Desktop | Да | Да |  
| Создание отчетов Power BI в браузере | Нет | Да |  
| Требуется шлюз | Нет | Да для локальных источников данных |  
| Потоковая передача в реальном времени | Нет | Да | [Потоковая передача в реальном времени в Power BI](../service-real-time-streaming.md)
| Панели мониторинга | Нет | Да | [Панели мониторинга в службе Power BI](../consumer/end-user-dashboards.md) 
| Распределение групп отчетов с помощью приложений | Нет | Да | [Создание и публикация приложений с панелями мониторинга и отчетами](../service-create-distribute-apps.md) 
| Пакеты содержимого | Нет | Да | [Знакомство с пакетами содержимого организации](../service-organizational-content-pack-introduction.md) 
| Подключение к службам, таким как Salesforce | Нет | Да | [Подключение к используемым службам](../consumer/end-user-connect-to-services.md) с помощью службы Power BI
| Вопросы и ответы | Нет | Да | ["Вопросы и ответы" в службе Power BI и Power BI Desktop](../consumer/end-user-q-and-a.md) 
| Краткая аналитика | Нет | Да | [Автоматическое создание аналитических сведений с помощью Power BI](../consumer/end-user-insights.md) 
| Анализ в Excel | Нет | Да | [Анализ в Excel](../service-analyze-in-excel.md) 
| Отчеты с разбивкой на страницы | Да | Нет | Отчеты с разбивкой на страницы не будут доступны в службе Power BI, но вы можете [прикрепить элементы этих отчетов к панелям мониторинга Power BI](https://docs.microsoft.com/sql/reporting-services/pin-reporting-services-items-to-power-bi-dashboards).
| Мобильные приложения Power BI | Да | Да | [Обзор мобильных приложений Power BI](../consumer/mobile/mobile-apps-for-mobile-devices.md) 
| Карты ArcGIS | Нет | Да | [Карты ArcGIS от ESRI в службе Power BI и Power BI Desktop](../power-bi-visualization-arcgis.md)
| Подписки по электронной почте на отчеты Power BI | Нет | Да | [Подписка на отчеты или панели мониторинга](../consumer/end-user-subscribe.md) в службе Power BI 
| Подписки по электронной почте на отчеты с разбивкой на страницы | Да | Нет | [Доставка электронной почты в Reporting Services](https://docs.microsoft.com/sql/reporting-services/subscriptions/e-mail-delivery-in-reporting-services)  
| Оповещения о данных | Нет | Да | [Оповещения о данных](../service-set-data-alerts.md) в службе Power BI
| Безопасность на уровне строк | Только через источник данных в режиме DirectQuery | Доступно в режимах DirectQuery (источник данных) и импорта | [Безопасность на уровне строк (RLS)](../service-admin-rls.md) в Power BI 
| Полноэкранный режим | Нет | Да | [Полноэкранный режим](../service-fullscreen-mode.md) в службе Power BI 
| Расширенные возможности совместной работы Office 365 | Нет | Да | [Совместная работа в рабочей области приложений](../service-collaborate-power-bi-workspace.md) с Office 365 
| визуальные элементы R; | Нет | Да | [Создание визуальных элементов R](../visuals/service-r-visuals.md) в службе Power BI  
| Функции предварительной версии | Нет | Да | [Включение предварительных версий функций Power BI](../consumer/end-user-preview-features.md) 
| Настраиваемые визуальные элементы | Да | Да | [Пользовательские визуальные элементы в Power BI](../power-bi-custom-visuals.md) 
| Power BI Desktop | Версия, оптимизированная для сервера отчетов, доступна для скачивания вместе с сервером отчетов | Версия, оптимизированная для службы Power BI, доступна в Windows Store | [Power BI Desktop для сервера отчетов](https://powerbi.microsoft.com/report-server/) <br><br> [Power BI Desktop для службы Power BI](http://aka.ms/pbidesktopstore)

## <a name="next-steps"></a>Дальнейшие действия
[Установка сервера отчетов Power BI](install-report-server.md)  



