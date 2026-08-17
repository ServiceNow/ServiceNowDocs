---
title: Resolving custom variant issues in Workplace Central
description: After upgrading Workplace Service Delivery \(WSD\) to a later release, custom variants created using the legacy application-specific screen collection model no longer display correctly in Workplace Central. Affected variants must be migrated to the new standardized unified screen collection model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/custom-variants-in-workplace-central.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: topic
last_updated: "2022-08-11"
reading_time_minutes: 5
breadcrumb: [Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Resolving custom variant issues in Workplace Central

After upgrading Workplace Service Delivery \(WSD\) to a later release, custom variants created using the legacy application-specific screen collection model no longer display correctly in Workplace Central. Affected variants must be migrated to the new standardized unified screen collection model.

## App Shell UI variants overview

Workplace Central runs on the ServiceNow App Shell UI framework, which renders each record page using a variant — a screen or layout definition tied to the record's table. Rather than a single fixed layout, App Shell UI selects the variant that matches the record being opened.

A custom variant is a variant that an administrator defines to replace the default layout for a given set of records. For example, an admin might build a custom variant for Workplace Case records that adds extra fields or rearranges components differently from the out-of-box layout.

Symptom:

Customers may observe one or more of the following after upgrading to the later release:

-   Custom variants don't render or display a empty screen when navigating to a record.
-   Custom variants created before the previous release are no longer applied.
-   The correct variant is not selected when opening a Workplace Central record.
-   Record pages fall back to the default variant instead of the configured custom variant.

As part of a recent WSD release, ServiceNow standardized WSD record page routing to improve consistency across applications and reduce long-term maintenance complexity. Previously, custom variants relied on application-specific screen collections \(for example, "Case Record"\) to determine which variant to display. The new model consolidates all variants under a single unified record variant collection \(`record`\) and uses table-specific screen conditions \(encoded queries\) to route the correct variant per table.

**Important:** Custom variants that still reference a legacy application-specific screen collection will not be evaluated under the new routing model and will not display.

## Resolution

## Procedure

1.  Update each affected custom variant by changing the Screen Collection to the unified `record` collection and adding a Screen Condition that specifies the target table\(s\). Complete all steps for every custom variant that uses a legacy screen collection. Variants not updated will remain non-functional after the upgrade.
2.  Navigate to your variant.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **App Shell UIs**.

    2.  From the list, select **Workspace App Shell**.

    3.  In the related list **Child Screens**, choose the screen under which your custom variant is configured.

    4.  Open the custom variant record.

3.  Update the **Screen Collection** field.

    In the variant record, locate the **Screen Collection** field and change the value from the legacy application-specific collection \(for example, "Case Record"\) to:

    ```
    record
    ```

4.  Add a **Screen Condition**.

    The **Screen Condition** field must contain an encoded query that identifies the table\(s\) this variant applies to. Use the following format:

    ```
    table=<table_name>^ORtable=<table_name_2>
    ```

    Example — variant applies to both Workplace Case and Move Case:

    ```
    table=sn_wsd_case_workplace_case^ORtable=sn_wsd_move_case
    ```

    **Tip:** If multiple custom variants exist for the same screen, verify each has a unique and non-overlapping Screen Condition to avoid routing conflicts.

5.  Select **Save** to apply the configuration changes.

    The following table shows the exact field values before and after the update for a custom variant used on Workplace Case records:

    |Before \(Legacy Configuration\)|After \(Updated Configuration\)|
    |-------------------------------|-------------------------------|
    |Screen Collection: Case Record|Screen Collection: `record`|
    |Screen Condition: \(empty\)|Screen Condition: `table=sn_wsd_case_workplace_case^ORtable=sn_wsd_move_case`|

6.  Verify the variant displays correctly.

    1.  Navigate to a record that should use the custom variant.

    2.  Confirm the variant renders correctly and the expected layout is applied.

    3.  If the variant still does not display, check the encoded query for typos and verify the table name is correct.

    For more information about support and troubleshooting, see [KB3107832](https://support.servicenow.com/kb_knowledge.do?sys_id=af2dedc747e14fdc77b5ab29736d4363&sysparm_record_target=kb_knowledge&sysparm_record_row=1&sysparm_record_rows=1&sysparm_record_list=sys_created_bySTARTSWITHchitra%5EORDERBYDESCnumber).


**Parent Topic:**[Workplace Central reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/workplace-central-references.md)

**Related topics**  


[Components installed with Workplace Central]()

[Space Optimization - Key features and actions]()

[Workplace Central Event planner]()

[Scenario and Building - Views, states, settings, and key features]()

[Space request approvals, states, actions, and key features]()

[Move management key features and actions]()

[Case Management - Key features, Actions &amp; Case details]()

[Schedule Plan details form]()

[Scenario details form]()

[Space Deployment Plan]()

[User Deployment Plan]()

[Excel column lengths for move projects]()

[Move conflicts for projects created via Excel upload]()

[Workplace Central troubleshooting]()

[Workplace Task form - Space Assignment task]()

[Neighborhood User Assignment Rule form]()

[User Workplace Profile form]()

