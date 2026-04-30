---
title: Manage onboarding of hardware products using Application Portfolio Management
description: Onboard your hardware products and manage the Technology Reference Model \(TRM\) life-cycle by using Technology Reference Model \(TRM\) of Application Portfolio Management along with the Hardware Asset Management application.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Hardware Asset Management, IT Asset Management]
---

# Manage onboarding of hardware products using Application Portfolio Management

Onboard your hardware products and manage the Technology Reference Model \(TRM\) life-cycle by using Technology Reference Model \(TRM\) of Application Portfolio Management along with the Hardware Asset Management application.

The Technology Reference Model enables you to maintain a list of hardware products with information on their approval of use within the organization. The TRM library is maintained by enterprise architects and used by application owners. For detailed information on TRM, see [Exploring Technology Reference Model - Legacy](https://www.servicenow.com/docs/access?context=technology-reference-model-in-apm&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US). TRM enables application owners to request hardware products to be used in the organization, onboard the product, and define the TRM life-cycle phases.

Each hardware product model is associated with a set of life-cycle phases with a start and end date. The Hardware Asset Management application gives visibility into the TRM life-cycle phases for all hardware models associated with a product.

## Synchronizing TRM information with Hardware Asset Management

The HAM - Sync TRM information scheduled job in Hardware Asset Management runs daily to fetch information such as TRM phase and life-cycle for normalized product models from TRM. The job then sends the TRM details to the Hardware Asset Management application. When the scheduled job runs daily, any updates made to the TRM phase are synchronized with Hardware Asset Management.

You can view the following TRM-related information for a hardware product model in the Model Management view of Hardware Asset Workspace:

-   The TRM phase using the **TRM product phase** field on the **Details** tab of the hardware product model.
-   TRM life-cycle information using the **TRM Product Lifecycles** related tab of the hardware product model.

