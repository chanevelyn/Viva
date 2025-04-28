---
title: Data residency for Viva Glint
description: "Data residency for Viva Glint"
ms.reviewer: 
ms.author: hasrivas
author: hasrivas
manager: josemm
audience: Admin
f1.keywords: NOCSH
ms.date: 04/28/2025
ms.topic: concept-article
ms.service: viva-glint
ms.localizationpriority: medium
ms.collection:
- m365initiative-viva-glint 
- essentials-compliance
- essentials-security
search.appverid: MET150
---

# Data residency for Viva Glint

## Summary

Microsoft Viva Glint helps organizations measure employee engagement and experiences so they can take action to improve them. Grounded in our approach to employee [engagement](https://aka.ms/VivaGlintAModernApproach), Glint offers a flexible surveying approach so organizations can gain a greater understanding of key experiences that shape an employee's journey and the resulting impact on individual and business outcomes.

## Data residency for Viva Glint

Viva Glint data residency is limited to three regions: West US, EU, and Australia. This applies to data stored at rest which constitutes metadata for the Glint surveys authored and responded to, and reports generated for those surveys. 

**West US data residency**

Required conditions:
1. _Tenant_ has a tenant hosting location country that is non-EU.
2. _Tenant_ has a valid Viva Glint license.  

**EU data residency**

Required conditions:
1. _Tenant_ has a tenant hosting country included in European Union Data Boundary (EUDB). 
2. _Tenant_ has a valid Viva Glint license.

**Australia data residency**

Required conditions:
1. _Tenant_ has a tenant hosting location country that is Australia or New Zealand.
2. _Tenant_ has a valid Viva Glint license.
3. _Tenant_ opts into migration to Australian data center.

> [!IMPORTANT]
> We may temporarily move the data outside Australia into US/EU for processing data using Microsoft 365 core services. Any data that moves outside AUustralia won't reside for more than 24 hours and will be deleted at the end of processing operations.
> For using any integrations with other products with Viva Pulse & Insights, you're agreeing to Viva Pulse & Insights data storage location

## User experience

Viva Glint data residency is seamless to the end user. The application will appropriately redirect the user to the correct region where their organizational data is hosted.


## How long is my Viva Glint data stored for?
Viva Glint data is stored for up to 3 (three) years or when an admin explicitly deletes it. Some Customer Content, like insights or inferences based on individual responses, must be deleted at the source to cascade through computed outputs. Admins can delete files on behalf of users.

