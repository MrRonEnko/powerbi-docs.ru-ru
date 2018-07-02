---
title: Удаленная настройка доступа мобильных приложений Power BI для iOS к серверу отчетов
description: Узнайте, как удаленно настроить доступ мобильных приложений для iOS к серверу отчетов.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-report-server
ms.topic: conceptual
ms.date: 05/22/2018
ms.author: maggies
ms.openlocfilehash: bbade67c9510b8d316364d991c09444712309514
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2018
ms.locfileid: "34722185"
---
# <a name="configure-power-bi-ios-mobile-app-access-to-a-report-server-remotely"></a>Удаленная настройка доступа мобильных приложений Power BI для iOS к серверу отчетов

В этой статье вы узнаете, как настроить доступ мобильных приложений Power BI для iOS к серверу отчетов с помощью средства MDM организации. Для этого ИТ-администратор создает политику настройки приложения с требуемыми сведениями, которые должны быть переданы в приложение. 

 После этого пользователям мобильного приложения Power BI для iOS будет проще подключаться к серверу отчетов организации, так как подключение к нему уже настроено. 


## <a name="create-the-app-configuration-policy-in-mdm-tool"></a>Создание политики настройки приложения в средстве MDM 

Чтобы создать политику настройки приложения, администратору необходимо выполнить в Microsoft Intune указанные ниже действия. В других средствах MDM процедура, необходимая для создания политики настройки приложения, может быть иной. 

1. Подключите средство MDM. 
2. Создайте политику настройки приложения и присвойте ей имя. 
3. Выберите пользователей, к которым будет применена эта политика. 
4. Создайте пары "ключ — значение". 

Эти пары представлены в таблице ниже.

|Ключ  |Тип  |Описание  |
|---------|---------|---------|
| com.microsoft.powerbi.mobile.ServerURL | String | URL-адрес сервера отчетов </br> Должен начинаться с префикса http или https |
| com.microsoft.powerbi.mobile.ServerUsername | String | [необязательно] </br> Имя пользователя для подключения к серверу. </br> Если оно отсутствует, в приложении будет выведен запрос на ввод имени пользователя.| 
| com.microsoft.powerbi.mobile.ServerDisplayName | String | [необязательно] </br> Значение по умолчанию — "Сервер отчетов" </br> Понятное имя, представляющее сервер в приложении | 
| com.microsoft.powerbi.mobile.OverrideServerDetails | Boolean | Значение по умолчанию — True </br> Если задано значение True, имеющееся на мобильном устройстве определение сервера отчетов переопределяется (уже настроенные серверы будут удалены). </br> Кроме того, пользователь не может удалить данную конфигурацию. </br> Если задано значение False, передаваемые значения добавляются, но существующие параметры сохраняются. </br> Если в мобильном приложении уже настроен данный URL-адрес сервера, его конфигурация сохраняется и пользователю не предлагается повторно пройти проверку подлинности для этого сервера. |

Ниже приведен пример настройки политики конфигурации с помощью Intune.

![Параметры конфигурации Intune](media/configure-powerbi-mobile-apps-remote/power-bi-ios-remote-configuration-settings.png)

## <a name="end-users-connecting-to-a-report-server"></a>Подключение конечных пользователей к серверу отчетов

После публикации политики настройки приложения пользователи и устройства, включенные в список рассылки, определенный для этой политики, проходят через описанную ниже процедуру при запуске мобильного приложения Power BI для iOS. 

1. Появляется сообщение о том, что для мобильного приложения настроен доступ к серверу отчетов. Пользователю необходимо коснуться элемента **Вход**.

    ![Вход на сервер отчетов](media/configure-powerbi-mobile-apps-remote/power-bi-config-server-sign-in.png)

2.  На странице **Подключение к серверу** сведения о сервере отчетов уже заполнены. Необходимо коснуться элемента **Подключиться**.

    ![Заполненные сведения о сервере отчетов](media/configure-powerbi-mobile-apps-remote/power-bi-ios-remote-configure-connect-server.png)

3. Необходимо ввести пароль, чтобы пройти проверку подлинности, а затем коснуться элемента **Вход**. 

    ![Заполненные сведения о сервере отчетов](media/configure-powerbi-mobile-apps-remote/power-bi-config-server-address.png)

Теперь пользователи могут просматривать ключевые показатели эффективности и отчеты Power BI, хранящиеся на сервере отчетов, и взаимодействовать с ними.

## <a name="next-steps"></a>Дальнейшие действия
[Обзор функций администратора](admin-handbook-overview.md)  
[Установка сервера отчетов Power BI](install-report-server.md)  

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](https://community.powerbi.com/)
