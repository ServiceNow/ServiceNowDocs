---
title: SAP products discovery
description: ITOM Visibility can discover SAP applications, SAP HANA Database, and SAP HANA DB Catalog. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.Map a service instance containing an SAP application and verify that Service Mapping discovered all SAP components correctly.Fix basic discovery issues based on the symptoms and discovery messages.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# SAP products discovery

ITOM Visibility can discover SAP applications, SAP HANA Database, and SAP HANA DB Catalog. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about the SAP components and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](../reference/r_SupportedApplications.md).

## Prerequisites

-   **Verify that the applications are up to date**

    Discovery and Service Mapping Patterns

    Visibility Content

    CMDB CI Class Models

-   **Verify the configuration of the credentials**
    -   \(If hosted on a UNIX server\) On the ServiceNow AI Platform, configure [applicative credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/applicative-creds.md) and [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md). The SSH credentials are used to create connections from SAP Central Instance \(CI\) to other applications and devices. In addition, provide the user elevated rights to be able to run commands requiring a privileged user: [Service Mapping commands requiring a privileged user](../reference/r_CommandsnCredentials.md).
    -   \(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_WindowsCredentialsForm.md) to create connections from SAP CI to other applications and devices.
    -   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/enable-winRM-MID-servers.md).
    -   \(Optional for top-down discovery by Service Mapping\) Provide a user with permissions to run SOAP on RFC read table function.
    -   \(Optional for top-down discovery by Service Mapping\) If your organization deploys SAP Digital Business Services using web services and you want to map all connected services, perform the following actions:
        -   Configure applicative credentials for a user with permissions to access the following tables: CVERS, DBCONS, and RFCDES.
        -   Ensure that you have the web service URL. For information on how to create web services, see [https://blogs.sap.com/2012/10/24/how-to-create-web-services-abap-based/](https://blogs.sap.com/2012/10/24/how-to-create-web-services-abap-based/).
-   **SAP HANA 2.0 DB Catalog on UNIX**

    Verify that the Applicative Credentials for **SAP HANA DB App Creds** are configured with **SAP Hana Db \[cmdb\_ci\_appl\_sap\_hana\_db\]** as CI type.

-   **Verify the permissions to run Service Mapping commands**

    [Service Mapping commands not requiring a privileged user](../reference/r_NonSudoCommands.md)

-   **Verify the user has the permissions to run the Patterns queries**

    The following commands are executed when running the SAP HANA DB and SAP HANA DB Catalog Patterns.

    -   `select * from schemas;`
    -   `select * from M_HOST_INFORMATION where upper(KEY) like '%TIMEZONE%';`
    -   `select SCHEMA_NAME, round(sum(TABLE_SIZE) /1024/1024) from M_TABLES GROUP BY SCHEMA_NAME`
<table id="table_nmf_jcg_vzb"><thead><tr><th>

The query type

</th><th>

Fallback commands executed in order

</th></tr></thead><tbody><tr><td>

Schemas Info

</td><td>

1.  `$hdbsql_path + " -n " + $entry_point.ip_address + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select * from schemas;\""`
2.  `$hdbsql_path + " -n " + $ip_address + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select * from schemas;\""`
3.  `$hdbsql_path + " -n " + $server_name + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select * from schemas;\""`
4.  `$hdbsql_path + " -n localhost -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select * from schemas;\""`


</td></tr><tr><td>

Time Zone:

</td><td>

1.  `$hdbsql_path + " -n " + $entry_point.ip_address + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select * from M_HOST_INFORMATION where upper(KEY) like '%TIMEZONE%';\""`
2.  `$hdbsql_path + " -n " + $ip_address + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select * from M_HOST_INFORMATION where upper(KEY) like '%TIMEZONE%';\""`
3.  `$hdbsql_path + " -n " + $server_name + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select * from M_HOST_INFORMATION where upper(KEY) like '%TIMEZONE%';\""`
4.  `$hdbsql_path + " -n localhost -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select * from M_HOST_INFORMATION where upper(KEY) like '%TIMEZONE%';\""`


</td></tr><tr><td>

Disk Size

</td><td>

1.  `$hdbsql_path + " -n " + $entry_point.ip_address + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select SCHEMA_NAME, round(sum(TABLE_SIZE) /1024/1024) from M_TABLES GROUP BY SCHEMA_NAME;\""`
2.  `$hdbsql_path + " -n " + $ip_address + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select SCHEMA_NAME, round(sum(TABLE_SIZE) /1024/1024) from M_TABLES GROUP BY SCHEMA_NAME;\""`
3.  `$hdbsql_path + " -n " + $server_name + ":" + $query_port + " -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select SCHEMA_NAME, round(sum(TABLE_SIZE) /1024/1024) from M_TABLES GROUP BY SCHEMA_NAME;\""`
4.  `$hdbsql_path + " -n localhost -i " + $digits + " -u '$$username$$' -p '$$password$$' \"select SCHEMA_NAME, round(sum(TABLE_SIZE) /1024/1024) from M_TABLES GROUP BY SCHEMA_NAME;\""`


</td></tr></tbody>
</table>-   **Verify the configuration of the Discovery schedule**

    For more information, see [Running discoveries in your network](../../discovery/concept/running-discoveries.md)


## Data collected by Discovery during horizontal discovery

|Table and field|Description|
|---------------|-----------|
|SAP ASCS \[cmdb\_ci\_appl\_sap\_ascs\]|
|Name \[name\]|Data collected for SAP ABAP Central Services \(ASCS\)|
|Version \[version\]|
|Installation directory \[install\_directory\]|
|Configuration directory \[config\_directory\]|
|Configuration file \[confi\_file\]|
|Instance name \[instance\_name\]|
|Instance number \[instance\_number\]|
|System ID \[sid\]|
|System directory \[system\_directory \]|
|System type \[system\_type\]|
|Transport domain \[transport\_domain\]|
|SAP Business Objects CMS server \[cmdb\_ci\_appl\_sap\_bo\]|
|Name \[name\]|Data collected for SAP Business Objects CMS Server|
|Server Name \[server\_name\]|
|Version \[version\]|
|Installation directory \[install\_directory\]|
|SAP SCS Application \[cmdb\_ci\_appl\_sap\_scs\]|
|Name \[name\]|Data collected for SAP Central Services \(SCS\)|
|Version \[version\]|
|Installation directory \[install\_directory\]|
|Configuration directory \[config\_directory\]|
|Configuration file \[config\_file\]|
|Instance name \[instance\_name\]|
|Instance number \[instance\_number\]|
|System ID \[sid\]|
|System directory \[system\_directory\]|
|System type \[system\_type\]|
|Transport domain \[transport\_domain\]|
|SAP CI Application \[cmdb\_ci\_appl\_sap\_ci\]|
|Name \[name\]|Data collected for SAP CI|
|Version \[version\]|
|Installation directory \[install\_directory\]|
|Configuration directory \[config\_directory\]|
|Configuration file \[config\_file\]|
|Instance name \[instance\_name\]|
|Instance number \[instance\_number\]|
|System ID \[sid\]|
|System directory \[system\_directory\]|
|System type \[system\_type\]|
|Transport domain \[transport\_domain\]|
|SAP DI Applications \[cmdb\_ci\_appl\_sap\_di\]|
|Name \[name\]|Data collected for SAP Dialog Instance \(DI\)|
|Version \[version\]|
|Installation directory \[install\_directory\]|
|Configuration directory \[config\_directory\]|
|Configuration file \[config\_file\]|
|Instance name \[instance\_name\]|
|Instance number \[instance\_number\]|
|System ID \[sid\]|
|System directory \[system\_directory\]|
|System type \[system\_type\]|
|Transport domain \[transport\_domain\]|
|SAP ERS Application \[cmdb\_ci\_appl\_sap\_ers\]|
|Name \[name\]|Data collected for SAP Enqueue Replication Server \(ERS\)|
|Version \[version\]|
|Installation directory \[install\_directory\]|
|Configuration directory \[config\_directory\]|
|Configuration file \[config\_file\]|
|Instance name \[instance\_name\]|
|Instance number \[instance\_number\]|
|System ID \[sid\]|
|System directory \[system\_directory\]|
|System type \[system\_type\]|
|Transport domain \[transport\_domain\]|
|HANA Database \[cmdb\_ci\_appl\_sap\_hana\_db\]|
|Name \[name\]|Data collected for SAP HANA Database|
|IP Address \[id\_address\]|
|Class \[sys\_class\_name\]|
|Fully qualified domain name \[fqdn\]|
|Version \[version\]|
|Installation directory \[install\_directory\]|
|SAP SID \[cmdb\_ci\_sap\_sid\]|
|Name \[name\]|Data collected for the SAP System Identification \(SID\) code is a unique identification code for an SAP R/3 installation. An SID is a three-character code like D10, PRD, or E56. An R/3 installation consists of a database server plus several application servers. ITOM Visibility uses the SAP SID shared library pattern to discover SIDs for SAP applications.|
|Version \[version\]|
|Patch Level Info \[sap\_patch\_info\]|

## Data collected by the SAP HANA DB Catalog on UNIX pattern during horizontal discovery

|Field|Description|
|-----|-----------|
|Catalog Owner \[catalog\_owner\]|The user ID of the schema owner.|
|Catalog Create Time \[catalog\_create\_time\]|The catalog creation time.|
|Disk Allocated Size \(MB\) \[disk\_allocated\_size\_mb\]|The allocated Disk size in MB.|
|Database Reference \[database\_instance\]|The reference to the SAP HANA DB.|

## CI Relationships

The SAP SID shared library pattern creates CI relationships between all major CI applications and SAP System ID.

|CI|Relationship|CI|
|---|------------|---|
|SAP ERS Application \[cmdb\_ci\_appl\_sap\_ers\]|Uses::Used by|SAP SID \[cmdb\_ci\_sap\_sid\]|
|SAP DI Applications \[cmdb\_ci\_appl\_sap\_di\]|Uses::Used by|SAP SID \[cmdb\_ci\_sap\_sid\]|
|SAP ASCS \[cmdb\_ci\_appl\_sap\_ascs\]|Uses::Used by|SAP SID \[cmdb\_ci\_sap\_sid\]|
|SAP CI Application \[cmdb\_ci\_appl\_sap\_ci\]|Uses::Used by|SAP SID \[cmdb\_ci\_sap\_sid\]|
|SAP SCS Application \[cmdb\_ci\_appl\_sap\_scs\]|Uses::Used by|SAP SID \[cmdb\_ci\_sap\_sid\]|
|SAP JC Application \[cmdb\_ci\_appl\_sap\_jc\]|Uses::Used by|SAP SID \[cmdb\_ci\_sap\_sid\]|

-   **SAP HANA DB Catalog on UNIX CI relationships**

    |CI|Relationship|CI|
    |---|------------|---|
    |SAP HANA DB \[cmdb\_ci\_appl\_sap\_hana\_db\]|Contains::Contained by|SAP HANA DB Catalog \[cmdb\_ci\_db\_hana\_catalog\]|


## Limitations

Service Mapping can map only one instance of ASCS per deployment.

The SAP HANA DB Catalog pattern can only run on UNIX.

**Parent Topic:**[Software discovery](../../discovery/concept/c_Software.md)

## Map application services containing SAP applications

Map a service instance containing an SAP application and verify that Service Mapping discovered all SAP components correctly.

### Before you begin

Role required: service\_mapping\_admin

### Procedure

1.  Create a service instance.

    1.  Navigate to **All** &gt; **Service Mapping** &gt; **Service Instances**.

    2.  Select **New**.

        The **Discoverable by Service Mapping** option is selected by default.

    3.  In the **Name** field, enter a descriptive name for the service instance.

2.  Define the entry point for this application service:

    1.  Select the **SAP application** tile.

        The **Discoverable by Service Mapping** option is selected by default.

    2.  Define the entry point as follows:

        -   A URL to any SAP module
        -   A TCP connection to any SAP module
        -   To discover environments with connected services, provide the URL to the web service in the following format:

            ```
             http://<hostname>:<port>/sap/bc/srt/scs/sap/z_servicenow_read?sap-client=003
            ```

    3.  Select **Add**.

    4.  Select **Save**.

3.  Select **Additional Info** on the left and clear the **Traffic based discovery** check box.

4.  Select **Update**.

5.  Verify that the mapping result is satisfactory:

    1.  Select **View Map** and wait until the mapping is complete.

        It may take a few minutes.

    2.  Review the application service map and make sure that the service layout is as in the following examples.

        ![Check the result of mapping an application service containing SAP components.](../image/SAP-top-down-map.png)

    If the SAP environment integrates SAP components with Tibco services, you can expect this mapping result:

    ![Check the result of mapping an application service containing SAP components integrated with Tibco services.](../image/SAP-with-Tibco-top-down-map.png)


## Troubleshoot application services containing SAP applications

Fix basic discovery issues based on the symptoms and discovery messages.

### Symptom

The application service map in Service Mapping displays the following message `Failed to discover <SAP component name>.`

### Cause

The CI failed to identify, and process detection retrieves the process attributes.

### Solution

Perform the following steps:

1.  Open the failed pattern step in Debug mode:
    1.  On the business service or service instance map, right-click the error message and select **Show discovery log**.

        The Discovery Log window opens.

    2.  In the right pane, locate the failed identification section and the failed step within this section.
    3.  Select this failed identification section and click **Debug**.

        The Debug Identification Section window opens.

    4.  If necessary, fill in the required details and click **Connect**.
2.  Click the **set variables** step under **Steps**.
3.  Make sure that the regular expression includes `SYS`.
4.  Click the **set install\_dir** step under **Steps**.
5.  Make sure that the regular expression includes `sap`.

### Symptom

Service Mapping fails to discover the web service your organization uses to deploy SAP digital business services.

### Cause 1

The pattern fails at the EVAL function for identifying the web service.

### Solution 1

1.  Verify that the format of the entry point is the URL to the web service as described in the mapping procedure.
2.  Verify that you configured the necessary applicative credentials as described in the mapping procedure.
3.  Check that the discovery log contains the following message: GROOVE\_CODE\_FAILURE: No such property: com for class: Script1.
4.  Open the failed pattern step in Debug mode:
    1.  On the business service or service instance map, right-click the error message and select **Show discovery log**.

        The Discovery Log window opens.

    2.  In the right pane, locate the failed identification section and the failed step within this section.
    3.  Select this failed identification section and click **Debug**.

        The Debug Identification Section window opens.

    4.  If necessary, fill in the required details and click **Connect**.
5.  Pattern Designer opens showing the selected identification section.
6.  Select the failed step on the right.
7.  Verify that the function running on EVAL is `com.snc.sw.util.HttpInvokerUtil.post`.
8.  Try to map the application service again and check the result.

### Cause 2

The pattern fails at the EVAL function for identifying the web service, because the web service was configured incorrectly.

### Solution 2

1.  Verify that the format of the entry point is the URL to the web service as described in the mapping procedure.
2.  Verify that you configured the necessary applicative credentials as described in the mapping procedure.
3.  Check that the discovery log contains the following message: "Debug run railed: Test step failed. GROOVE\_CODE\_FAILURE: All command implementations \(HTTP\) failed on host 10.x.x.x. Host must be down or unreachable. \(\)"
4.  Recreate the web service as described in [https://blogs.sap.com/2012/10/24/how-to-create-web-services-abap-based/](https://blogs.sap.com/2012/10/24/how-to-create-web-services-abap-based/).
5.  Try to map the application service again and check the result.

### Cause 3

The pattern fails at the EVAL function for identifying the web service, because the URL configured in the entry point is not correct or because the MID Server cannot access this URL.

### Solution 3

1.  Verify that the format of the entry point is the URL to the web service as described in the mapping procedure.
2.  Verify that you configured the necessary applicative credentials as described in the mapping procedure.
3.  Check that the discovery log contains the following message: "Debug run railed: Test step failed. GROOVE\_CODE\_FAILURE: All command implementations \(HTTP\) failed on host 10.x.x.x. Host must be down or unreachable. \(\)"
4.  Verify that you used the correct URL for the service entry point:
    1.  In the TCode SOAMANAGER, navigate to **Simplified Web Service Configuration**.
    2.  On the **Configuration** tab of the Simplified Service Configuration window, search for the web service that is part of the service instance.
    3.  Click the check box under **User Name/Password \(Basic\)** for this web service.
    4.  Click **Show Details**.
    5.  On the Details of the Service Definition window, verify the actual URL of the web service under WSDL URLs.
    6.  If necessary, fix the URL you configure for the entry point and try to map the service instance again.

### Cause 4

MID Server cannot access this URL configured in the entry point of the service instance.

### Solution 4

1.  Verify that the format of the entry point is the URL to the web service as described in the mapping procedure.
2.  Verify that you configured the necessary applicative credentials as described in the mapping procedure.
3.  Check that the discovery log contains the following message: "Debug run failed: Test step failed. GROOVE\_CODE\_FAILURE: All command implementations \(HTTP\) failed on host 10.x.x.x. Host must be down or unreachable. \(\)"
4.  Verify that you used the MID Server that can access the URL you configured in the service entry point:
    1.  Log into the MID Server host remotely.
    2.  Open a browser.
    3.  Paste the URL into the browser address bar and press Enter.
    4.  If the page does not open, it means that there is a network issue, for example, there is a firewall that prevents the MID Server from accessing this URL.
5.  Resolve the network issue and verify that the MID Server can access the URL as described in step [4](sap-discovery.md#VerifyingCredentials-networkIssues).

### Cause 5

MID Server cannot access this URL configured in the entry point of the service instance.

### Solution 5

1.  Verify that the format of the entry point is the URL to the web service as described in the mapping procedure.
2.  Verify that you configured the necessary applicative credentials as described in the mapping procedure.
3.  Check that the discovery log contains the following message: "Debug run railed: Test step failed. GROOVE\_CODE\_FAILURE: All command implementations \(HTTP\) failed on host 10.x.x.x. Host must be down or unreachable. \(\)"
4.  Verify that the applicative credentials you configured on the ServiceNow AI Platform for the web service are valid:
    1.  Log into the MID Server host remotely.
    2.  Open a browser.
    3.  Paste the URL into the browser address bar and press Enter.
    4.  The browser page displays the credentials pop-up window.
    5.  Enter the credentials and check that the page opens.

        The page does not open, it means that the configured applicative credentials are incorrect.

5.  Find out the right credentials.
6.  Verify the new credentials as described in step [4](sap-discovery.md#CredetialVerif-IncorrectCredtials).
7.  If the page opens after you use the new credentials, configure these credentials as applicative credentials on the ServiceNow AI Platform.

### Cause 6

MID Server cannot access this URL configured in the entry point of the service instance.

### Solution 6

1.  Verify that the format of the entry point is the URL to the web service as described in the mapping procedure.
2.  Check that the discovery log contains the following message: "Debug run railed: Test step failed. GROOVE\_CODE\_FAILURE: Missing applicative credentials for CI type &lt;name of the CI type&gt;".
3.  Verify that you defined applicative credentials for the relevant CI according as described in [Map application services containing SAP applications](sap-discovery.md#).

