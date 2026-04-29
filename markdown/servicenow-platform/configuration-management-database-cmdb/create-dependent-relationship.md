---
title: Create dependent relationship rules
description: Create hosting and containment rules \(dependent relationship rules\) for CI classes to help with correctly identifying dependent CIs during the business discovery process and service mapping. Discovery calls the identification API that applies dependent relationship rules.Use the CI Class Manager to create a basic dependent relationship rule \(hosting or containment relationship rule\) for a CMDB class.Create containment rule for CIs to help with correctly identifying dependent CIs during the business discovery process and service mapping. Discovery calls the identification API that applies dependent relationship rules.Create hosting rule for CIs to assist in correctly identifying dependent CIs during the business discovery process and service mapping. Discovery calls the identification API that applies dependent relationship rules.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [dependent relationship, dependent rules, hosting rule, containment rule]
breadcrumb: [CMDB dependent relationship rules, Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create dependent relationship rules

Create hosting and containment rules \(dependent relationship rules\) for CI classes to help with correctly identifying dependent CIs during the business discovery process and service mapping. Discovery calls the identification API that applies dependent relationship rules.

You can create a basic hosting or containment rule in the CI Class Manager. Or, use the Metadata Editor to create groups of hosting and containment rules, and inbound or outbound endpoints in containment rules. The CI Class Manager and the Metadata Editor are synchronized, and you can use each of those tools to display and edit a dependent rule.

**Parent Topic:**[CMDB dependent relationship rules](c_ServiceRulesMetadata.md)

## Create a dependent relationship rule for a CMDB class

Use the CI Class Manager to create a basic dependent relationship rule \(hosting or containment relationship rule\) for a CMDB class.

### Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin have full access.

### About this task

The class for which you create dependent relationship rule, must have a [dependent identification rule](c_IdentificationRules.md).

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Click **Hierarchy** to display the CI Classes list, and select the class for which you want to create a hosting or a containment rule.

3.  In the class navigation bar, click **Dependent Relationships**.

4.  In the Dependent Relationships view, click **Add dependency**.

5.  Fill out the details in the Add Dependent Relationship Rule dialog box.

    |Field|Description|
    |-----|-----------|
    |Rule Type|Designation of whether this rule is a hosting rule or a containment rule.|
    |This Class|The class that the rule applies to.|
    |Relationship|The relationship type for the rule.|
    |Target Class|The target class for the dependent relationship rule. The designation of this class as a child or parent class, is based on the specified **Relationship**.|

6.  Click **Save**.


### What to do next

You can click **Reset to derived** and then confirm the operation to delete all dependent relationship rules that were added specifically for the selected class. Only dependent relationships that are derived from a parent class, remain.

For more information about child and parent classes, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Create or edit a collection of containment rules

Create containment rule for CIs to help with correctly identifying dependent CIs during the business discovery process and service mapping. Discovery calls the identification API that applies dependent relationship rules.

### Before you begin

Role required: sn\_cmdb\_admin or admin

### About this task

A containment rule is a dependent relationship rule which defines a relationship between two CIs, structured as: CIType1 RelationshipType CIType2. The first CI type that you add becomes the top level CI of a containment rules group which is a chain of containment rules. The entire set of containment rules is organized as groups according to top-level CIs.

To create a containment rules group for a new CI type, you need to first add the CI Type1 of the relationship. To add a child containment rule for a CI type that exists, you need to select that CI type, and define the second portion of the relationship rule which is the relationship type and CI Type2.

To each rule within a containment rules group you can add inbound or outbound endpoints, which are noted by blue up and down arrows. After adding an endpoint, you can not add a containment rule in that branch of the containment rules hierarchy.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Metadata Editor**.

2.  In the Metadata Editor, click the **Containment Rules** tab.

3.  Click **Add New Rule** to add a top-level rule or point to a rule for which you want to add a child rule and click the green '+' icon that appears on the right.

4.  Complete the **Add Containment Rule to &lt;class&gt;** form.

    |Field|Description|
    |-----|-----------|
    |Configuration Item Type|The CI class that the rule applies to.|
    |Relationship Type|The relationship type for the rule.|
    |Reverse Relationship Direction|Enable to use the reverse relationship in the rule.|
    |Always include in Service Model|Enable to always include the CIs of the specified class in the Service Map if their parent CI \(based on the containment relationship\) is present in the Service Map.|

5.  Click **Create**.

6.  Add an endpoint to a child rule:

    1.  Point to a child rule for which you want to add an endpoint.

    2.  Click the blue "+" icon that appears on the right.

    3.  Complete the **Add Endpoint To &lt;class&gt;** form.

        |Field|Description|
        |-----|-----------|
        |Endpoint Type|The type of endpoint.|
        |Inbound or Outbound|The direction of the endpoint.|

    4.  Click **Create**.


## Create or edit a collection of hosting rules

Create hosting rule for CIs to assist in correctly identifying dependent CIs during the business discovery process and service mapping. Discovery calls the identification API that applies dependent relationship rules.

### Before you begin

A hosting rule is a dependent relationship rule which defines a relationship between two CIs, structured as: &lt;CI Type1&gt; &lt;relationship type&gt; &lt;CI Type2&gt;. To create a hosting rule, you need to add a CI type as &lt;CI Type1&gt; in the relationship rule, and then define the second portion of the relationship rule which is the relationship type and &lt;CI Type2&gt;. The entire set of hosting rules is organized as groups according to the top-level hosted CIs.

A hosting rule implicitly contains two rules, which are the reversal of each other. When you create the rule '&lt;CI Type1&gt; &lt;relationship type&gt; &lt;CI Type2&gt;', the rule '&lt;CI Type2&gt; &lt;reversed relationship type&gt; &lt;CI Type1&gt;' is automatically added.

Role required: sn\_cmdb\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Metadata Editor**.

2.  In the Metadata Editor, click the **Hosting Rules** tab.

3.  Click **Add New Rule** to add a top-level rule or point to a rule for which you want to add a child rule and click the green '+' icon that appears on the right.

4.  Complete the **Add Hosted/Hosting Rule to &lt;class&gt;** form.

    |Field|Description|
    |-----|-----------|
    |Configuration Item Type|The &lt;CI Type2&gt; in the rule.|
    |Relationship Type|The relationship type for the rule.|
    |Reverse Relationship Direction|Check to reverse relationship in the rule.|

5.  Click **Create**.


