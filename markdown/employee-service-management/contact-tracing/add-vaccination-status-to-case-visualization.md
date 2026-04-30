---
title: Configure contact tracing visualization to show vaccination status
description: Configure Contact Tracing so case managers can view the vaccination status of potentially exposed contacts in the contact tracing visualization.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure contact tracing visualization to show vaccination status

Configure Contact Tracing so case managers can view the vaccination status of potentially exposed contacts in the contact tracing visualization.

## Before you begin

The Vaccination Status application must be installed and configured. For more information, see [Vaccination Status](../../vaccination-status/concept/vaccination-status.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Properties**.

2.  Set the **sn\_imt\_tracing.show\_contact\_vaccination\_status** property to **Yes**.

    This step enables vaccination statuses to display on the contact tracing visualization.

3.  Click **Save**.

4.  Assign the Vaccination Status application sn\_imt\_vaccine.vaccine\_profile\_reader role to each case manager.

    The vaccination status and the **Vaccinated** column in **Exposed Contacts** are hidden until you have this role.

    **Note:** If the **sn\_imt\_tracing.show\_contact\_vaccination\_status** property is set to **No**, case managers with the sn\_imt\_vaccine.vaccine\_profile\_reader role can see the **Vaccinated** column, but the column is empty.


## Result

Case managers can see the vaccination status of users on the case form in both the contact tracing visualization and the **Exposed Contacts** list. For more information, see [Working on a case through contact tracing visualization](../reference/contact-tracing-case-visualization.md).

If a case manager can't see vaccination statuses even though the **sn\_imt\_tracing.show\_contact\_vaccination\_status** property is set to **Yes**, confirm that the case manager has the sn\_imt\_vaccine.vaccine\_profile\_reader role.

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

