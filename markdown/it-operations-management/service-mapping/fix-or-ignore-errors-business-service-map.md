---
title: Fix errors in individual application service maps
description: You can address discovery issues in each application service map individually.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Fix errors in individual application service maps

You can address discovery issues in each application service map individually.

## Before you begin

Role required: service\_mapping\_admin

## About this task

You can fix errors in individual application services at any time. When you perform initial mapping of application services in your organization, you typically fix errors in individual application services after resolving errors in multiple services, in bulk. You may also need to fix errors in an approved and completed application service at a later stage.

![Fixing errors in individual application services as part of the Service Mapping workflow](../image/SMMapFlowReviewFix.png "Service Mapping workflow")

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Ensure that the map opens in Edit mode.

    ![Discovery messages appear under the map.](../image/MapEditDiscoveryMessages.png)

    CIs discovered with errors appear with the warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) on the map. Discovery messages on the **Discovery Messages** tab give short error descriptions.

3.  Group errors by types by clicking **Group Errors**.

    The discovery error messages on the **Discovery Messages** tab appear grouped by predefined types, error codes.

4.  To review and fix an error from the list, click **Handle Error** next to the error description.

    Or

5.  To review the first error in the largest error group, click **Handle Next Error** at the left top corner of the map.

6.  To learn how to resolve the error, click **Open instructions** under **Action on Selected** in the right pane.

    **Note:** Instructions are available only for the most common errors.

7.  Click the relevant semi-automated resolution option to resolve the error under **Action on Selected** in the right pane.

    Error resolution options vary, because they depend on the specific discovery error associated with the selected CI.

<table id="choicetable_phf_4qd_41b"><thead><tr><th align="left" id="d458554e244">

Use this option

</th><th align="left" id="d458554e247">

To do this

</th></tr></thead><tbody><tr><td id="d458554e253">

**Add Management IP**

</td><td>

Enter the management IP to trigger discovery on the host resources and connections. Typically, you need this solution for application services that have undiscovered devices like load balancers as their entry points. The management IP address of a network device is the address that you use to reach the device using the SNMP or any other management protocol.**Note:** The system does not save the management IP you configure.

</td></tr><tr><td id="d458554e265">

**Create new WMI credentials**

</td><td>

Open the Windows Credentials form and configure missing Windows credentials for the selected CI. See [Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_WindowsCredentialsForm.md).

</td></tr><tr><td id="d458554e278">

**Create new SSH credentials**

</td><td>

Open the SSH Credentials form and configure missing SSH credentials for the selected CI. See [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md).

</td></tr><tr><td id="d458554e291">

**Create new SSH private key**

</td><td>

Open the SSH private keys form and configure missing credentials for the selected CI. See [SSH private key credential type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md).

</td></tr><tr><td id="d458554e305">

**Create new SNMP credentials**

</td><td>

Open the SNMP credentials form and configure missing SNMP credentials for the selected CI. See [SNMP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_SNMPCredentials.md).

</td></tr><tr><td id="d458554e318">

**Show Discovery Log**

</td><td>

See the log to understand at what stage an error occurred and what caused it.

</td></tr><tr><td id="d458554e327">

**Skip and resume**

</td><td>

Manually add the CI whose discovery failed and configure attributes of the entry point from which Service Mapping continues discovery. For more information, see [Skip errors to continue discovering an application service](skip-errors-continue-discovery-individual-services.md).

</td></tr><tr><td id="d458554e350">

**Retry discovery**

</td><td>

Run the discovery process for the selected CI after trying to resolve a discovery error associated with it.

</td></tr><tr><td id="d458554e359">

**View affected services**

</td><td>

Display a list of all services affected by the selected error. In the list, click a service to view service details.

</td></tr></tbody>
</table>8.  If there are no instructions or semi-automated resolution options available, [fix errors based on symptoms and discovery messages](fix-errors-by-discovery-messages.md).

9.  To ignore an irrelevant error, right-click its error message on the **Discovery Messages** tab and select `Toggle Ignore State`.

    The ignored error disappears from the map and from the list of discovery error messages.

    **Note:** If necessary, you can still display ignored errors by switching on the **Include Ignored Errors** option under **More Options** menu. For more info, see [Modify view for an application service map](modify-map-view.md).

10. Click **Handle Next Error** to review the next error in the largest error group.

11. When finished reviewing and handling errors, click anywhere in the map to close the **Resolve Error** pane.


## What to do next

If you resolved most errors, [send the service instance for review](send-business-service-for-review.md).

-   **[Fix errors in individual application services using discovery messages](fix-errors-by-discovery-messages.md)**  
Service Mapping does not offer semi-automated resolution options for errors that require advanced resolution. Fix such errors using symptoms and discovery messages.
-   **[Skip errors to continue discovering an application service](skip-errors-continue-discovery-individual-services.md)**  
If you know what configuration items \(CIs\) and connections make up your service instance, you can enable Service Mapping to continue discovery of the service instance even if there are some errors. You can skip errors to troubleshoot later so you can complete mapping most of the service instance, even if some CIs are missing.
-   **[Resolve pattern-related mapping errors](t_TBSMapProcess.md)**  
You can troubleshoot mapping errors caused by patterns.

**Parent Topic:**[Application service mapping using classic Service Mapping](../concept/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping](map-business-services-in-bulk.md)

[Map application services using tags with classic Service Mapping](map-service-tag.md)

[Map multiple application services from a CSV file using classic Service Mapping](import-business-services-csv.md)

[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

[Fix application service errors in bulk](fix-bus-serv-errors-by-category.md)

[Review and approval of application service maps](business-service-approval.md)

[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

[Application service completion](../concept/advanced-business-service-definitions.md)

[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

[Prerequisites for performing top-down discovery using Service Mapping](../reference/prerequisites-service-mapping.md)

