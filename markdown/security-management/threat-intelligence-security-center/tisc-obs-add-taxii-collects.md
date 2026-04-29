---
title: Add to TAXII Collections from Library List View
description: Add to TAXII Collections feature enables analysts to add the selected threat intelligence including observables, indicators, and objects such as attack patterns, threat actors and so on directly to TAXII collections.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Add to TAXII Collections from Library List View

Add to TAXII Collections feature enables analysts to add the selected threat intelligence including observables, indicators, and objects such as attack patterns, threat actors and so on directly to TAXII collections.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

Following is the procedure that shows how to add TAXII collections to an observable.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Select the observable type.

    **Note:** The **Add to TAXII Collections** button is not available if you select **All Observables**. To enable this button, you must select a specific observable type, for example **Email Message**.

3.  Click **Add to TAXII Collections** button.

4.  Select the TAXII Collections sample template.

    All the templates configured on the Outbound Intel Sharing page appear here, allowing you to select the one you need. For more information, see .

    ![Add to TAXII collections dialog showing template selection drop down with available collection options.](../image/tisc-add-taxii-collection-lib.png)

5.  Select **Add**.

    You will be prompted to select a template. Any templates you’ve previously created will be listed here for you to select.

6.  Once you have selected the template select **Add**.

    A TAXII collection addition job record is created to track the action.

7.  Click on the job record to view its details.

    You will see the specific records that have been successfully added to the TAXII Collection.

    This process confirms which intelligence items were shared and provides an auditable record of the action.

    **Note:** A system property `sn_sec_tisc.add_to_taxii_collection_entity_threshold` defines the maximum number of entities \(observable records\) that can be added to a TAXII Collection in a single request. The system enforces a hard limit of 10000 entities.

8.  Select the **Record** section of the job record.

9.  Drill down to the **TAXII Collection Records** section.

    You will notice that the selected observable\(s\) are added to the TAXII collection and you will also see the exclusion rules.

    Exclusion rules define which records or data should not be included when adding items to a TAXII Collection, ensuring that only the intended intelligence is shared. Each template comes with its own sharing template controls, which specify the attributes and information to include or exclude during sharing.

    In addition, exclusion rules also allows you to automatically prevent certain records from being added to a TAXII Collection.

    Any records that match the criteria defined in these rules are excluded and cannot be shared. For example, if a global exclusion rule is configured to block domains with a specific status, such as red or clear, any record matching that condition will be automatically excluded.

    When you attempt to add such records to a TAXII Collection, the application will indicate that they have been excluded \(see the screenshot below\), ensuring that only the intended and allowed intelligence is shared. For more information on the exclusion rules, see .

    ![Dialog box showing excluded records notification when adding to TAXII collections.](../image/tisc-excluded-records-taxii-collect.png)


## What to do next

Once you add the records to the TAXII collections, navigate to **Administration** &gt; **TAXII Outbound Server** &gt; **TAXII Collections** to view the added records under the **TAXII Collection Records** section. For more information, see  and .

**Marking Definitions for Records Added to TAXII Collections**

When you add a record to a TAXII Collection, the application automatically applies marking definitions to provide additional context about the record.

For example:

If a record has a TLP \(Traffic Light Protocol\) classification, such as TLP White a related reference record is created to explain what that TLP level means.

This ensures that users accessing the shared intelligence are aware of the requirements of each record. When a record is added to a collection, any relevant metadata or contextual records such as TLP markings are automatically created and linked.

**Note:** When adding records, the Traffic Light Protocol \(TLP\) value associated with the intelligence records is included as a TLP 2.0 marking definition object. For more information, see [Define Marking Definition](define-market-definition.md).

**Managing Global Exclusion Rules in TAXII Collections**

In the **Administration** section, you can view and manage all configuration-related settings, including global exclusion rules. These rules determine which records are automatically excluded from being added to a TAXII Collection.

For example, an exclusion rule might exclude domains marked with TLP Red or TLP Clear. You can customize these rules. For example, you could modify it to exclude only TLP Red records.

When you attempt to add records to a TAXII collection:

-   If all selected records match the exclusion rules, the application prevents any records from being added.
-   If some records from the selection are valid, then those records are added to the TAXII collection, while the excluded records are automatically filtered out.

For more information on the exclusion rules, see .

