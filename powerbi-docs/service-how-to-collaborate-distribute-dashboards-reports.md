---
title: Как совместно работать и предоставлять общий доступ в Power BI?
description: В Power BI реализовано несколько способов организации совместной работы над панелями мониторинга, отчетами, плитками и приложениями, а также предоставления к ним общего доступа. Каждый имеет свои преимущества.
author: maggiesMSFT
manager: kfile
ms.reviewer: lukaszp
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/02/2018
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: bcec05211d3748e992f0e0cf68acd6460b2715d4
ms.sourcegitcommit: 52ac456bf2ac025b22ea634c28482f22e1cc19ac
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2018
ms.locfileid: "48908976"
---
# <a name="how-should-i-collaborate-and-share-in-power-bi"></a>Как совместно работать и предоставлять общий доступ в Power BI?

Вы создали панели мониторинга и отчеты. Их также можно создавать совместно с сотрудниками. Затем возникает необходимость предоставить к ним доступ другим пользователям. Какой же лучший способ распространить их?

В этой статье мы сравним варианты совместной работы и предоставления общего доступа в Power BI: 

* Совместная работа с сотрудниками для создания полноценных отчетов и информационных панелей в *рабочих областях приложений*.
* Объединение готовых панелей мониторинга и отчетов в *приложения* и их публикация для большой группы пользователей или всей организации.
* Предоставление нескольким пользователям общего доступа к панелям мониторинга или отчетам из службы или мобильных приложений Power BI.
- Печать отчетов.
* Публикация в Интернете на общедоступных веб-сайтах, где его могут видеть и использовать люди по всему миру.

Вы можете выбрать любой из вариантов совместного использования панели мониторинга. В любом случае вам нужна лицензия [Power BI Pro](service-features-license-type.md) либо же содержимое должно находиться в [емкости Premium](service-premium.md). В зависимости от выбранного варианта требования к лицензии могут быть разными для коллег, просматривающих ваши информационные панели. В следующих разделах представлен подробный обзор возможностей. 

![Приложения в службе Power BI](media/service-how-to-collaborate-distribute-dashboards-reports/power-bi-apps-home-blog.png)

*Приложения в службе Power BI*

## <a name="collaborate-with-coworkers-in-an-app-workspace"></a>Совместная работа с коллегами в рабочей области приложения

Если команды работают вместе, им нужен доступ к одним и тем же документам для удобной совместной работы. Рабочие области приложений в Power BI предоставляют место, где команды совместно управляют нужными панелями мониторинга, отчетами, наборами данных и книгами. Иногда пользователи Power BI упорядочивают рабочие области в зависимости от структуры организации, а иногда создают их для конкретных проектов. Иногда в организациях используется несколько рабочих областей для хранения разных версий отчетов и панелей мониторинга. 

Рабочие области приложений предоставляют роли, которые определяют, какие разрешения есть у ваших коллег. С помощью этих ролей можно определить, кто может управлять всей рабочей областью или просто предоставлять для нее содержимое.

![Рабочие области приложений](media/service-how-to-collaborate-distribute-dashboards-reports/power-bi-apps-workspaces.png)

Некоторые пользователи помещают содержимое в раздел "Моя рабочая область" и предоставляют к нему общий доступ. Рабочие области приложений лучше подходят для совместной работы, чем раздел "Моя рабочая область", поскольку у содержимого может быть несколько владельцев. Все члены вашей команды могут вносить изменения и предоставлять доступ другим. Раздел "Моя рабочая область" подходит для размещения одноразового или личного содержимого отдельными пользователями.

Предположим, у вас есть готовая панель мониторинга и вы хотите предоставить коллегам общий доступ к ней. Как лучше всего предоставить доступ к панели мониторинга? Ответ зависит от ряда факторов. Если определенный сотрудник должен быть владельцем панели мониторинга и отвечать за ее обновление, или ему нужен доступ ко всему содержимому в рабочей области приложения, лучше всего добавить его в рабочую область. Если вашему коллеге нужна только эта панель мониторинга, а не все содержимое рабочей области, у вас снова есть несколько вариантов. Если панель мониторинга является частью большого набора содержимого, доступ к которому нужен многим сотрудникам, лучше всего опубликовать приложение. Но если вашему коллеге нужна только одна определенная панель мониторинга, можно просто предоставить к ней общий доступ. 

Узнайте больше о создании [рабочих областей приложений](service-create-workspaces.md).

**Знаете ли вы?** В Power BI доступна предварительная версия нового интерфейса рабочей области. Ознакомьтесь со статьей [Создание новых рабочих областей (предварительная версия)](service-create-the-new-workspaces.md) и узнайте, как рабочие области изменятся в будущем. 

## <a name="distribute-data-and-insights-by-creating-an-app"></a>Распространение данных и сведений путем создания приложения

Предположим, что вам необходимо распространить свою панель мониторинга для широкой аудитории. Вы и ваши сотрудники создали *рабочую область приложения*, затем создали и настроили в ней информационные панели, отчеты и наборы данных. Теперь выберите нужные панели мониторинга и отчеты и опубликуйте их как приложение для группы или для всей организации. 

![Значок "Публикация приложения"](media/service-how-to-collaborate-distribute-dashboards-reports/power-bi-app-publish-600.png)

Служба Power BI ([https://powerbi.com](https://powerbi.com)) позволяет легко находить и устанавливать приложения. Вы можете отправить бизнес-пользователям прямую ссылку на приложение, или они могут найти его в AppSource. С разрешения администратора Power BI его можно установить автоматически в учетных записях Power BI коллег. Дополнительные сведения о [публикации приложений](service-create-distribute-apps.md). 

После установки приложения они смогут просматривать его в браузере или на мобильном устройстве.

Для просмотра приложения пользователям требуется лицензия Power BI Pro, либо приложение должно быть сохранено в емкости Power BI Premium. Дополнительные сведения см. в статье [Что такое Power BI Premium?](service-premium.md)

Вы также можете публиковать приложения для пользователей за пределами организации. Они могут просматривать панель мониторинга и взаимодействовать с содержимым приложения, но не могут предоставлять к ней общий доступ.

## <a name="share-dashboards-and-reports"></a>Совместное использование информационных панелей и отчетов
Предположим, вы завершили работу над панелью мониторинга и отчетом в своей рабочей области или рабочей области приложения, и хотите, чтобы у других пользователей был к ним доступ. Чтобы реализовать это, *предоставьте к ней общий доступ* пользователям. 

![Значок "Предоставить общий доступ"](media/service-how-to-collaborate-distribute-dashboards-reports/power-bi-share-in-situ.png)

Вы можете предоставить общий доступ к вашему содержимому. Для этого у вас и соответствующих пользователей должна быть лицензия Power BI Pro либо же содержимое должно находиться в рабочей области в [емкости Premium](service-premium.md). При совместном использовании панели мониторинга или отчета получатели могут просматривать их и взаимодействовать с ними, но не могут их изменять. Они видят на панелях мониторинга и в отчетах те же данные, что и вы, при условии, что к базовому набору данных не применяется защита на уровне строк (RLS). Коллеги, которым вы предоставляете общий доступ, тоже могут, с вашего разрешения, предоставлять доступ своим коллегам. 

Вы можете также предоставлять общий доступ пользователям за пределами своей организации. Они тоже могут просматривать панель мониторинга и отчет и взаимодействовать с ними, но не могут предоставлять к ним общий доступ. 

См. дополнительные сведения о [предоставлении общего доступа к панелям мониторинга и отчетам](service-share-dashboards.md) из службы Power BI. Можно также добавить фильтр в ссылку и [предоставить общий доступ к отфильтрованному представлению отчета](service-share-reports.md).

## <a name="annotate-and-share-from-the-power-bi-mobile-apps"></a>Добавление заметок и предоставление общего доступа из мобильных приложений Power BI
В мобильных приложениях Power BI для устройств iOS и Android вы можете добавлять заметки к плиткам, отчетам или визуальным элементам, а затем предоставлять к ним доступ другим пользователям по электронной почте. 

![Добавление заметок и предоставление доступа в мобильных приложениях](media/service-how-to-collaborate-distribute-dashboards-reports/power-bi-iphone-annotate.png)

Когда вы предоставляете доступ к моментальному снимку, плитке, отчету или визуальному элементу, получатели видят эти элементы такими же, какими они были отправлены в сообщении электронной почты. Сообщение также содержит ссылку на панель мониторинга или отчет. Если у получателей есть лицензия Power BI Pro либо же содержимое находится в [емкости Premium](service-premium.md), а вы уже предоставили им общий доступ к объекту, они смогут его открыть. Моментальные снимки плиток можно отправлять кому угодно, не только сотрудникам в том же домене электронной почты, что и вы.

См. дополнительные сведения в статье [Добавление заметок и совместное использование плиток, отчетов или визуальных элементов в мобильных приложениях iOS](consumer/mobile/mobile-annotate-and-share-a-tile-from-the-mobile-apps.md).

Вы также можете [предоставить общий доступ к моментальному снимку плитки](consumer/mobile/mobile-windows-10-phone-app-get-started.md) из приложения Power BI для устройств Windows 10.

## <a name="print-or-save-as-pdf-or-other-static-file"></a>Печать или сохранение в формате PDF или в другом формате статических файлов
Вы также можете распечатать или сохранить в формате PDF (или в другом формате статических файлов) всю панель мониторинга, плитку панели мониторинга, страницу отчета или визуализацию отчета в службе Power BI. Отчеты можно распечатывать только постранично, весь отчет сразу распечатать нельзя. Ознакомьтесь с дополнительными сведениями о [печати или сохранении в качестве статического файла](consumer/end-user-print.md).

## <a name="publish-to-the-web"></a>Публикация в Интернете

> [!WARNING]
> Используйте функцию **Публикации в Интернете** только для того, чтобы сделать содержимое общедоступным, а не для предоставления общего доступа внутри организации.

Вы можете публиковать отчеты Power BI в Интернете, внедряя интерактивные визуализации в записи блога, веб-сайты, социальные сети и другие средства коммуникации в сети на любом устройстве. Любой пользователь в Интернете может просматривать ваши отчеты; вы не можете выбирать, кто может просматривать уже опубликованный отчет. Пользователям не нужна лицензия Power BI. Функция публикации в Интернете доступна только для отчетов с возможностью редактирования. Отчеты, к которым вам предоставили доступ или которые находятся в приложении, публиковать нельзя. Дополнительные сведения о [публикации в Интернете](service-publish-to-web.md).

## <a name="next-steps"></a>Дальнейшие действия
* [Предоставление общего доступа к информационным панелям коллегам и другим пользователям](service-share-dashboards.md)
* [Создание и публикация приложений с информационными панелями и отчетами в Power BI](service-create-distribute-apps.md)
* Хотите оставить отзыв? Поделитесь своими предложениями на [веб-сайте сообщества Power BI](https://community.powerbi.com/).
* Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI](http://community.powerbi.com/).

