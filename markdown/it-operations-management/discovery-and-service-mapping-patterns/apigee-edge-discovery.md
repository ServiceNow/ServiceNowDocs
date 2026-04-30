---
title: Apigee Edge Enterprise edition discovery
description: The ServiceNow Discovery application uses the APIGee pattern to find Apigee Edge Enterprise edition versions 4.x.x. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Apigee Edge Enterprise edition discovery

The ServiceNow Discovery application uses the APIGee pattern to find Apigee Edge Enterprise edition versions 4.x.x. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The APIGee pattern uses a built-in cache mechanism that collects data from each API service into a local cache file. Service Mapping performs top-down discovery on these cache files to find outgoing Apigee Edge connections.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Linux user**

    Provide the Linux operating system \(OS\) user with elevated rights for running the cat, ls, netstat, and stat commands. For more information, see [Service Mapping commands requiring a privileged user](../reference/r_CommandsnCredentials.md).

    In addition, provide this Linux user with permissions to run the following commands on the OS user home folder:

    |Command|Description|
    |-------|-----------|
    |"date +%s"|Gets the current date.|
    |"ls -d $HOME/APIGee\_Cache/cache\_folder\*"|Gets the last cache folder.|
    |"mkdir-p $HOME/APIGee\_Cache/cache\_folder\_" + $today + ";ls -d$HOME/APIGee\_Cache/cache\_folder\_" + $today|Creates the cache file if the cache file is empty.|
    |"ls -d $HOME/APIGee\_Cache/cache\_folder\*"|Verifies that the cache file has been created.|
    |"echo \`expr " + $today + " -" + $current\_date+ "\`”|Calculates the gap between the folder creation time and the current date.|
    |"if \[ " + $diff + " -ge" + $week\_seconds+ " \]; then echo true; fi”|Checks if it is necessary to recreate the folder.|
    |"ls" + $cache\_folder+ "/\* \| sort \| xargsgrep -l " + $entry\_point.source\_url|Checks if existing cache files contain the source URL that you enter as the entry point for the service.|
    |"rm-rf" + $cache\_folder+ ";mkdir-p $HOME/APIGee\_Cache/cache\_folder\_" + $today + ";ls -d $HOME/APIGee\_Cache/cache\_folder\_" + $today|Removes old cache files.|
    |“curl -k -X GETurl-H '&lt;ClientID&gt;: &lt;Token&gt;’”|Gets the API response for the given token.|
    |"ls" + $cache\_folder+ "/\* \| sort \| xargsgrep -l " + $entry\_point.source\_url|Gets the URL definition from the cache file.|

-   **Applicative credential**

    Configure the applicative credential as follows:

<table id="table_p5x_2ys_52b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The credential name, for example Apigee token.

</td></tr><tr><td>

Active

</td><td>

Check box for enabling this credential for discovery.

</td></tr><tr><td>

User name

</td><td>

The name of the user of this applicative credential. You can use any user for the credential for this pattern, since the information is extracted from a local cache.

</td></tr><tr><td>

Password

</td><td>

The actual user password of this applicative credential.

</td></tr><tr><td>

CI type

</td><td>

The CI type for which this credential is used: APIGee Service \[cmdb\_ci\_appl\_apigee\_srv\]. **Note:** ServiceNow applications refer to devices and applications that comprise a service instance as configuration items \(CIs\).

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

Order

</td><td>

Enter the order \(sequence\) in which the platform tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr></tbody>
</table>-   **curl command**

    Make sure that the curl command is installed on the Linux server hosting Apigee Edge.

-   **Configure system properties**

    -   To create top-down outgoing Apigee Edge connections, configure the Apigee URLs \(apigee.urls\) system property using the following syntax:

        `01#DVL#https://<url1>.com/dashboard/v1/targetServers/dvl### 02#QA#https://<url2>.com/dashboard/v2/targetServers/qa###`

        Where

        01 is the URL number.

        DVL is the environment type, like development.

        \# is the delimiter between the attributes. Place it exactly where it is in the example above.

        \#\#\# is the delimiter between URLs.

    -   Configure the Apigee API Client ID \(apigee.api.client.id\) system property by entering the Apigee API Client ID in the Value field. The pattern uses this property as header for the curl command with the token:

        `curl -k -X GET " + url + " -H ' apigee.api.client.id: " + token`

    The pattern populates these two system properties using the Add Apigee URLs and Apigee api client id sa\_pre\_task\_script.


## Data collected by Discovery for Apigee Edge Enterprise edition

Discovery populates the data in the CMDB when running the APIGee pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the server hosting the Apigee Edge.|
|Version \[version\]|The version of the Apigee Edge.|
|Installation directory \[install\_directory\]|The folder containing all the Apigee Edge libraries and executable files.|
|Configuration directory \[config\_directory\]|The folder containing all the Apigee Edge configuration files.|

## CI relationships

The APIGee pattern does not create any CI relationships.

## Data collected by Service Mapping during top-down discovery

The APIGee pattern identifies connections from the Apigee Edge to other CIs based on the URL you configure in the connection section of the pattern.

**Parent Topic:**[Available discovery patterns](available-patterns.md)

