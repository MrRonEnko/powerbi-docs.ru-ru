---
title: Доступ и копирование пакетов содержимого организации
description: Узнайте о создании копий пакетов содержимого организации и устранении неполадок в них в Power BI
author: maggiesMSFT
manager: kfile
ms.reviewer: lukaszp
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/02/2018
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: 37cfca811b7e60bde832396e67b246933d4e0a8e
ms.sourcegitcommit: 52ac456bf2ac025b22ea634c28482f22e1cc19ac
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2018
ms.locfileid: "48908424"
---
# <a name="organizational-content-packs-copy-refresh-and-get-access"></a>Пакеты содержимого организации: копирование, обновление и получение доступа

После публикации пакета содержимого организации все получатели видят одну и ту же панель мониторинга, одни и те же отчеты, книги Excel и наборы данных (если источником данных не являются службы SQL Server Analysis Services (SSAS).  [Только автор пакета содержимого может изменять и повторно публиковать](service-organizational-content-pack-manage-update-delete.md) его.  Тем не менее все получатели могут сохранить копию пакета содержимого, которая может сосуществовать с исходным вариантом.

Создание пакетов содержимого отличается от предоставления общего доступа к информационным панелям и от совместной работы над ними в группе. Чтобы выбрать оптимальный вариант для вашей ситуации, см. статью [Как предоставить общий доступ к панелям мониторинга, отчетам и плиткам?](service-how-to-collaborate-distribute-dashboards-reports.md)

> [!NOTE]
> Нельзя создавать или устанавливать пакеты содержимого организации в предварительной версии нового интерфейса рабочей области. Сейчас самое время обновить пакеты содержимого для приложений, если вы еще этого не сделали. Узнайте [больше о новом интерфейсе рабочей области](service-create-the-new-workspaces.md).
> 

## <a name="create-a-copy-of-an-organizational-content-pack"></a>Создание копии пакета содержимого организации
Создайте собственную копию пакета содержимого, не отображающуюся для других пользователей.

1. Нажмите кнопку с многоточием (...) возле информационной панели и выберите команду "Создать копию".
   
    ![](media/service-organizational-content-pack-copy-refresh-access/power-bi-create-copy-organizational-content-pack.png)
2. Нажмите кнопку **Сохранить**.  

Теперь у вас есть копия, которую можно изменять. Никто другой не увидит ваши изменения.

## <a name="help--i-can-no-longer-access-the-content-pack"></a>Помогите!  Мне больше не доступен пакет контента
Это может произойти по следующим причинам.

* **Изменение членства**: пакеты содержимого публикуются в группах рассылки электронной почты, группах безопасности и [группах Power BI, основанных на Office 365](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9).  Если вы были удалены из группы, вы потеряете доступ к пакету содержимого.
* **Изменения сферы распространения**: автор пакета содержимого меняет сферу распространения. Например, если пакет содержимого первоначально был опубликован для всей организации, но автор повторно опубликовал его для меньшей аудитории, вы можете потерять право на использование пакета.
* **Изменения параметров безопасности**: если информационная панель и отчеты подключаются к локальным источникам данных SSAS и в параметры безопасности внесены изменения, ваши разрешения на этом сервере могут быть отозваны.

## <a name="how-are-organizational-content-packs-refreshed"></a>Как обновляются пакеты контента организации?
Когда пакет контента создается, параметры обновления наследуются от набора данных.  Когда вы создаете копию пакета содержимого, новая версия сохраняет ссылку на исходный набор данных и соответствующее расписание обновления. 

См. статью [Управление пакетами содержимого организации, их обновление и удаление](service-organizational-content-pack-manage-update-delete.md).

## <a name="next-steps"></a>Дальнейшие действия
* [Знакомство с пакетами содержимого организации](service-organizational-content-pack-introduction.md)
* [Создание группы в Power BI](service-create-distribute-apps.md)
* Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)

