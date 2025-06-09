---
ms.date: 06/05/2025
title: "Report a Viva Engage conversation"
description: "Configure conversation reporting in Viva Engage to enable people to report conversation starter posts and comments that don't follow guidelines or policies."
ms.reviewer: spencerperry
ms.author: mamiejohnson
author: v-rgrace
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-engage
ms.localizationpriority: medium
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Report a Viva Engage conversation

Viva Engage admins can empower network users to report conversations and comments that don't follow organizational guidelines or policies. To set it up, enable the **Report conversations** option in the Viva Engage admin center.

Admin center configuration options vary based on licensing that includes Microsoft Purview Communication Compliance:

- **Licenses that don't include communication compliance**. When you enable communication compliance, the Viva Engage admin must define a Microsoft Entra-backed email address to receive reported conversations. As described in this article, the admin can also enter pre-submission instructions and post-submission confirmations for the user.

- **Licenses that do include communication compliance**. When you enable communication compliance, reported conversations automatically route through communication compliance for investigation and remediation. [Learn more about routing reported conversations through Microsoft Purview Communication Compliance](/purview/communication-compliance-policies).

## Enable conversation reporting without a communication compliance license

1. Go to the Viva Engage admin center.

2. In the **Setup & Configuration** tab, select **Tenant settings**.

3. In the Tenant settings page, under **Conversation settings**, select **Edit**.

4. In the Conversation settings page, enable the **Report conversations** toggle.

5. After you enable conversations, configure the following settings:

    - **Email** - Enter an organization email address to receive reports. The email address must be backed by Microsoft Entra ID.

    - **Introductory message** – Enter messaging that explains the reporting process to users when they select **Report a Conversation**.  

    For example, explain who receives the report, and the next steps. If you can, provide a link to the company's network usage guidelines. This field is limited to 1,500 characters.

6. Optionally, use the **Confirmation message** setting to explain to your employees what happens after they submit a report. Set expectations for when the submitter can expect a response and describe next steps for the organization. This field is limited to 1,500 characters.  

    :::image type="content" source="../media/engage/admin/admin-center-report-conversation-settings.png" alt-text="Screenshot shows the reporting admin panel.":::

### End user experience

When you enable this feature, Viva Engage users see the **Report Conversation** option on conversation starters, and **Report Comment** on comments and replies.

:::image type="content" source="../media/viva-engage-conversations-report-dropdown.png" alt-text="Screenshot showing user reporting for conversation starter.":::

#### Report Conversation option on conversation starter

:::image type="content" source="../media/viva-engage-conversations-report-comment-dropdown.png" alt-text="Screenshot showing user reporting for comment.":::

#### Report Conversation option on conversation comment

Users can find a right-panel pop-out with a custom message from the Viva Engage admin and a required **Reason for Reporting** box.

:::image type="content" source="../media/viva-engage-conversations-report-comment.png" alt-text="Screenshot showing reason for reporting box.":::

The email address in **Report Conversations** settings receives the reported conversation or comment, the reporting user, and the reason for reporting.

After successful submission, the user sees the admin's custom message, if any. They also receive a confirmation message that includes their report, and a link to the reported content.

:::image type="content" source="../media/viva-engage-conversations-report-submitted-panel-closeup.png" alt-text="screenshot showing success reporting submission.":::

### Email reports

After a report submission, the organization email address receives an email. It includes the following information:

- The name of the person who submitted the report.
- The title and text of the email indicates whether a conversation starter or comment is being reported.
- The name of the person who started the conversation or wrote the reported comment.
- The community in which the reported conversation or comment was made.
- The date and time at which the reported conversation or comment was made.
- A link to the specific conversation starter.
- Any comments entered by the reporting user.

> [!NOTE]
> Viva Engage doesn't support deep links to comments. Report emails always show the conversation starter link for both conversation starters and comments. Reports don't contain deep links to a reported comment. Report reviewers can use the conversation starter link together with the reported comment timestamp to find the actual reported comment in the conversation.

The Viva Engage user who submitted the report also receives a copy of this email.

## FAQ

### I’m a Viva Engage admin. How do I know if my network is eligible for reporting conversations and comments?

The Report conversations feature is available to all tenants.

### Can I add multiple email addresses to receive the reports?

You can define only one email. Use a group email or distribution list alias if you want the reports to go to multiple people. Reports must go to an organizational email address backed by Entra ID.

### Is this functionality on by default?

Viva Engage disables this feature by default. A Viva Engage admin must turn on the Report conversations feature for users so they can see the option to report conversations and comments.

### Can users report conversations from external networks?

Report conversations functionality is only available in the Viva Engage home network. Conversations in external networks can't be reported.

### Can users report private Viva Engage messages?

Users can't report private messages.

### Can users report messages from private communities?

Users can report conversations from all public and private communities in Viva Engage. The email report includes a link to the original conversation starter where the starter or comment was reported. If the person reviewing the reports doesn't have access to the private community, they can work with the Engage admin to get access to that community for further review. Admins can also work with the community administrator to get access to the reported message.

### Can users report messages from Viva Engage integrations with Teams, Outlook, and SharePoint?

Users can report conversations from the Viva Engage app in Teams.

### How do I route reported conversations through Microsoft Purview Communication Compliance instead of using a single email address to report conversations?

If you have a license that includes communication compliance, [learn how to take advantage of review and remediation capabilities of Microsoft Purview Communication Compliance](/purview/communication-compliance-policies).
