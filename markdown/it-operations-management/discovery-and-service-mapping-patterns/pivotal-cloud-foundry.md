---
title: Pivotal Cloud Foundry discovery
description: The ServiceNow Discovery application finds Pivotal Cloud Foundry \(PCF\) version 3 components using the Pivotal Cloud Foundry pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Pivotal Cloud Foundry discovery

The ServiceNow Discovery application finds Pivotal Cloud Foundry \(PCF\) version 3 components using the Pivotal Cloud Foundry pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

You can use this pattern on the ServiceNow AI Platform starting Kingston version.

The discovery of PCF V3 components is supported when the Discovery and Service Mapping Patterns plugin Version 1.0.99, March 2023 is installed. The Pattern continues to support the discovery of PCF V2 components.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Pivotal Cloud Foundry credentials**

    Create the Pivotal Cloud Foundry credentials.

    1.  Navigate to **Discovery** &gt; **Credentials**.
    2.  Select **New**.
    3.  Select **CloudFoundry Credentials**.
    4.  On the form, fill in the fields:

<table id="table_gxd_ljv_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Credential name. As an example, `pcf_user credentials`

</td></tr><tr><td>

Active

</td><td>

Option for enabling this credential for discovery. Select this check box to enable discovery.

</td></tr><tr><td>

Applies to

</td><td>

Credentials that you may or may not want to apply to **All MID servers** in your network, or to one or more **Specific MID servers**. Select **Specific MID servers**.

</td></tr><tr><td>

Order

</td><td>

Order in which the platform tries this credential as it tries to log in to devices. A smaller number indicates that the credential seems higher in the list. Establish the credential order when using large numbers of credentials or when security locks out users after three failed logins tries. If all the credentials have the same order number, or none, the instance tries the credentials in a random order. The default value is 100.

</td></tr><tr><td>

User name

</td><td>

Name of the user of these credentials. Avoid leading or trailing spaces in user names. A warning seems if the platform detects leading or trailing spaces in the user name. An example is `pcf_user`. Use the `client_id` that is used to generate the JWT token.

</td></tr><tr><td>

Password

</td><td>

Password for the user of these credentials. Use the `client_secret` that is used to generate the JWT token.

</td></tr><tr><td>

Credential alias

</td><td>

Alternate name for these credentials. As an example, `cf` If this field is closed, select the unlock icon to unlock the field.

</td></tr></tbody>
</table>    5.  Select **Update**.
-   **JSON web token credentials**

    To verify the JSON web token \(JWT\), perform the following token validation steps.

    The format of the JWT token is: [https://docs.cloudfoundry.org/api/uaa/version/4.27.0/index.html\#jwt-bearer-token-grant](https://docs.cloudfoundry.org/api/uaa/version/4.27.0/index.html#jwt-bearer-token-grant)

    1.  Run the following cURL script against the User Account and Authentication \(UAA\) server API and verify the results:

        `curl -s -k https://ip_address:port/oauth/token -X; POST -H ”Content-Type: application/x-www-form-urlencoded” -H “Accept: application/json” -d “client_id=<INSERT_USER_HERE>&client_secret=<INSERT_PASS_HERE>&grant_type=client_credentials&token_format=jwt&response_type=token”`

        If this command doesn’t generate a token, verify that the credentials in the ServiceNow repository are correct, otherwise go to step 2.

    2.  Run the following cURL script against Pivotal Cloud Foundry API:

        `curl https://ip_address:port/v3/spaces -k -v -H “Accept: application/json” -H “Authorization: bearer<INSERT TOKEN HERE>”`

        If this command doesn’t retrieve the PCF spaces information, verify the credentials on the ServiceNow credentials repository.

-   **Credentials for V3 API elements**

    Provide a read-only user with permission to use the following API elements:

    -   –/v3/organizations
    -   –/v3/spaces
    -   –/v3/domains
    -   –/v3/routes
    -   –/v3/organization\_quotas
    -   –/v3/space\_quotas
    -   –/v3/apps
    -   -/v3/service\_offerings
    -   -/v3/service\_plans
    -   -/v3/service\_instances
    -   -/v3/droplets
    **Note:** The Pivotal Cloud Foundry Pattern also supports the PCF V2 APIs.

-   **Create a serverless Discovery schedule**
    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Select **New**.
    3.  On the form, fill in the fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter a unique and descriptive name for this Discovery schedule, for example, `pcf`|
        |Discover|For the Discover type, select **Serverlesss**|
        |MID Server|MID Servers that the credentials apply to. Specify the required MID Server, for example, `Discovery_Server`|
        |Active|Option for enabling this credential for discovery. Select this check box to enable discovery.|
        |Credential alias|Alternate name for these credentials. Use the alias related with the Pivotal Cloud Foundry credentials that you created earlier.|

    4.  Right-click the header of the Discovery Schedule form and select **Save**.

        ![Serverless execution pattern](../image/serverless-execution-pattern.png)

    5.  Select the Serverless Execution Patterns tab.
    6.  Select **New**.
    7.  On the form, fill in the fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter a unique and descriptive name for this Serverless Execution Pattern, for example, `pcf1`|
        |Pattern|Select **CloudFoundry**.|
        |Proxy Host|Fully qualified domain name of the machine on which you’re installing the proxy server. Specify **Global**.|
        |Active|Check box to enable this schedule for discovery. Select this check box.|

    8.  Right-click the header of the Serverless Execution Patterns form and select **Save**.
    9.  Select the Serverless Execution Patterns tab
    10. Create and define the serverless execution pattern as described in the product documentation.

        Configure the parameters required by the Pivotal Cloud Foundry Pattern as follows:

        |Parameter|Description|
        |---------|-----------|
        |Organization|Name of the organization that is required to be discovered, or all where the input is “\*”.|
        |CredentialAlias|Alternate name for these credentials. Use the alias related with the Pivotal Cloud Foundry credentials that you created earlier.|
        |URL\_CF|API URL of the Cloud Controller that is used to retrieve the information from Pivotal Cloud Foundry.|
        |URL\_CF\_AUTH|UAA server API​that is used to generate the token. Enter the value in the format: https://uaa.sys.dev.phx.pcf.example.com/oauth/token|

    11. **Update**.
    12. To start discovery, navigate to the Serverless Discovery definition and select **Discover Now**.
-   **EVAL closure functions**

    Use the following EVAL closure functions to concatenate all organizations with “,” as a separator.

    ```
    var rtrn = ’’;
    var organizations = ${organizations[*].name};
    var beforeReturn = ’’;
    var separator = ’’;
    for (var i = 0; i < organizations.size(); i++)   
    	{
    	beforeReturn += separator + organizations.get(i);  
    	separator = ',';   
    	}
    rtrn = beforeReturn;
    
    ```

    Use the following EVAL closure functions to return 1 if the operational status is active and 2 if it isn’t active.

    ```
    var rtrn = '';
    var currentOrgStatus = ${organizations[].operational_status};
    var status = currentOrgStatus.toLowerCase();
    if(status == "active"){  
       rtrn = "1";  
    }
    else { 
       rtrn = "2";
    }
    
    ```

    Use the following EVAL closure function to return 1 if the operational status is started and 2 if it isn’t started.

    ```
    var rtrn = '';
    var currentAppStatus = ${apps[].state};
    var status = currentAppStatus.toLowerCase();
    if(status == "started"){
       rtrn = "1";  
    }
    else {   
       rtrn = "2";   
    }
    
    ```

-   **CloudFoundry Get Call**

    The CloudFoundry Get Call custom operation handles the generation of tokens. It uses the credentials and URL\_CF\_AUTH context variable to generate a token that is used to create API calls.

    When a token is generated, the URL\_CF is used to create the API calls defined in the **Resource** field. The custom operation also handles pagination where the response has more than one page.

    CloudFoundry Get Call parses the input JSON to populate the tables and variables.

    ![Cloud Foundry custom operation](../image/cloud-foundry-custom-operation.png)


## Pivotal Cloud Foundry BOSH extension section

The Pivotal Cloud Foundry BOSH is an extension section of the Pivotal Cloud Foundry Pattern.

The extension is available on the ServiceNow® Store for the June 2023 release of Discovery and Service Mapping Patterns 1.6.0.

-   **Requirements for Pivotal Cloud Foundry BOSH**

    **Note:** The following requirements are relevant only to the BOSH extension section.

    The Opsman authentication URL has to be provided as a pattern parameter with the name **URL\_OPSMAN\_AUTH**. For example: `https://<opsman entry point>/uaa/oauth/token`

    The added credentials must have permission to execute the following APIs:

    -   /uaa/oauth/token
    -   /api/v0/deployed/products
    **Note:** Custom APIs are added as Tanzu Opsman Get API step to the Pattern.


## Data collected by Discovery during horizontal discovery

<table id="table_o21_dlv_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Main CI: PCF Foundation \[cmdb\_ci\_pcf\_foundation\]

</td></tr><tr><td>

Name

</td><td>

Pivotal Cloud Foundry cluster entry name`<name>-<hostCf:<portCf>`

</td></tr><tr><td>

ip\_address

</td><td>

Pivotal Cloud Foundry host IP.

</td></tr><tr><td>

port

</td><td>

Pivotal Cloud Foundry service port.

</td></tr><tr><td>

short\_description

</td><td>

Pivotal Cloud Foundry service build number.

</td></tr><tr><td>

Organization

</td><td>

Organization list, managed by PCF cluster. The entries are separated using a “,” comma separator.

</td></tr><tr><td class="sub-head" colspan="2">

PCF Organization \[cmdb\_ci\_pcf\_organization\]

</td></tr><tr><td>

Name

</td><td>

Organization name

</td></tr><tr><td>

URL

</td><td>

Organization unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Organization UID in CF

</td></tr><tr><td>

operational\_status

</td><td>

Organization status

</td></tr><tr><td class="sub-head" colspan="2">

PCF Space \[cmdb\_ci\_pcf\_space\]

</td></tr><tr><td>

Name

</td><td>

Space name

</td></tr><tr><td>

URL

</td><td>

Space unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Space UID in CF

</td></tr><tr><td class="sub-head" colspan="2">

PCF Application \[cmdb\_ci\_pcf\_appl\]

</td></tr><tr><td>

Name

</td><td>

Application name

</td></tr><tr><td>

URL

</td><td>

Application unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Application UID in CF

</td></tr><tr><td class="sub-head" colspan="2">

PCF Route \[cmdb\_ci\_pcf\_route\]

</td></tr><tr><td>

Name

</td><td>

Route name

</td></tr><tr><td>

URL

</td><td>

Route unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Route UID in CF

</td></tr><tr><td>

port

</td><td>

Route port

</td></tr><tr><td>

type

</td><td>

Route type

</td></tr><tr><td class="sub-head" colspan="2">

PCF Quota \[cmdb\_ci\_pcf\_quota\]

</td></tr><tr><td>

Name

</td><td>

Quota name

</td></tr><tr><td>

URL

</td><td>

Quota unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Quota UID in CF

</td></tr><tr><td class="sub-head" colspan="2">

PCF Domain \[cmdb\_ci\_pcf\_domain\]

</td></tr><tr><td>

name

</td><td>

Domain name

</td></tr><tr><td>

url

</td><td>

Domain unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Domain UID in CF

</td></tr><tr><td class="sub-head" colspan="2">

PCF Space instance \[cmdb\_ci\_pcf\_space\_instance\]

</td></tr><tr><td>

name

</td><td>

Space service instance name

</td></tr><tr><td>

url

</td><td>

Space service instance unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Space service instance UID in CF

</td></tr><tr><td class="sub-head" colspan="2">

PCF Service Plan \[cmdb\_ci\_pcf\_service\_plan\]

</td></tr><tr><td>

name

</td><td>

Service plan instance name

</td></tr><tr><td>

url

</td><td>

Service plan unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Space service instance UID in CF

</td></tr><tr><td class="sub-head" colspan="2">

PCF Service \[cmdb\_ci\_pcf\_service\]

</td></tr><tr><td>

name

</td><td>

Service name

</td></tr><tr><td>

url

</td><td>

Service unique URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Service UID in CF

</td></tr><tr><td class="sub-head" colspan="2">

PCF Droplet \[cmdb\_ci\_pcf\_droplet\]

</td></tr><tr><td>

name

</td><td>

Resource URL

</td></tr><tr><td>

pcf\_guid

</td><td>

Droplet ID

</td></tr><tr><td>

url

</td><td>

Droplet URL

</td></tr><tr><td>

install\_status

</td><td>

Installation status: 1, "installed"

</td></tr><tr><td>

operational\_status

</td><td>

Operational status: 1, "operational"

</td></tr><tr><td class="sub-head" colspan="2">

Key Value \[cmdb\_key\_value\]

</td></tr><tr><td>

key

</td><td>

Resource Tag key**Note:** This data is only collected for V3 API calls.

</td></tr><tr><td>

value

</td><td>

Resource Tag value.**Note:** This data is only collected for V3 API calls.

</td></tr></tbody>
</table><table id="table_b4d_dy1_dxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

BOSH Deployment \(cmdb\_ci\_bosh\_deployment\)

</td></tr><tr><td>

Name

</td><td>

The installation name of the resource.

</td></tr><tr><td>

object\_id

</td><td>

The ID of the deployed product.

</td></tr><tr><td>

install\_status

</td><td>

Hard-coded to the value: *1= installed*.

</td></tr><tr><td>

operational\_status

</td><td>

Hard-coded to the value: *1= operational*.

</td></tr><tr><td>

deployment\_version

</td><td>

The version of the deployed product.

</td></tr><tr><td>

deployment\_type

</td><td>

The type of the deployed product.

</td></tr></tbody>
</table>## CI relationships

These relationships are created to support Pivotal Cloud Foundry discovery.

<table id="table_vkt_ywd_rdb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

PCF Space \[cmdb\_ci\_pcf\_space\]

</td></tr><tr><td>

cmdb\_ci\_pcf\_space

</td><td>

Contains::Contained by

</td><td>

cmdb\_ci\_pcf\_organization

</td></tr><tr><td class="sub-head" colspan="3">

PCF Application \[cmdb\_ci\_pcf\_appl\]

</td></tr><tr><td>

cmdb\_ci\_pcf\_appl

</td><td>

Contains::Contained by

</td><td>

cmdb\_ci\_pcf\_space

</td></tr><tr><td class="sub-head" colspan="3">

PCF Route \[cmdb\_ci\_pcf\_route\]

</td></tr><tr><td>

cmdb\_ci\_pcf\_route

</td><td>

Contains::Contained by

</td><td>

cmdb\_ci\_pcf\_foundation

</td></tr><tr><td class="sub-head" colspan="3">

PCF Quota \[cmdb\_ci\_pcf\_quota\]

</td></tr><tr><td>

cmdb\_ci\_pcf\_quota

</td><td>

Uses::Used by

</td><td>

cmdb\_ci\_pcf\_spacecmdb\_ci\_pcf\_organization

</td></tr><tr><td class="sub-head" colspan="3">

PCF Domain \[cmdb\_ci\_pcf\_domain\]

</td></tr><tr><td rowspan="3">

cmdb\_ci\_pcf\_domain

</td><td>

Uses::Used by

</td><td>

cmdb\_ci\_pcf\_route

</td></tr><tr><td>

Owns::Owned by

</td><td>

cmdb\_ci\_pcf\_organization

</td></tr><tr><td>

Contains::Contained by

</td><td>

cmdb\_ci\_pcf\_foundation

</td></tr><tr><td class="sub-head" colspan="3">

PCF Space instance \[cmdb\_ci\_pcf\_space\_instance\]

</td></tr><tr><td>

cmdb\_ci\_pcf\_space\_instance

</td><td>

Contains::Contained by

</td><td>

cmdb\_ci\_pcf\_space

</td></tr><tr><td class="sub-head" colspan="3">

PCF Service Plan \[cmdb\_ci\_pcf\_service\_plan\]

</td></tr><tr><td>

cmdb\_ci\_pcf\_service\_plan

</td><td>

Uses::Used by

</td><td>

cmdb\_ci\_pcf\_space\_instance

</td></tr><tr><td class="sub-head" colspan="3">

PCF Service \[cmdb\_ci\_pcf\_service\]

</td></tr><tr><td>

cmdb\_ci\_pcf\_service

</td><td>

Uses::Used by

</td><td>

cmdb\_ci\_pcf\_service\_plan

</td></tr><tr><td class="sub-head" colspan="3">

PCF Droplet \[cmdb\_ci\_pcf\_droplet\]

</td></tr><tr><td>

cmdb\_ci\_pcf\_appl

</td><td>

Contains::Contained by

</td><td>

cmdb\_ci\_pcf\_droplet

</td></tr><tr><td class="sub-head" colspan="3">

Key Value \[cmdb\_key\_value\]

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_droplet

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_organization

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_space

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_domain

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_route

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_appl

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_service

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_service\_plan

</td></tr><tr><td>

cmdb\_key\_value

</td><td>

Reference only.For example: configuration\_item

</td><td>

cmdb\_ci\_pcf\_space\_instance

</td></tr></tbody>
</table>## Pivotal Cloud Foundry BOSH relationships

These relationships are created to support Pivotal Cloud Foundry BOSH extension section discovery.

<table id="table_xmf_cbb_dxb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Cloud Foundry Cluster \[cmdb\_ci\_pcf\_foundation\]

</td><td>

Contains::Contained by

</td><td>

BOSH Deployment \[cmdb\_ci\_bosh\_deployment\]

</td></tr></tbody>
</table>**Parent Topic:**[Available on-premise discovery patterns](available-patterns.md)

