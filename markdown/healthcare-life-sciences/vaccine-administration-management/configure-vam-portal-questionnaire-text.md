---
title: Configure the questionnaire text for the user and clinician portals
description: Configure the questionnaire text that is displayed in the user and clinician portals for Vaccine Administration Management.
locale: en-US
release: zurich
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure the questionnaire text for the user and clinician portals

Configure the questionnaire text that is displayed in the user and clinician portals for Vaccine Administration Management.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Catalog** &gt; **Catalog Definitions** &gt; **Maintain Catalogs**.

2.  Open the Vaccination Catalog record.

3.  From the Catalog Items related list, update the questionnaire text by updating the corresponding variables from the following catalog items.

    **Note:** The questionnaire text is distributed across the following catalog items and variables.

<table id="table_bk2_dzq_bpb"><thead><tr><th>

Catalog item

</th><th>

Variable set

</th><th>

Variable

</th></tr></thead><tbody><tr><td rowspan="3">

Pre-appointment questionnaire

</td><td rowspan="3">

Pre-vaccination screening

</td><td>

recently\_sick

</td></tr><tr><td>

recent\_vaccination

</td></tr><tr><td>

pregnant

</td></tr><tr><td rowspan="4">

Schedule your vaccination

</td><td rowspan="4">

Disclose any conditions

</td><td>

long\_term\_health\_issues

</td></tr><tr><td>

long\_term\_health\_history

</td></tr><tr><td>

any\_reaction

</td></tr><tr><td>

any\_infections

</td></tr><tr><td>

Enter your personal info

</td><td>

Your demographic info

</td><td>

age\_group

</td></tr></tbody>
</table>    For details on how to configure a variable, see [Service Catalog variables](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariables&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    **Important:**

    -   Updating the questionnaire text updates that text in both the user and clinician portals.
    -   If you deactivate a variable, then the question will be hidden in both the user and clinician portals.
    -   If you're creating a question, the new question isn’t displayed in the clinician portal by default. You must also update the pre-vaccine\_questionnaire widget by navigating to **All** &gt; **Service Portal** &gt; **Widgets**. For details on how to configure a widget, see [Service Portal widgets](https://www.servicenow.com/docs/access?context=service-portal-widgets&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
4.  Click **Update**.


**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

