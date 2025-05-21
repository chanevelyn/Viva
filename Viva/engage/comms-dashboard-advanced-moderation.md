---
title: "Enable advanced moderation from the admin center"
description: "Describes the straightforward process for enabling and verifying the Engage AI Summarization service."
ms.reviewer: shreyanarla
ms.author: donnabouldin
author: v-rgrace
manager: donnabouldin
ms.date: 05/21/2025
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Theme moderation in Viva Engage

Verified admins, network admins, and corporate communicators with Advanced Moderation permissions can set custom themes to moderate and monitor conversations across the Viva Engage network. Theme moderation automatically mutes and reports conversations related to admin and communicator themes of interest. You can also quickly check for matches against any theme.

Theme moderation is built upon the [Viva Engage **AI Summarization** service](https://learn.microsoft.com/viva/engage/engage-ai-summarization). This feature gives Viva Engage users and admins access to Large Language Model (LLM) technology with [Microsoft Responsible AI protections](https://www.microsoft.com/ai/responsible-ai).

>[!NOTE]
>Theme moderation requires at least 50% of users in your organization to have the Viva Suite license, or the Viva Employee Communications and Communities license. The Microsoft 365 enterprise plan includes keyword monitoring, detected conversations, and the advanced moderation feature set.

:::image type="content" source="../media/engage/admin/lmc-adv-moderation-themes-design.png" alt-text="Define themes under the Advanced moderation tab":::

## Set up theme moderation

Check your Viva Engage Admin Center settings to ensure that the **AI Summarization** setting reflects your network preferences. You can find the controls for this setting through Viva Feature Access Management. It controls all AI data processing for your network. By default, AI summarization is enabled and processes data across all users in your network unless you specify otherwise.

:::image type="content" source="../media/engage/admin/ladmin-center-ai-summarization-settings.png" alt-text="AI summarization in Admin Center":::

Network admins and corporate communicators can use theme moderation to track conversations related to their themes. Viva Engage supports concurrent use of up to 30 themes at a time. The feature is available in the Advanced Moderation page of the Communications dashboard.

When you add new themes, ongoing conversations that match themes start to populate the **Advanced moderation > Detected conversations** table.

>[!NOTE]
>Retroactive detection doesn't take place for existing conversations that match newly added themes.

## See also

For an overview of frequently asked questions related to the underlying AI system powering this feature, see [Upcoming AI Summarization and theme extraction FAQ article](link here)

For more information about how AI works in Viva Engage, see [Data, Privacy, and Security for Microsoft 365 Copilot in Viva Engage](https://learn.microsoft.com/viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage)

For a more detailed walkthrough of Advanced moderation and its use of themes, see the [Communications dashboard: Advanced moderation](https://support.microsoft.com/topic/13f58cf0-b8e5-40ab-bc55-34d69f762c1d?preview=true) article.
