---
title: Configure the Spending Overview Widget and Filter pills
description: Use script includes to configure the Spending Overview widget and filter pills on the Funding Allocation tab for the rolling grant approvals feature. Admins can add, remove, relabel, and reorder chart widgets and filter pills, and create custom ones to match program requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-gm-config-spending-overview-widget.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
keywords: [Configure funding allocation charts, Spending Overview widget, filter pills, Funding Allocation tab, UI Builder, grants management configuration]
breadcrumb: [Set up a grant program, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the Spending Overview Widget and Filter pills

Use script includes to configure the **Spending Overview** widget and filter pills on the **Funding Allocation** tab for the rolling grant approvals feature. Admins can add, remove, relabel, and reorder chart widgets and filter pills, and create custom ones to match program requirements.

## Before you begin

The **Spending Overview** widget and filter pills are available on the **Funding Allocation** tab starting with Grants Management version 1.31. Verify that the grant program is open and in an active state before making configuration changes. For information about using script includes, see [Use script includes](https://www.servicenow.com/docs/r/zurich/api-reference/scripts/c_ScriptIncludes.html?section=c_UseScriptIncludes).

Role required: admin

## About this task

The **Spending Overview** widget is a UI Builder component on the **Funding Allocation** tab. It contains two built-in chart areas: **Overall Spending** and **Decisions in Progress**. You can add custom chart widgets to the panel alongside the built-in charts.

The filter pills appear in the **Proposals** tab under the **Scored Proposals** list. They provide quick-access views by proposal status. The default filter pills are:

-   **All**
-   **Undecided**
-   **Marked**
-   **Pending approval**
-   **Returned**
-   **Decided**

You can relabel, reorder, add, remove, or create custom filter pills with custom filter conditions by configuring the `FundingAllocationUtil` and `FundingAllocationUtilImpl` script includes.

You can also use UI Builder to configure the Funding allocation tab widgets of the Grants management playbook. In UI Builder, navigate to **Page collections** &gt; **Grant Program Record Page Collection** and select the **Funding allocation** page. Configure the values in the **Funding allocation review task record page** and the **Funding allocation tab page**. For more information, see [Working in UI Builder](https://www.servicenow.com/docs/r/application-development/ui-builder/using-ui-builder.html).

## Procedure

1.  Navigate to **All** &gt; **Activity subscriptions** &gt; **Administration** &gt; **Script Includes**.

2.  Open the `FundingAllocationUtilImpl` script include.

3.  Configure the values by overriding the methods and add them to the `FundingAllocationUtil` script.

4.  Select **Save** to apply your changes.

    Once you reload the page, the **Funding Allocation** tab reflects the updated widget layout and filter pill configuration for all users with access to the grant program workspace.


## What to do next

To verify the configuration, open a grant program record and select the **Funding Allocation** tab. Confirm that the **Spending Overview** widget and filter pills display as configured.

**Parent Topic:**[Set up a grant program in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-grant-pgr.md)

**Previous topic:**[Configure a merit review scoring rubric for a grants proposal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-create-rubric.md)

**Next topic:**[Configuring Investigative Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-investigative-case-management.md)

