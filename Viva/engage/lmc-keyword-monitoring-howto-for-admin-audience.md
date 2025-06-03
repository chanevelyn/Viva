---
title: "Advanced moderation: Keyword monitoring for Viva Engage admins"
description: "Conversation monitoring through keyword definitions"
ms.reviewer: shreyanarla
ms.author: donnabouldin
author: v-rgrace
manager: donnabouldin
ms.date: 06/01/2025
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

# Advanced moderation: keyword monitoring for Viva Engage admins

In the Communications Dashboard, the **Advanced moderation** page provides a central experience for configuring and monitoring specific keywords and phrases detected across your Engage network.

## Who Can Use This Feature

This feature is available to all Microsoft 365 customers. The following admin roles can define filters, monitored conversations, and act on them:  

- Verified Admins
- Network Admins
- Viva Engage Admins
- Corporate Communicator (requires advanced moderation granular permissions)

After you define custom keywords for the network, all conversations in Storylines and Communities that match your keywords appear on the Communications dashboard.

## Use keyword monitoring

Admins with appropriate permissions can go to the Communications dashboard and open the **Advanced moderation** page to do the following tasks:

- Add and manage keyword lists
- Use regular expressions to craft more sophisticated keyword/phrase monitoring
- Specify email recipients for keyword alert notifications
- View a centralized table of all conversations flagged with keyword matches
- Act on matching conversations – mute, close, delete, or dismiss from review

Using filter controls, you can review moderated conversations on the **Detected conversations** table. Muted and dismissed conversations appear for 30 days with timestamps and actor information.

### Apply regular expressions for keyword monitoring

You can use regular expressions for pattern matching. A regular expression is a character string of code that defines a matching _pattern_ in text. String-searching algorithms like Advanced moderation use these patterns to find matches in independently posted inputs such as Viva Engage storyline posts and comments. The following table lists examples:

| Purpose | RegEx Pattern or phrase | Matching values examples |
| ------- | ------------------| ----------------------- |
| Word boundary | `\b`word`\b`    | `\b`theme`\b` matches the word "theme" <br> but doesn't match "themes" or "them." <br>Substitute any word or phrase for your match in any filter. |
| Credit card | `\b(?:\d[ ‐]*?){13,16}\b` | 1234 5678 90123<br>1234 5678 9012 3456 |
| Social Security numbers | `\b\d{3}[ -]\d{2}[ -]\d{4}\b` | 123 45 6789<br>123‐45‐6789 |
| Monitor group creation | `"just created"` | Matthew just created the Eastern Region Sales group for us. |

### Content of email notifications for keyword alerts

When a post in Viva Engage matches a monitored keyword, the moderation system sends an email notification to the specified address. The notifications help admins and moderators stay informed and take timely action on potentially sensitive or relevant content. Notifications include the following content:

**Subject Line**: provides quick context, including the matched keyword and the type of conversation (community or storyline) where it was detected.

**Email Body**: content varies depending on the visibility and type of the conversation.

- **Public community or Storyline posts**: email notifications include the full conversation and all associated replies. For context, the alert also lists the name of the community or storyline.

- **Private community posts**: email notifications include a direct link to the conversation and to the private community where the match is detected. Community members can select the link to view the matching conversation.

### Security and compliance safeguards

To enhance security and compliance, Viva Engage inherits a set of safeguards from Microsoft Entra. Tenant emails observe the following restrictions:

- Entra ID–backed email addresses from within your Microsoft 365 tenant are supported as keyword alert recipients.
- Consumer email addresses (Gmail, Yahoo, Outlook.com) aren't supported.
- If an unsupported email is entered, Viva Engage prompts the user to provide a valid tenant-based address.

Exclusion of Private Messages employs the following safeguards:

- Keyword detection doesn't apply to private messages between individuals.
- These messages are confidential and must be accessed through approved compliance tools such as eDiscovery and Microsoft Purview when needed.
