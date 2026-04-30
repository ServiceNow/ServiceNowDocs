---
title: Install ServiceNow Voice applications
description: You can install the ServiceNow Voice applications if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Install ServiceNow Voice applications

You can install the ServiceNow Voice applications if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Your organization must have purchased a license for a ServiceNow application, such as ITSM or CSM, which includes the ServiceNow Voice SKU.
-   You should install at least one content pack, for example, CSM or ITSM.

Role required: admin

## About this task

The following ServiceNow Voice applications should be installed.

<table id="table_fmc_lzj_5mb"><thead><tr><th>

Application

</th><th>

Description

</th><th>

Components installed

</th></tr></thead><tbody><tr><td>

ServiceNow Voice\[sn\_cti\_core\]

</td><td>

Provides the framework that supports the integration with your third-party phone system.

</td><td>

For information about the components installed with this application, see [Components installed with ServiceNow Voice Core](../reference/instld-with-cloud-call-center.md).

</td></tr><tr><td>

ServiceNow Voice with Amazon Connect \[sn\_cti\_amzn\_cct\]

</td><td>

Integrates Amazon Connect with ServiceNow Voice Core.

</td><td>

For information about the components installed with this application, see [Components installed with Amazon Connect Integration with ServiceNow Voice](../reference/instld-with-amazn-cnct-integ.md).

</td></tr><tr><td>

ServiceNow Voice UI Components\[sn\_cti\_ux\]

</td><td>

Enables call recording, transcription, and sentiment analysis for ServiceNow Voice with Workspace experience.

</td><td>

None

</td></tr><tr><td>

ServiceNow Real Time Transcription\[sn\_cti\_amzn\_cct\]

\(Available for ServiceNow Voice for Customer Service Management only.\)

</td><td>

Enables real-time call transcription so that the agent can see the call transcript while on a call with the customer.

</td><td>

\[sn\_cti\_csm\_cnt.enable\_ims\_update\]

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find these applications using the filter criteria and search bar.

    -   ServiceNow Voice \(sn\_cti\_core\)
    -   ServiceNow Voice with Amazon Connect \(sn\_cti\_amzn\_cct\)
    -   ServiceNow Voice UI Components \(sn\_cti\_ux\)
    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install the Voice applications.

    -   ServiceNow Voice \(sn\_cti\_core\)
    -   ServiceNow Voice with Amazon Connect \(sn\_cti\_amzn\_cct\)
    -   ServiceNow Voice UI Components \(sn\_cti\_ux\)
    For the complete Voice experience, install ServiceNow Voice for ITSM or ServiceNow Voice for CSM applications. For information about these installations, see [Install ServiceNow Voice for ITSM](install-ccc-itsm.md) and [Install ServiceNow Voice for CSM](install-ccc-csm.md).

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Setting up ServiceNow Voice](../concept/ccc-setup.md)

