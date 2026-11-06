---
title: Configure ADM discovery parameters and properties
description: Using properties, you can enable or disable ADM discovery, and you can set the location of the TCP tracking file for enhanced ADM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/configuring-adm-disco.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Application Dependency Mapping \(ADM\) for Discovery, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure ADM discovery parameters and properties

Using properties, you can enable or disable ADM discovery, and you can set the location of the TCP tracking file for enhanced ADM.

## Before you begin

Role required: discovery\_admin or admin

## About this task

You can also control both the size of the TCP tracking file and the payload using parameters on the enhanced ADM probes. See [TCP connection discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/r_DataCollDiscoTCPConnections.md) for the names of the probes and parameters.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Discovery** to set the system properties.

2.  Navigate to **Discovery Definition** &gt; **Probes** to set the probe parameters.

3.  Configure the following properties and probe parameters.

    See the knowledge article [KB0822767](https://support.servicenow.com/kb_view.do?sysparm_article=KB0822767) for more information.

<table id="table_pg3_bfx_q1b"><thead><tr><th>

Probe parameter

</th><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

glide.discovery.enable\_adme

</td><td>

ADME: Enable enhanced ADM probe. If "yes", the ADM Enhanced probe is triggered and only fall back to the ADM probe as needed.-   Type: true \| false
-   Default value: false


</td></tr><tr><td>

 

</td><td>

glide.discovery.application\_mapping

</td><td>

Enable the application mapping feature. When this property is set to true, all discoveries trigger the relevant ADM probe during the exploration phase if Discovery finds a server.

 **Important:** Disabling this property disables the creation of relationships between applications but doesn’t disable the ADM probes and sensors, nor does it prevent process classification.

 -   Type: true \| false
-   Default value: true


</td></tr><tr><td>

sampling\_interval

</td><td>

glide.discovery.adme.sampling\_interval

</td><td>

ADME - Sampling interval \(sec\): How often to sample process and connection data in seconds. Must be a minimum of 5 seconds.-   Type: integer
-   Default value: 120


</td></tr><tr><td>

base\_dir

</td><td>

glide.discovery.adme.base\_dir\_unix

</td><td>

ADME - Unix Base Dir: An existing directory on the target UNIX machines to be used as a workspace. Must be an absolute path to the directory. The [UNIX and Linux credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_SSHCredentialsForm.md) that you use to connect to the device must also be able to access this folder.-   Type: string
-   Default value: /tmp


</td></tr><tr><td>

powershell\_param\_base\_dir

</td><td>

mid.powershell.target\_base\_dir

</td><td>

Powershell - Target Base Dir: A network share on the target Windows machines to be used as a workspace. If you change the directory, it must also be a network shared folder.-   Type: string
-   Default value: admin$\\temp


</td></tr><tr><td>

aggregation\_interval \(Unix\)powershell\_param\_aggregation\_interval \(Windows\)

</td><td>

glide.discovery.adme.aggregation\_interval

</td><td>

ADME - Aggregation interval \(sec\): How often to aggregate instantaneous data into chunks in seconds. It must be a minimum of 60 seconds and it must be a multiple of ADME Sampling interval.-   Type: integer
-   Default value: 3600


</td></tr><tr><td>

rolling\_window\_size \(Unix\)powershell\_param\_rolling\_window\_size \(Windows\)

</td><td>

glide.discovery.adme.rolling\_window\_size

</td><td>

ADME - Rolling window size: How many recently aggregated chunks to keep. An aggregated chunk consists of ADME Aggregation interval divided by ADME Sampling interval samples. Only the newest chunks are kept.-   Type: integer
-   Default value: 24


</td></tr><tr><td>

max\_total\_samples \(Unix\)powershell\_param\_max\_total\_samples \(Windows\)

</td><td>

glide.discovery.adme.max\_total\_samples

</td><td>

ADME - Max total samples: The limit of samples being taken by the script. The script will stop running after this number of samples are taken.-   Type: integer
-   Default value: 100


</td></tr><tr><td>

 

</td><td>

mid.windows.management\_protocol

</td><td>

MID Server parameter that selects the Windows management protocol used for device and process classification. Options include:

-   WMI
-   WinRM
 -   Type: string
-   Default value: WMI


</td></tr><tr><td>

powershell\_param\_max\_result\_payload\_size \(Windows\)

</td><td>

\[OXY-PLACEHOLDER\]

</td><td>

ADME - Max result payload size: The maximum size of the ADME result payload.

 -   Type: \[OXY-PLACEHOLDER\]
-   Default value: 4 MB


</td></tr></tbody>
</table>4.  Click **Save**.


**Parent Topic:**[Application Dependency Mapping \(ADM\) for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/r_ApplicationDependencyMapping.md)

