---
title: Lift and Shift and Innovate - LOB Apps
titleSuffix: Azure Solution Ideas
author: adamboeglin
ms.date: 12/16/2019
description: This architecture shows how to easily connect multiple business systems to enable customer support.
ms.custom: acom-architecture, line of business app, lob app, lift and shift cloud strategy, cloud migration, cloud innovation, lift and shift solution, lift and shift strategy, interactive-diagram, 'https://azure.microsoft.com/solutions/architecture/modern-customer-support-portal-powered-by-an-agile-business-process/'
ms.service: architecture-center
ms.subservice: solution-idea
---

# Lift and Shift and Innovate - LOB Apps

[!INCLUDE [header_file](../header.md)]

This line-of-business application solution provides a mechanism for monitoring and responding to customer feedback. Easily connect multiple business systems to enable nimbler customer support.

Related Links:

* [Matching the architecture to your business needs](../../guide/design-principles/build-for-business.md)

* [Managing identities in your applications](../../multitenant-identity/index.md)

* [Automate access and use of data across applications with Logic Apps](https://docs.microsoft.com/azure/logic-apps)

* [Infuse intelligence into your apps with Cognitive Services](https://docs.microsoft.com/azure/cognitive-services/welcome)

## Architecture

![Architecture diagram](../media/modern-customer-support-portal-powered-by-an-agile-business-process.svg)

## Data Flow

1. Customer submits feedback posted to a web endpoint.
1. The feedback is posted to Microsoft Cognitive Services Text Analytics API to extract sentiment and keywords.
1. The customer feedback creates a new case in Dynamics CRM or other CRM.
1. The solution sends a text message to the customer, thanking them for the feedback.
1. If the feedback sentiment scores lower than 0.3, the app posts this information to a customer service channel to respond.
