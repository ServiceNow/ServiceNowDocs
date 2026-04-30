---
title: Link the insurance product model and claim case service definition
description: Link the insurance product model and claim case service definition by using the Insurance claims application. Without this link, the system doesn’t know which policies are relevant to the case service definition.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2024-10-10"
reading_time_minutes: 1
breadcrumb: [Creating a service definition for Insurance claims, Setting up Insurance claims, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Link the insurance product model and claim case service definition

Link the insurance product model and claim case service definition by using the Insurance claims application. Without this link, the system doesn’t know which policies are relevant to the case service definition.

## Before you begin

Set the application scope of your instance to **Insurance claims**.

Role required: admin

## About this task

After creating an insurance product model and a claim case service definition, you must create a link between them. By linking the claim case service definition to the product model, you can help to ensure that the policies that are connected to the insurance product model are available for selection. This claim creation process helps to ensure that all claims are accurately tied to the appropriate policies and coverages.

## Procedure

1.  Navigate to **All** &gt; **Insurance claims** &gt; **Administration** &gt; **Service definition**.

2.  Open the service definition that you wish to link.

3.  In the Product Service Relationships related list, select **New**.

4.  In the **Product** field, select the insurance product model that you want to link.

5.  Select **Submit**.

    You can associate multiple product models to a case service definition. For example, you might associate multiple products if you have a commercial product model.


## What to do next

Associate another product model by repeating steps 3–5.

**Parent Topic:**[Creating a service definition for Insurance claims](../concept/create-service-definitions-for-insurance-claims.md)

