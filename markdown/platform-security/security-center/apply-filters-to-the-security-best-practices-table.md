---
title: Filters the security best practices table
description: Apply filters to return more relevant results for your security best practices.Discover the steps for saving filters in your security best practices for later reuse.Discover the steps for using the filters that you saved for your security best practices.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security Best Practices, Security posture console, Security Center, Platform Security]
---

# Filters the security best practices table

Apply filters to return more relevant results for your security best practices.

## Before you begin

Role required: admin

## Procedure

1.  Access Security Best Practices Manager by selecting **All** on your ServiceNow instance and entering best practice.

2.  Navigate to the **Best Practices** table and select a field you want to apply a filter to by selecting its kebab menu, or the one with three vertical dots \(![vertical dots](../../../reuse/icons/product-icons/ellipsis-vertical-fill-24.svg)\).

<table id="choicetable_k12_2fy_cbc"><thead><tr><th align="left" id="d139749e74">

Fields

</th><th align="left" id="d139749e77">

Filter

</th></tr></thead><tbody><tr><td id="d139749e83">

**Name**

</td><td>

Combine a conditional operator with a string of text to return security best practices that match the name you entered.

</td></tr><tr><td id="d139749e92">

**Maturity level**

</td><td>

Apply a filter to return security best practices that match one or more of the following maturity levels:

 -   Build a foundation
-   Enhance the experience
-   Optimize the functionality
-   Add advanced features


</td></tr><tr><td id="d139749e119">

**Status**

</td><td>

Apply a filter to return security best practices that match one or more of the following statuses:

 -   Empty
-   Open
-   In progress
-   Completed


</td></tr><tr><td id="d139749e146">

**Priority**

</td><td>

Apply a filter to return security best practices that match the following priorities:

 -   Empty
-   Immediate
-   Later
-   Not applicable


</td></tr><tr><td id="d139749e174">

**Goals**

</td><td>

Apply a filter to return security best practices that match one or more of the following goals:

 -   Address initial security configurations
-   Keep instances up to date
-   Manage access controls
-   Monitoring logs
-   Protect with encryption
-   Secure emails
 **Note**: Advanced filters are applied for goals by default. To modify them, select **Make changes** &gt; **Advanced view** &gt; **Select field goals** and then build the rest of the conditions and select **Update**.

</td></tr><tr><td id="d139749e228">

**First introduced**

</td><td>

Combine a conditional operator with a string of text to return best practices that were first introduced with the version you entered.

</td></tr><tr><td id="d139749e237">

**Changed**

</td><td>

Combine a conditional operator with a string of text to return security best practices that changed in the version you entered.

</td></tr><tr><td id="d139749e246">

**Removed**

</td><td>

Combine a conditional operator with a string of text to return security best practices that were removed in the version you entered.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Best Practices](../concept/security-best-practices-manager.md)

## Save a filter for future use

Discover the steps for saving filters in your security best practices for later reuse.

### Before you begin

Role required: none

### About this task

After you create filters in the security best practices table, you can save them for use the next time you authenticate into your instance. If you want more flexibility on the type of filters you can create, you can apply an advanced filter.

### Procedure

1.  Select the Show filter \(![filter icon](../../../reuse/icons/product-icons/filter-outline-24.svg)\) panel icon.

2.  In the **Filter** dialog panel, scroll down and select **Advanced view**.

3.  Build a filter by adding conditions that contain a field, operator, and values.

4.  Select **Save filter**

5.  Enter the Filter name.

6.  Select a permission.

7.  Select **Save**.

8.  Select **Update** to apply the saved filter to the security best practices table.


## Use a saved filter

Discover the steps for using the filters that you saved for your security best practices.

### Before you begin

Role required: none

### About this task

After you log out of your instance your filters are reset to the default settings. The following steps show how to retrieve a saved filter so that you can reapply it on the security best practices table.

### Procedure

1.  Select the Show filter panel \(![filter icon](../../../reuse/icons/product-icons/filter-outline-24.svg)\) icon.

2.  In the Filter dialog box, scroll down and select **Advanced view**.

3.  Select **Use existing filter**, and then select a saved filter from the dropdown list.

4.  Select **Update** to apply the saved filter.


