---
title: Retail release notes
description: The ServiceNow retail applications streamline frontline operations and customer experiences. See the following sections for release notes by version.Store associates and managers can view and act on the Strategic Portfolio Management project work behind a store opening, closing, renovation, or relocation without leaving Retail.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/retail-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-15"
reading_time_minutes: 3
keywords: [SPM-RO Better Together, OCRR, App SPM Retail]
breadcrumb: [Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Retail release notes

The ServiceNow® retail applications streamline frontline operations and customer experiences. See the following sections for release notes by version.

## About Retail

-   Enable HQ users and regional managers to create operational store plans involving cases and tasks for multiple stores through a guided, streamlined user experience.
-   Schedule and manage recurring tasks such as daily store opening procedures with parent cases for store-level tracking.
-   Fulfillment of store case and task for regional managers and store teams through Retail mobile app.
-   Let store associates and managers view and act on the Strategic Portfolio Management project work behind a store opening, closing, renovation, or relocation, without leaving the Retail application.

See [Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-operations-overview.md) for more information.

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    The ServiceNow ® Customer Service Management \(CSM\) application provides the foundation for the Retail Core application. Leverage the functionality of CSM applications to provide support to customers as well as retail sites.

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/fsm-application-landing-page.md)**

    The ServiceNow ® Field Service Management application aligns with Retail Core by providing capabilities such as work orders for use by each retail location that uses the Retail Core application.


## Activation and other requirements

**Important:** Retail is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install the Retail applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/new-features-changes.md)

## September 2026 store release

Store associates and managers can view and act on the Strategic Portfolio Management project work behind a store opening, closing, renovation, or relocation without leaving Retail.

### What's new

-   **SPM-RO Better Together**

    SPM-RO Better Together surfaces Customer Service Management and Strategic Portfolio Management project data inside Retail. Store personas can browse the store opening, closing, renovation, and relocation \(OCRR\) projects for their store, drill into individual project tasks, and assign, take, or close those tasks.

    The experience is available in the Retail Service Portal and in Retail Mobile. It is a consumption layer over the CSM/SPM project tables — Retail adds no tables, roles, or access control rules of its own, and project visibility remains governed by the CSM/SPM access control layer.

-   **Track Plan dashboard**

    Track the progress of a store plan in a single view from the **Track Plan** tab of a plan. The plan progress summary shows the percentage of store cases closed and the number of open, overdue, closed, and all store cases for the selected occurrence, and you can filter the summary by occurrence. Select a metric to open the matching list of cases.

    The hierarchical list view provides a navigation tree of the cases and tasks in a plan, with **Open**, **Overdue**, **Closed**, and **All** tabs. The tree is plan-type agnostic and adapts to current and future plan types, including the plan types that you configure. The plan progress summary applies to the base-system HQ Communications and Store Audit plan types. Plan types with custom configurations or custom case or task states might require additional configuration.


### What's changed

-   **Template item column for store plan cases**

    New cases that are created from a store plan or a store audit plan will populate the **Template item** column, while the **Origin** field will no longer be populated for newly created cases.

    **Note:** If you have a custom implementation that relies on the **Origin** field to determine the template item that a case was created from, those use cases will need to be updated accordingly.


### Plugin information

-   **New plugins**

    App SPM Retail \(com.snc.spm\_retail\): Enables the SPM-RO Better Together experience. When this plugin is not active, the OCRR project and task surfaces do not appear in the Retail Service Portal or Retail Mobile, and there is no separate setting to turn the feature on or off.


