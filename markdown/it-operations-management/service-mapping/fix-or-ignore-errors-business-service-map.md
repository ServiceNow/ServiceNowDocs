---
title: Fix errors in individual application service maps
description: You can address discovery issues in each application service map individually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/fix-or-ignore-errors-business-service-map.html
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

\[Omitted image "SMMapFlowReviewFix.png"\] Alt text: Fixing errors in individual application services as part of the Service Mapping workflow

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Ensure that the map opens in Edit mode.

    \[Omitted image "MapEditDiscoveryMessages.png"\] Alt text: Discovery messages appear under the map.

    CIs discovered with errors appear with the warning icon \(\[Omitted image "MapWarningIcon.png"\] Alt text: The Warning icon\) on the map. Discovery messages on the **Discovery Messages** tab give short error descriptions.

3.  Group errors by types by clicking **Group Errors**.

    The discovery error messages on the **Discovery Messages** tab appear grouped by predefined types, error codes.

4.  To review and fix an error from the list, click **Handle Error** next to the error description.

    Or

5.  To review the first error in the largest error group, click **Handle Next Error** at the left top corner of the map.

6.  To learn how to resolve the error, click **Open instructions** under **Action on Selected** in the right pane.

    **Note:** Instructions are available only for the most common errors.

7.  Click the relevant semi-automated resolution option to resolve the error under **Action on Selected** in the right pane.

    Error resolution options vary, because they depend on the specific discovery error associated with the selected CI.

<table id="choicetable_phf_4qd_41b"><thead><tr><th align="left" id="d480844e244">

Use this option

</th><th align="left" id="d480844e247">

To do this

</th></tr></thead><tbody><tr><td id="d480844e253">

**Add Management IP**

</td><td>

Enter the management IP to trigger discovery on the host resources and connections. Typically, you need this solution for application services that have undiscovered devices like load balancers as their entry points. The management IP address of a network device is the address that you use to reach the device using the SNMP or any other management protocol.**Note:** The system does not save the management IP you configure.

</td></tr><tr><td id="d480844e265">

**Create new WMI credentials**

</td><td>

Open the Windows Credentials form and configure missing Windows credentials for the selected CI. See [Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_WindowsCredentialsForm.md).

</td></tr><tr><td id="d480844e278">

**Create new SSH credentials**

</td><td>

Open the SSH Credentials form and configure missing SSH credentials for the selected CI. See [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_SSHCredentialsForm.md).

</td></tr><tr><td id="d480844e291">

**Create new SSH private key**

</td><td>

Open the SSH private keys form and configure missing credentials for the selected CI. See [SSH private key credential type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_SSHCredentialsForm.md).

</td></tr><tr><td id="d480844e305">

**Create new SNMP credentials**

</td><td>

Open the SNMP credentials form and configure missing SNMP credentials for the selected CI. See [SNMP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_SNMPCredentials.md).

</td></tr><tr><td id="d480844e318">

**Show Discovery Log**

</td><td>

See the log to understand at what stage an error occurred and what caused it.

</td></tr><tr><td id="d480844e327">

**Skip and resume**

</td><td>

Manually add the CI whose discovery failed and configure attributes of the entry point from which Service Mapping continues discovery. For more information, see [Skip errors to continue discovering an application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/skip-errors-continue-discovery-individual-services.md).

</td></tr><tr><td id="d480844e350">

**Retry discovery**

</td><td>

Run the discovery process for the selected CI after trying to resolve a discovery error associated with it.

</td></tr><tr><td id="d480844e359">

**View affected services**

</td><td>

Display a list of all services affected by the selected error. In the list, click a service to view service details.

</td></tr></tbody>
</table>8.  If there are no instructions or semi-automated resolution options available, [fix errors based on symptoms and discovery messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/fix-errors-by-discovery-messages.md).

9.  To ignore an irrelevant error, right-click its error message on the **Discovery Messages** tab and select `Toggle Ignore State`.

    The ignored error disappears from the map and from the list of discovery error messages.

    **Note:** If necessary, you can still display ignored errors by switching on the **Include Ignored Errors** option under **More Options** menu. For more info, see [Modify view for an application service map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/modify-map-view.md).

10. Click **Handle Next Error** to review the next error in the largest error group.

11. When finished reviewing and handling errors, click anywhere in the map to close the **Resolve Error** pane.


## What to do next

If you resolved most errors, [send the service instance for review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/send-business-service-for-review.md).

-   **[Fix errors in individual application services using discovery messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/fix-errors-by-discovery-messages.md)**  
Service Mapping does not offer semi-automated resolution options for errors that require advanced resolution. Fix such errors using symptoms and discovery messages.
-   **[Skip errors to continue discovering an application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/skip-errors-continue-discovery-individual-services.md)**  
If you know what configuration items \(CIs\) and connections make up your service instance, you can enable Service Mapping to continue discovery of the service instance even if there are some errors. You can skip errors to troubleshoot later so you can complete mapping most of the service instance, even if some CIs are missing.
-   **[Resolve pattern-related mapping errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_TBSMapProcess.md)**  
You can troubleshoot mapping errors caused by patterns.

**Parent Topic:**[Application service mapping using classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping]()

[Map application services using tags with classic Service Mapping]()

[Map multiple application services from a CSV file using classic Service Mapping]()

[Map a single application service using classic Service Mapping]()

[Fix application service errors in bulk]()

[Review and approval of application service maps]()

[Fine-tune application services to implement owner requests]()

[Application service completion]()

[Application service analysis and maintenance using classic Service Mapping]()

[Prerequisites for performing top-down discovery using Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/prerequisites-service-mapping.md)

