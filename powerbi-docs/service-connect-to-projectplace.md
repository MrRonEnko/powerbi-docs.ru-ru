---
title: Подключение к Projectplace с помощью Power BI
description: Projectplace для Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: fa5e0e35a3cb5fe7375032f15653b1c45bedf980
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2018
ms.locfileid: "46544217"
---
# <a name="connect-to-projectplace-by-planview-with-power-bi"></a>Подключение к Projectplace от Planview с помощью Power BI
С помощью пакета содержимого Projectplace by Planview вы можете визуализировать данные о совместной работе над проектом совершенно новыми способами непосредственно в Power BI. Используйте учетные данные для входа Projectplace, чтобы интерактивно просмотреть ключевую статистику по проектам, узнать, кто в группе является наиболее активным и продуктивным, а также определить рискованные области и действия в проектах в вашей учетной записи Projectplace. Также можно расширить готовую информационную панель и отчеты, чтобы получить именно те ценные сведения, которые необходимы вам.

[Подключение к пакету содержимого Projectplace в Power BI](https://app.powerbi.com/getdata/services/projectplace)

>[!NOTE]
>Чтобы импортировать данные Projectplace в Power BI, необходимо быть пользователем Projectplace. Дополнительные требования см. в разделе ниже.

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.
   
    ![](media/service-connect-to-projectplace/get.png)
2. В поле **Службы** выберите **Получить**.
   
    ![](media/service-connect-to-projectplace/services.png)
3. На странице Power BI выберите **Projectplace by Planview** и затем **Получить**:  
   
    ![](media/service-connect-to-projectplace/projectplace.png)
4. В текстовом поле OData Feed URL (URL-адрес веб-канала OData) введите URL-адрес веб-канала OData Projectplace, который вы хотите использовать, как показано на следующем рисунке:
   
    ![](media/service-connect-to-projectplace/params.png)
5. В списке "Метод проверки подлинности" выберите **OAuth** , если это значение еще не установлено. Щелкните **Вход** и следуйте процедуре входа в систему.  
   
   ![](media/service-connect-to-projectplace/creds.png)
6. На левой панели выберите **Projectplace** в списке информационных панелей. Power BI импортирует данные Projectplace в информационную панель. Обратите внимание, что загрузка данных может занять некоторое время.  
   
    Информационная панель содержит плитки, которые отображают данные из базы данных Projectplace. Ниже приведен пример информационной панели Projectplace по умолчанию в Power BI.
   
    ![](media/service-connect-to-projectplace/dashboard.png)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](consumer/end-user-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](consumer/end-user-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**

## <a name="system-requirements"></a>Требования к системе
Чтобы импортировать данные Projectplace в Power BI, необходимо быть пользователем Projectplace. Эта процедура предполагает, что вы уже выполнили вход на домашнюю страницу Microsoft Power BI с помощью учетной записи Power BI. Если у вас нет учетной записи Power BI, перейдите на сайт [powerbi.com](https://powerbi.microsoft.com/get-started/) и в разделе **Power BI — совместная работа и общий доступ в облаке** нажмите кнопку **Попробовать бесплатно**. Затем нажмите кнопку **Получить данные**.

## <a name="next-steps"></a>Дальнейшие действия
[Что такое Power BI?](power-bi-overview.md)

[Power BI — основные понятия](consumer/end-user-basic-concepts.md)

