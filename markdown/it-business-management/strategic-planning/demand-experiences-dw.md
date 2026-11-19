---
title: Demand experiences
description: A demand experience defines a governance process and controls which form view, modules, and dynamic attributes appear on a demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/demand-experiences-dw.html
release: brazil
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 4
breadcrumb: [Manage demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Demand experiences

A demand experience defines a governance process and controls which form view, modules, and dynamic attributes appear on a demand.

Demands support EWD in two complementary ways: partitioning, which controls who can see a demand, and demand experiences, which control what a demand looks like to users who can see it. For the full EWD concept, including partitions for SPM tables, see [Exploring SPM Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/explore-ewd.md).

A demand experience controls the fields, modules, and layout a demand shows for a given governance process, such as Marketing or IT.

The following demand-record behaviors depend on a demand's experience:

-   Modules available for a given demand experience
-   Form layout for a given demand experience
-   Dynamic fields when a demand experience has a dynamic category with configured dynamic attributes

Different teams often need different governance processes for their demands. For example, a marketing team and an IT team may each need their own set of fields, modules, and layout. Each team captures the information that's relevant to their process. You can use a demand experience record to define one governance process, such as Marketing or IT. After a demand experience is set on a demand, it can't be changed or cleared.

The base system includes a Default demand experience for the Demand \[dmn\_demand\] table. The Default experience enables all demand modules and has no dynamic category. Demands, including existing demands, aren't automatically assigned the Default experience. A demand without a demand experience also enables all demand modules. Each enabled module still appears only for users who meet its role conditions. For more information, see [Create a demand experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-a-demand-experience-dw.md).

## Personas

|Role|Function|
|----|--------|
|EWD admin role \[sn\_spm\_ewd.ewd\_admin\]|Creates and manages demand experiences.|
|System admin role \[admin\]|Creates dynamic categories from SPM Dynamic Categories.|
|PPS admin role \[pps\_admin\]|Creates and manages demand experiences: selects the table, form view, optional dynamic category, and which modules are enabled.|
|Demand user role \[it\_demand\_user\]|Creates and views demands. On a demand record, accesses the modules enabled for that demand's experience and, when applicable, the **Additional Information** tab with its dynamic attributes.|

## Dynamic category

A demand experience can optionally reference a dynamic category. The dynamic category defines the set of dynamic attributes that are relevant to that governance process. Only an administrator can create a dynamic category. When a demand experience with a dynamic category is selected on a demand, any dynamic attributes configured on that category are available on the demand. When a demand experience includes dynamic attributes, the demand record displays an **Additional Information** tab in Details page that shows those fields.

A dynamic category belongs to the `Default SPM Dynamic Namespace` and groups the dynamic attributes that appear on demand records of that experience. Dynamic attributes are scoped to a specific experience and don't appear on records of other experiences or affect default fields.

-   A dynamic category can have a parent category. A child category inherits the attributes of its parent, so you can define shared fields once and add experience-specific fields in each child category.
-   Dynamic attributes support the String, Boolean, Date, Date/Time, Integer, Decimal, Floating point, Choice, and Reference data types.

For more information, see [Create a dynamic category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-a-dynamic-category-dw.md).

## Form view precedence

Saving a demand experience automatically creates its view rule and workspace view rule. A demand's form view can be determined by more than one view rule \[sysview\_rule\] record. When more than one view rule applies, the rule with the lower execution order takes effect. When a demand experience's view rule is in effect, users can't change the view themselves.

## Additional Information tab

The demand record page in Next Experience for Demand Management can display a conditional **Additional Information** tab that shows a demand's dynamic attributes. The tab is displayed when both of the following are true:

-   The demand has a dynamic category from its selected demand experience.
-   That dynamic category has one or more dynamic attributes defined.

If the demand has no dynamic category, or a category with no dynamic attributes, the **Additional Information** tab isn't displayed. The tab shows the configured dynamic attributes as editable fields, and the values that you enter are saved to the demand. For more information, see [Add dynamic attributes to a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/add-dynamic-attributes-to-a-demand-dw.md).

**Related topics**  


[Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-demand-from-dw.md)

[Add dynamic attributes to a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/add-dynamic-attributes-to-a-demand-dw.md)

