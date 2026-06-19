---
title: Define the authorization boundary
description: An authorization boundary defines the scope of a particular system that can be continuously managed and monitored using the CAM application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/continuous-risk-monitoring/define-auth-boundaries.html
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-10-05"
reading_time_minutes: 1
breadcrumb: [RMF step 0 - Prepare the authorization package, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Define the authorization boundary

An authorization boundary defines the scope of a particular system that can be continuously managed and monitored using the CAM application.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner or sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **All Authorization Boundaries**.

    \[Omitted image "cam-auth-boundaries.png"\] Alt text: All authorization boundaries

2.  Select **New** and then fill in the form.

    The settings are described in [Fields on the Authorization Boundary form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/continuous-risk-monitoring/cam-form-authorization-boundary.md).

    \[Omitted image "cam-auth-boundaries-classic.png"\] Alt text: Authorization boundary - new record

3.  Save the record.

    Use the tabs that appear to identify which systems and parts of systems you own and should go through the authorization process.



    \[Omitted image "cam-filters-classic.png"\] Alt text: Boundary tabs

4.  You can use the **Boundary Filters** tab to create filters for identifying all of your system elements.

    After running the filters, the results appear in the **System Elements** tab.

5.  If elements appear that should not be included in the authorization process, you can select them, and select **Delete** from the **Actions on selected rows** list at the bottom of the screen.

6.  You can select **New** to include additional assets or systems to the list of system elements in the authorization boundary.


## What to do next

This completes the procedure for defining the authorization boundary. The next step is to create the authorization package that will be processed through approvals. You can initiate the process by clicking the **Authorization Packages** tab or via the navigation pane. For details, see [Create an authorization package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/continuous-risk-monitoring/create-auth-package.md).

**Parent Topic:**[Risk Management Framework \(RMF\) step 0 - Prepare the authorization package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/continuous-risk-monitoring/prepare-auth-pkg.md)

