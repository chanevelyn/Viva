---
title: "AI summarization and advanced moderation FAQ"
description: "Information to address customer questions about AI summarization and Advanced moderation."
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

# AI Summarization and theme extraction FAQ

## What is AI summarization and theme extraction?  

AI summarization and theme extraction are Viva Engage features for network admins, corporate communicators, and community managers to understand the impact and trends of Viva Engage content across spaces you manage. For advanced analytics, AI summarization uses LLMs (large language models) to analyze the messages and interactions across a network, audience, community, or conversation, and give an overview of engagement trends across those entities.

Theme extraction is a key feature of *advanced moderation*, which uses LLMs to to monitor and moderate content at scale across the Engage network. It does so through use of user-defined *Themes*.

## What are the deeper capabilities of AI summarization and theme extraction?

*Summaries and related conversations*: AI summarization generates concise and informative summaries of the conversations that happen around posts in the network, and shows their related threads and comments. You can get a quick overview of the main points and opinions in conversations, and explore the details if you want.

*Themes*: theme extraction identifies the most frequently discussed and trending themes anywhere in your network. You can see how your audience feels about different subjects, and what kind of content resonates with them.

*Monitor conversations*: Theme moderation identifies conversations and posts that match your specified themes. It helps you efficiently monitor the spread and engagement of specific topics across your network.

## How do users benefit from AI summarization in Viva Engage?

AI summarization supports several important capabilities to enhance and define user interactions with their Engage network and audience.  

*Understand Network Trends and Sentiment*: Allows leaders and managers to understand the network trends and sentiment that emerge from their Viva Engage content. They can identify emerging themes that are most popular, relevant, or interesting to their audience, and the positive or negative feelings associated with them. Knowing trends and sentiment helps leaders and admins gain insights into their audience's interests, needs, and opinions, and adjust their content strategy accordingly.  

*Summarize and Explore Conversations*: Help admins and managers follow the conversations that happen around posts in their network. A key target of AI summarization is to generate concise, informative summaries of the main points and opinions expressed by leaders' audiences, and show related threads and comments. Summaries save time from reading and analyzing large amounts of text, allowing leaders and managers to focus on the most relevant information.

*Create Engaging and Impactful Posts*: Help leaders and communicators create engaging posts based on their goals and preferences. By knowing the major themes related to the content posted in their network, leaders can refine their messages through content that best resonates with their intended audience.

## What are the performance metrics for AI summarization?

AI summarization measures performance with several key metrics:  

| **Metric** | **Description** |
| ---------  | --------------- |
| **Accuracy** | Assess how often the AI system's suggestions or summaries match the correct human-authored responses. Accuracy provides a fundamental measure of the system's correctness. |
| **Precision and Recall** | Evaluate the quality of suggestions and summaries. **Precision** quantifies how many of the AI-generated suggestions and summaries are relevant. **Recall** determines how many of the relevant suggestions and summaries are retrieved. |
| **F1 Score** | The F1 score combines measurements of precision and recalls for an overall measure of system performance. |
| **User Satisfaction** | To gauge user satisfaction, the Viva Engage team conducts user surveys and collects feedback to assess user satisfaction with AI system assistance. |
| **Generalizability** | Measure how the system's results generalize across different use cases. AI summarization tests on a diverse set of data and tasks. Generalizability evaluates system performance on a range of scenarios and domains that aren't part of initial training data. |
| **Red Teaming and Mitigations** | Microsoft conducts red teaming exercises, including invites of external experts and testers to find vulnerabilities or biases in the system. The process helps identify potential issues and improve system robustness.|

Our ongoing evaluation process uses continuous updates and improvements based on real-world usage and feedback. Through a combination of internal evaluation, user feedback, and external testing, Microsoft aims to ensure the accuracy, fairness, and generalizability of AI summarization.

## What are the limitations and risks of AI summarization and theme extraction?

AI summarization and theme extraction are NOT designed with a filter system in place. The objective is to allow offensive language and potentially sensitive information to surface to network admins and corporate communicators, so they can appropriately moderate content. Users of AI summarization and theme extraction can report offensive suggestions or summaries so the product team can use the feedback to inform future development.

The underlying model is trained on pre-2021 data and doesn't provide relevant responses if a question requires knowledge of the post-2021 world.

Some high-risk use cases apply in this effort:

**Privacy Concerns**: If the AI feature isn't adequately secured, it risks exposure of user data to unauthorized parties, including private themes and personal information. The Viva Engage team views the highest level of privacy and security for our users as the top priority.

**Bias**: The fairness and impartiality of AI systems like AI summarization and theme extraction depend on the quality and bias factor of the data they train on. If the training data contains biases, the AI feature could unintentionally generate content that reflects those biases, potentially causing harm or offense. We're dedicated to addressing bias in AI systems and work towards more equitable and inclusive outputs.

The Viva Engage team works to address high-risk cases and works collaboratively with the user community. We commit to deliver a safer, more responsible, and ethically sound AI experience with AI summarization and theme extraction features.

## What are the general security and privacy practices for AI summarization?

AI summarization and theme extraction include the following privacy protections:  

- The features only access content within communities and groups that each user has permission to view.

- The features don't expose content from private communities to unauthorized users.

- The features follow all existing Viva Engage privacy and security protocols.

To learn more, see [Microsoft’s privacy policy](https://go.microsoft.com/fwlink/?LinkID=331314).

## What are AI summarization's data usage, data residency and GDPR protections?

AI Summarization and theme extraction access only existing data within Viva Engage. They operate in the same data compliance framework as Viva Engage, and follow all applicable privacy regulations including GDPR. For details, see [Manage GDPR data subject requests in Viva Engage](./manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise) and [Privacy in Microsoft Viva](https://learn.microsoft.com/viva/viva-privacy).

## See also

[The Communications dashboard](https://support.microsoft.com/topic/bef4b52-ffb2-4832-8e5b-709bd04bee3b)

[Enable advanced moderation from the admin center](comms-dashboard-advanced-moderation.md)

[Admin roles for Advanced moderation and Keyword monitoring](lmc-keyword-monitoring-admin-article.md)

[Advanced moderation: keyword monitoring for Viva Engage admins](lmc-keyword-monitoring-howto-for-admin-audience.md)

For more information about how AI works in Viva Engage, see [Data, Privacy, and Security for Microsoft 365 Copilot in Viva Engage](/viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage).

For a more detailed walkthrough of Advanced moderation and its use of themes, see [Communications dashboard: Advanced moderation](https://support.microsoft.com/topic/13f58cf0-b8e5-40ab-bc55-34d69f762c1d).
