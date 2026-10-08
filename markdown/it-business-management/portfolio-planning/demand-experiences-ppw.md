---
title: Demand experiences
description: A demand experience defines a governance process and controls which form view, modules, and dynamic attributes appear on a demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/demand-experiences-ppw.html
release: brazil
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 2
breadcrumb: [EWD for demands, Explore, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Demand experiences

A demand experience defines a governance process and controls which form view, modules, and dynamic attributes appear on a demand.

Different teams often need different governance processes for their demands. For example, a marketing team and an IT team may each need their own set of fields, modules, and layout. Each team captures the information that's relevant to their process. You can use a demand experience record to define one governance process, such as Marketing or IT. The experience controls the form view, modules, and dynamic attributes that appear on each demand that uses it.

A demand experience can optionally reference a dynamic category. The dynamic category defines the set of dynamic attributes that are relevant to that governance process. Only an administrator can create a dynamic category. When a demand experience with a dynamic category is selected on a demand, any dynamic attributes configured on that category are available on the demand.

## Dynamic category

A dynamic category defines the custom fields for a specific demand experience. It belongs to the `Default SPM Dynamic Namespace` and groups the dynamic attributes that appear as custom fields on demand records of that experience. Custom fields are scoped to a specific experience and don't appear on records of other experiences or affect default fields.

-   A dynamic category can have a parent category. A child category inherits the attributes of its parent, so you can define shared fields once and add experience-specific fields in each child category.
-   Custom fields support the String, Boolean, Date, Date/Time, Integer, Decimal, Floating point, Choice, and Reference data types.
-   Demand managers view and update custom fields in Demand Management.

For more information, see [Create a dynamic category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-planning/create-a-dynamic-category-ppw.md).

## Form view precedence

Saving a demand experience automatically creates its view rule and workspace view rule. A demand's form view can be determined by more than one view rule \[sysview\_rule\] record. When more than one view rule applies, the rule with the lower execution order takes effect. When a demand experience's view rule is in effect, users can't change the view themselves.

## Additional Information tab

The demand record page in Next Experience for Demand Management can display a conditional **Additional Information** tab that shows a demand's dynamic attributes. The tab is displayed when both of the following are true:

-   The demand has a dynamic category from its selected demand experience.
-   That dynamic category has one or more dynamic attributes defined.

If the demand has no dynamic category, or a category with no dynamic attributes, the **Additional Information** tab isn't displayed. The tab shows the configured dynamic attributes as editable fields, and the values that you enter are saved to the demand. For more information, see [Add dynamic attributes to a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-planning/add-dynamic-attributes-to-a-demand-ppw.md).

**Related topics**  


[Enterprise-Wide Deployment for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-planning/ewd-for-demands-ppw.md)

[Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-planning/create-a-demand-ppw.md)

