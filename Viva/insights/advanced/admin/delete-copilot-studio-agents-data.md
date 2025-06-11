---
ms.date: 06/5/2025
title: Delete Copilot Studio agents data in Viva Insights
description: Learn how to delete data from Microsoft Copilot Studio agents in Viva Insights, which is used for the Copilot Studio agents report.
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

# Delete Copilot Studio agents data in Viva Insights (preview)

>[!IMPORTANT]
> This feature is for public preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader release.

Microsoft Copilot Studio sends agents metrics to Viva Insights, which populate the [Copilot Studio agents report](..//..//advanced/analyst/templates/copilot-studio-agents.md). This article shows you how to delete Copilot Studio agents data in Viva Insights.

>[!IMPORTANT]
> If you delete Copilot Studio agents data, the data can't be recovered. This also stops further data processing, so analysts won't be able to run new reports that use Copilot Studio agents data.
>
>Queries you ran *before* you deleted Copilot Studio agents data are also no longer available to analysts. 
>
>You can't un-do this deletion.

### Workflow 

1. The Viva Insights Administrator or, depending on your organization's settings, the tenant admin registers an Azure application. 

2. The tenant admin grants consent to the application to access the Viva Insights API.

3. The Viva Insights Administrator runs a PowerShell cmdlet to delete Copilot Studio agents data in Viva Insights.

## 1. Register a new app in Azure

*Applies to: Viva Insights Administrator or tenant admin*

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com). 

2. Navigate to **Identity** > **Applications** > **App registrations** and select **New registration**.
    1. On the next screen:
        1. Give your app a name. 
        2. Under **Supported account types**, leave the first option, **Accounts in this organizational directory only ([Your organization] only - Single tenant)**, selected. 
        3. Under **Redirect URI (optional)**, select **Public Client/native (mobile and desktop)** and provide the following URI: `https://login.microsoftonline.com/common/oauth2/nativeclient`.
        4. At the bottom, select **Register**.

        :::image type="content" source="../images/delete-agent-data-register-app.png" alt-text="Screenshot that shows how to register a new app in Azure." lightbox="../images/delete-agent-data-register-app.png":::

    2. On the **Overview** screen, copy the **Application (client) ID** and **Directory (tenant) ID**. Keep these IDs handy. You'll need them later.

        :::image type="content" source="../images/delete-agent-data-ids.png" alt-text="Screenshot that shows the application and directory IDs.":::

3. Add an API permission: 
    1. Select **API permissions**, then **Add a permission** and select **APIs my organization uses**. 
    2. In the search bar, enter "Workplace Analytics."
    3. Select **Workplace Analytics** and select **Delegated permissions**. 
    4. Under **Select permissions**, select **AdministratorSettings.ReadWrite**. 
    5. Select **Add permissions**.

4. Remove API permissions: 
    1. On the left, select **API permissions**. 
    2. For the Microsoft Graph API, select the ellipsis (...) to the right of the API and select **Remove permission**. 
    3. Confirm removal.
    
    When you remove permissions for the Microsoft Graph API, you're making sure the app only has permissions for what it needs.

> [!NOTE]
> [Learn more about how to register an app in Azure](/entra/identity-platform/quickstart-register-app).
>
> [Learn more about who can register applications](/security/zero-trust/develop/app-registration#who-can-add-and-register-applications).

## 2. Grant admin consent to the application 

*Applies to: Viva Insights Administrator and tenant admin*

The Viva Insights Administrator asks the tenant admin to grant permission to this app to access Viva Insights resources. [Learn more about permissions and consent](/entra/identity-platform/permissions-consent-overview).

## 3. Run the PowerShell cmdlet 

*Applies to: Viva Insights Administrator*

1. Launch Terminal on Windows. 

2. Execute the git clone command followed by the repository URL:

    ```powershell
    git clone https://github.com/microsoft/vivainsights_copilotstudioagentsdelete.git
    ```

3. Navigate to the folder: cd vivainsights_copilotstudioagentsdelete/PowerShellApp 

4. Run the script using the **Application (client) ID** and the **Directory (tenant) ID** you saved:

    ```powershell
    .\CopilotAgentsDelete.ps1 -[ClientId] -[TenantId]
    ```

### Related topics

[Copilot Studio agents report](..//..//advanced/analyst/templates/copilot-studio-agents.md)
