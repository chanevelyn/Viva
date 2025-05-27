---
ms.date: 05/5/2025
title: Copilot Studio agents report
description: Learn how to use the Copilot Studio agents Power BI template to understand the adoption and impact of Microsoft 365 Copilot custom agents across your organization.
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.localizationpriority: medium 
ms.collection: 
- viva-insights-advanced
- viva-copilot
- magic-ai-copilot 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Copilot Studio agents report (preview)

>[!IMPORTANT]
> This feature is for public preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader release.

The **Copilot Studio agents report** can help you understand the adoption and impact of Microsoft 365 Copilot custom agents across your organization.

This report can help you answer questions such as: 

* What are the top agents being used?
* What are top agents' high-level KPI-like sessions, satisfaction scores, and success rates?  
* What is the impact of individual agents, such as the split of engaged sessions  and topics distribution, as well as the impact of agent-assisted hours?

**Example Agent KPI's**

* Measuring agent engagement. [Learn more](/microsoft-copilot-studio/guidance/measuring-engagement).
* Measuring agent outcomes. [Learn more](/microsoft-copilot-studio/guidance/measuring-outcomes).

This report is based on Copilot usage and impact metrics for agents built using Microsoft Copilot Studio, which are published outside of Copilot and Copilot Chat. This report **excludes** agents that enhance Microsoft 365 Copilot as well as autonomous agents. [Learn more about Microsoft Copilot Studio](/microsoft-copilot-studio/fundamentals-what-is-copilot-studio).

**What's *not* covered in this report:**

1. Agents that enhance Microsoft 365 Copilot:

* Agents built using Microsoft Copilot Studio which are [published to Microsoft 365 Copilot](/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams) and Copilot Chat using the setting **Make agent available in Microsoft 365 Copilot** in the configuration panel for publishing to Teams and Microsoft 365 channels

* Agents published to [use within Microsoft 365 Copilot](/microsoft-365-copilot/extensibility/agents-overview) and Copilot Chat (declarative or custom engine agents), regardless of how they're built and published

2. Autonomous Agents that proactively respond to signals across your business and initiate tasks, which can be configured to react to events or triggers without human intervention. [Learn more](/microsoft-copilot-studio/authoring-triggers-about).

## Prerequisites

This report is enabled for tenants who meet the following eligibility criteria:

1. Tenant must have at least 50 Copilot licenses.
2. Tenant must have at least one Microsoft Copilot Studio license, either standalone, pay-as-you-go, or bundled with Copilot, and have created at least one agent and published it within a "Production" environment. [Learn more](/power-platform/admin/environments-overview).

In addition, before you can run the query and populate the report in Power BI, you’ll need to:

* Be assigned the role of **Insights Analyst** in Viva Insights. [Learn more about how to assign roles](../../setup-maint/assign-user-roles.md).
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/power-platform/products/power-bi/getting-started-with-power-bi) to download and install the latest version.
* Ensure that data from Copilot Studio flows to Viva Insights. [Learn more](https://go.microsoft.com/fwlink/?linkid=2301464).

## Report setup

### Run query

1. In the [Viva Insights analyst experience](https://analysis.insights.viva.office.com), select **Create analysis**.

2. Under **Power BI templates**, navigate to **Copilot Studio agents report** and select **Set up analysis**. The template can also be found under the **Copilot** section.

3. Under **Query setup**:
    1. Enter a **Query name**.
    2. Select a **Time period**, which defaults to **Last 1 months**.

    > [!NOTE]
    > To start, you can only run an analysis covering the last month, but eventually you'll be able to select a wider time period as Microsoft Copilot Studio collects more data.

    3. Set **Auto-refresh** (optional). You can set the query to automatically update by selecting **Auto-refresh**. When you select this option, your query automatically runs and computes a new result every time Viva Insights gets updated agent data.

    > [!NOTE]
    > If Agent data used in an auto-refreshing query changes (for example, an agent attribute name is changed or an attribute is removed), the query might stop auto-refreshing.

    4. Enter a **Description** (optional).
    
    > [!NOTE]
    > The **More settings** pane also contains **Group by** and **Metric rule** settings. This Power BI query is set to **Group by Month**, and you can't change this setting, and neither can you change the **Metric rule** setting.

4. Under **Predefined template metrics**, view a list of preselected metrics, which appear as gray tags. These metrics are required to set up the Power BI report and you can't remove them. Session-related metrics are always available, but the availability of topic- and Knowledge source-related metrics depends on the data available from Copilot Studio. You can add other metrics by selecting **Add metrics**.

5. Under **Select which agents you want to include in the query**, add filters to narrow down the agents in scope for your report. You can filter by agent name, agent surface, and agent type. [Learn more about filter and metric options](..//..//analyst/filters.md).

6. Under **Select which agent attributes you want to include in the query**, attributes are selected automatically. Once the query runs, you can use these attributes to group and filter the reports.

    > [!IMPORTANT]
    > This Power BI query needs some specific attributes to run, and we've preselected them for you. These attributes appear in gray and you can't remove them. You **can't** add other attributes by selecting **Add attributes**.

7. Select **Run** on the upper right. The query might take a few minutes to run.

### Access query results

You can access the report in two ways:  

* View the report in the browser. Use this option if you only want to view the report.  

* Open the Power BI template in Power BI desktop and connect to your query results. Use this option if you want to customize the report or share it with others in your organization by publishing the report to the Power BI Service.

### View report in the browser  

To view the report in the browser, go to the **Query results page** and select the eye icon in the View column. Select **Open in new tab** if you want to keep the report in the background while doing other tasks in Advanced insights.

### Open the Power BI template in Power BI Desktop

1. Go to the Query results page and select the Power BI icon in the Actions column to download the Power BI template and get the query and partition identifiers. You'll need these identifiers later.  

2. Open the downloaded template.  

3. If you're prompted to select a program, select **Power BI**.  

4. When you're prompted by Power BI:
    1. Paste in the partition and query identifiers.  
    2. Select **Load** to import the query results into Power BI.

5. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data. For large files, this process might take a few minutes.

    > [!IMPORTANT]
    > You need to sign in to Power BI with the same account you use to access Viva Insights. If available, select **Organizational account** from the left. You might have to sign in more than once.
    >
    > :::image type="content" source="../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab":::

## Page-level settings

Each report page includes the following settings at the top:

* **Time period for the report** – Select the start and end date for the data you'd like to view.

* **Apply filters** – Select the Category, Agent name, Type, and Internal or External values to filter the Agents shown in the report.

## About this report

The **Copilot Studio agents report** includes the following report pages to help you better understand agent adoption and KPI's across your organization.

### Custom agent adoption summary  

This page provides an initial overview of adoption of the agents across the organization for the selected filters. The card on the left summarizes the total number of engaged agent sessions. Learn more about measuring [agent engagement](/microsoft-copilot-studio/guidance/measuring-engagement) and [outcomes](/microsoft-copilot-studio/guidance/measuring-outcomes).

The page also provides the engaged agent session trend for the selected time frame.

The card in the middle of the page indicates the total number of agents enabled for the tenant as well as the top three custom agents based on the number of monthly engaged sessions.

The card on the right defines the overall Agent Outcome impact in terms of satisfaction score and resolution rate.

### Identify Top agents used across the organization  

This page lets you focus on top agents sorted in descending order based on the number of monthly engaged sessions, and explore the Key Agent KPI's.  

You can filter the agents on this page using the as Category, Agent name, Type, and Internal or External values.

### Understand Deep Dive Agent Impact page