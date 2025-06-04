---
title: Granular access controls for Viva Pulse
description: "Granular access controls for Viva Pulse"
ms.reviewer: 
ms.author: michellehu
author: michellehu
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 03/19/2025
ms.topic: how-to
ms.service: viva-pulse
ms.localizationpriority: medium
ms.collection:
- m365initiative-viva-pulse
- essentials-security  
search.appverid: MET150
---

# Granular access controls for Viva Pulse

As a Viva Pulse administrator, you can use create or manage policies to define which users can access specific features in Viva Pulse. Feature access management enables you to configure which specific features of Viva Pulse are available to certain groups or users within your tenant. These help to tailor Viva Pulse to meet your local regulatory and business requirements. See [Control access to features in Viva](https://go.microsoft.com/fwlink/p/?linkid=2245618) to learn more.

For all of the features below, admins can use centralized feature access management to determine access at the tenant level, at the group level by using Microsoft Entra ID groups or Microsoft 365 groups, or at the user level for maximum flexibility. The following features are all default turned on for your tenant.

## Pulse experience with Microsoft 365 Copilot

Users with a Microsoft 365 Copilot license have access to the full functionality of Viva Pulse to gather real-time feedback from their teams. Viva Pulse is default turned on for tenants with a Microsoft 365 Copilot license. Use the FeatureID value **PulseExpWithM365Copilot** to configure Viva Pulse for your tenant.

## Copilot in Viva Pulse

Viva Pulse authors can view a summary of their Pulse reports generated using Copilot. This summary can help give a quick overview of their report, highlights, and opportunity areas without needing to go into the details of their Pulse report. Use the FeatureID value **CopilotInVivaPulse** to configure conversations in Pulse reports for your tenant.

## Customization

Admins can control whether feedback authors can add their own questions to existing stock templates or edit existing stock questions. Use the FeatureID value **CustomizationControl** to configure customization capability for your tenant.

## Conversations in Pulse reports

Viva Pulse authors can respond to open text responses in their Pulse reports and have a de-identified conversation with the Pulse participant who provided that particular open text response. Use the FeatureID value **PulseConversation** to configure conversations in Pulse reports for your tenant.

## Resources

To configure these capabilities, see [Control access to features in Viva](https://go.microsoft.com/fwlink/p/?linkid=2245618). To control who has access to specific Viva features you can create and update policies in the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/?linkid=2310835) or in [PowerShell](https://go.microsoft.com/fwlink/?linkid=2310836). Policies are used to enable or disable specific features or types of data processing for users or groups in your tenant.
