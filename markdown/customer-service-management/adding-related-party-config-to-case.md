---
title: Add related party configurations to cases, sold products, install bases, or service organizations
description: Link related party entity responsibilities to responsibility definitions by adding related party configurations to cases, sold products, install bases, or service organizations for customer access management.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure customer access management, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Add related party configurations to cases, sold products, install bases, or service organizations

Link related party entity responsibilities to responsibility definitions by adding related party configurations to cases, sold products, install bases, or service organizations for customer access management.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Related Party Configuration**.

2.  To create a related party configuration, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Related party configuration type.|
    |Applies To|Table assigned with the related party configuration.|
    |Entity Type|Entity type such as an account, a consumer, or a product.|
    |Reference Condition|Filter condition for defining the related party configuration. In the **Reference Condition** field, you can select **Add Filter Condition** or **Add "Or" Clause**.|
    |Default Responsibility|Access level to different entities and the related information.|

4.  Select **Submit**.

    Related party configurations that are provided with the base system are listed in the following tables.

    1.  Types and responsibilities for cases are listed in the following table.

        |Type|Responsibility|
        |----|--------------|
        |Authorized Contact|Authorized Representative|
        |Authorized Consumer|Authorized Representative|
        |Authorized Contributor|Authorized Representative|
        |Listed Contact|Not applicable|
        |Listed Consumer|Not applicable|

    2.  Types and responsibilities for sold products are listed in the following table.

        |Type|Responsibility|
        |----|--------------|
        |Authorized Account|Authorized Account|
        |Authorized Contact|Authorized Representative|
        |Authorized Consumer|Authorized Representative|
        |Listed Account|Not applicable|
        |Listed Contact|Not applicable|
        |Listed Consumer|Not applicable|

    3.  Types and responsibilities for install bases are listed in the following table.

        |Type|Functional role|Responsibility|
        |----|---------------|--------------|
        |Authorized Account|Install Base Authorized Contact \(sn\_install\_base.install\_base\_authorized\_contact\)|Authorized Account|
        |Authorized Contact|Install Base Authorized Contact \(sn\_install\_base.install\_base\_authorized\_contact\)|Authorized Representative|
        |Authorized Consumer|Install Base Authorized Consumer \(sn\_install\_base.install\_base\_authorized\_consumer\)|Authorized Representative|
        |Authorized Contributor|Install Base Authorized Contributor \(sn\_install\_base.install\_base\_authorized\_contributor\)|Authorized Representative|
        |Authorized Member|Install Base Authorized Member \(sn\_install\_base.install\_base\_authorized\_member\)|Authorized Representative|
        |Authorized Service Organization|Install Base Authorized Member \(sn\_install\_base.install\_base\_authorized\_member\)|Authorized Service Organization|
        |Listed Account| |Not applicable|
        |Listed Contact| |Not applicable|
        |Listed Consumer| |Not applicable|
        |Listed Contributor| |Not applicable|
        |Listed Member| |Not applicable|
        |Listed Service Organization| |Not applicable|

    4.  Types and responsibilities for service organizations are listed in the following table.

        |Type|Responsibility|
        |----|--------------|
        |Location Agent|Location Agent|
        |Location Consumer Agent|Location Consumer Agent|
        |Location Contributor|Location Contributor|
        |Location Manager Contributor|Location Manager Contributor|
        |Location Manager Fulfiller|Location Manager Fulfiller|
        |Listed Member|Not applicable|

    **Note:**

    -   Whenever a related party record is created, the **Responsibility** field gets auto-populated from the default responsibility associated with the selected type​.
    -   Listed role types don’t have any responsibility. Since the correct role and responsibility determine access, related parties are not granted access if the **Responsibility** field is left empty.​ For more information on install base related parties, see [Add a related party to an install base item](add-related-party-install-base.md).
    -   Assign the sn\_customerservice.case\_contributor\_creator role to the Authorized Contributor related party to view and update the cases of the install base.

