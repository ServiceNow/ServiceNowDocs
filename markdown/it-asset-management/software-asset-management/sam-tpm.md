---
title: Use Software Asset Management and Application Portfolio Management to manage technology onboarding
description: Use the Software Asset Management application along with Technology Reference Model \(TRM\) of Application Portfolio Management to manage onboarding of technologies.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2022-09-14"
reading_time_minutes: 2
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Use Software Asset Management and Application Portfolio Management to manage technology onboarding

Use the Software Asset Management application along with Technology Reference Model \(TRM\) of Application Portfolio Management to manage onboarding of technologies.

TRM is a list of software products with information on their approval of use. Each product is associated with a set of lifecycle phases with a start and end date. The TRM library is maintained by the enterprise architect and used by application owners. For detailed information on TRM, see [Technology Reference Model](https://www.servicenow.com/docs/access?context=technology-reference-model-in-apm&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US).

The Software Asset Management application gives visibility into the TRM lifecycle phases for all products associated with software models. When a software model is created and associated with a product that is approved for use in TRM, the **Certified** check box in the software model form is selected by default. All software models associated with that product are then available for use.

![Software model from](../image/sam-tpm.png)

If the same product in TRM is later marked as unapproved, the existing software models associated with that product don't reflect that change. However, when you open the existing software models, a banner appears stating `This software is not approved for use in the Technology Reference Model (TRM). To be in sync with the TRM, set the Certified flag to FALSE.`.

If a new software model is created with this product, that software model is marked as unapproved, and a banner isn't displayed as this software model is in sync with TRM.

If a product is marked as unapproved in TRM, reclamation candidates are automatically created for all software installations that are associated with that product. After the product is approved for use in TRM, the existing reclamation candidates are either marked **Closed complete** or **Closed canceled**.

## Software Asset Management and TRM use case

This section describes a use case that demonstrates how the Software Asset Management application and TRM interact.

For example, you create a software model SW1, on September 15, 2022, and associate it with PostgreSQL, which is an unapproved product in TRM. By default, the **Certified** check box in the SW1 form is set to false and the **Restricted software** check box is set to true. Also removal candidates are created for any installations discovered.

On September 18, 2022, release 14.5 of PostgreSQL gets approved for use in TRM. If you now open SW1 a banner appears stating the following `This software is approved for use in the Technology Reference Model (TRM). To be in sync with the TRM, set the Certified flag as true`. However software models with older versions would continue to be restricted.

If you create another software model SW2, on September 19, 2022, and associate it with PostgreSQL, the **Certified** check box is set to true and the **Restricted software** check box is set to false in the SW2 form.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

