---
title: Content references in GRC
description: You can add tags to virtually any type of record defined in GRC applications that reference GRC content packs, integrations, use case accelerators, or any new regulations that use those records. After the records have been tagged, you can filter the content reference tags to identify which records are used within each application.As you are analyzing any of the many types of records available in GRC applications, it is easy to add a content reference tag so the record can be included when you perform searches for records associated with a given integration, content pack, use case accelerator, and so forth.You can define new content reference tags, as needed, to accommodate new regulations as they arise. You can define new tags in any GRC application, and they are then available in all GRC applications.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Content references in GRC

You can add tags to virtually any type of record defined in GRC applications that reference GRC content packs, integrations, use case accelerators, or any new regulations that use those records. After the records have been tagged, you can filter the content reference tags to identify which records are used within each application.

For example, you can tag all SOX control objectives that are scoped for the NIST RMF integration. You can also create reports that show relevant records that are tagged for specific integrations, use case accelerators, and so forth.

After records have been tagged, you can access all of the content references used within a specific GRC application by viewing the Content References module under each. In Policy and Compliance, for example, you can view all tagged records for the GDPR DPIA use case accelerator in a series of related lists.

![Content reference list](../image/content-reference-list.png "Content reference list")

After selecting GDPR DPIA, a series of related lists show all records tagged with content references to the GDPR DPIA Use Case Accelerator.

![Content references for GDPR DPIA](../image/content-reference-gdpr.png "Content references for GDPR DPIA")

## Records you can tag with content references

In the GRC Audit Management, Policy and Compliance Management, and Risk Management applications, you can tag any of the following types of records.

**Note:** Not all of these records are available within each of the GRC applications listed above The related lists displayed in each of the applications, however, include all of the record types regardless of whether they are available.

-   Authority Documents
-   Citations
-   Control Objectives
-   Controls
-   Engagements
-   Entity Types
-   Entities
-   Indicator Templates
-   Indicators
-   Metric Types
-   Dashboards
-   Policies
-   Policy Exceptions
-   Reports
-   Risk Frameworks
-   Risk Statements
-   Risks
-   Test Plans
-   Test Templates

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

## Add content reference tags to records

As you are analyzing any of the many types of records available in GRC applications, it is easy to add a content reference tag so the record can be included when you perform searches for records associated with a given integration, content pack, use case accelerator, and so forth.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Policy and Compliance** &gt; **Policy Exceptions** &gt; **My Policy Exceptions**, and open a specific policy exception record.

    If you are already working within a specific GRC application, open the record to which you want to add a content reference tag. Otherwise, navigate to the record.

    **Note:** For the sake of example, a Policy Exception record is used to illustrate how to add a content reference to a GRC record.

    ![Content reference related list in a policy exception record](../image/content-reference-policy-excp.png)

2.  Scroll down and click the **Content References** related list.

    ![Content References related list with New and Edit buttons](../image/content-reference-policy-excp-new.png)

3.  Click **Edit**.

    ![Sluchbucket for adding content reference tags](../image/content-reference-slushbucket.png)

4.  Click **Save**.

    Move the integrations, use case accelerators, and so forth to which you want to associate with this policy exception record from the **Collection** box to the **Content References List**, then click **Save**. In this example, policy exception record PER0000105 has been tagged as being associated with the NIST RMF Use Case Accelerator.

    ![Policy exception record tagged for GDPR DPIA use case accelerator](../image/content-reference-policy-excp-tag-added.png)

5.  Navigate to the **Content References** module under that application and select the associated use case accelerator.

    To view all records tagged for a specific use case accelerator within a specific GRC application, For example, to see all records tagged with content references in Risk Management for the SOX content pack, navigate to **Risk** &gt; **Administration** &gt; **Content References**, and click **SOX**.

    ![Records tagged as content references to SOX](../image/content-reference-sox.png)

6.  Click any of the related lists that show a number to see the records tagged as content references for SOX.


## Create content reference tags

You can define new content reference tags, as needed, to accommodate new regulations as they arise. You can define new tags in any GRC application, and they are then available in all GRC applications.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to the Content References module in any GRC application.

    For example, you can navigate to **All** &gt; **Audit** &gt; **Administration** &gt; **Content References**

    ![Content references included in base system](../image/content-reference-oob-tags.png)

2.  Click **New**.

    ![Content Reference new record](../image/content-reference-new-record.png)

3.  Provide a **Name**, **Version** number, and **Description** for the new tag.

    **Note:** The **Version** number can be the software version released from the ServiceNow Store

4.  Click **Submit**.

    The new content reference tag is added to the list and is available from the Content Reference module in the GRC Audit Management, Policy and Compliance Management, and Risk Management applications.


