---
title: Using push-based Discovery and SAM together
description: ACC-V collects installed software data for use cases for Software Asset Management \(SAM\), when the SAM plugin is installed. Using push-based Discovery and SAM together can help optimize software data collection with SAM basic metering and SAM total usage metrics. You can also retrieve some software edition information.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Using Agent Client Collector for Visibility, Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# Using push-based Discovery and SAM together

ACC-V collects installed software data for use cases for Software Asset Management \(SAM\), when the SAM plugin is installed. Using push-based Discovery and SAM together can help optimize software data collection with SAM basic metering and SAM total usage metrics. You can also retrieve some software edition information.

ACC-V can capture the last accessed time for the software or applications that are installed on the target via push-based Discovery. This information along with the target CI reference, is added to the Software Update \[samp\_sw\_usage\] table.

Starting in ACC-V version 2.2.0, SAM Basic metering is supported for Windows and macOS.

Starting in ACC-V version 3.3.0, SAM total usage metrics is supported for Windows and macOS.

The software usage records are domain separated. The records are persisted with the domain of the MID Server that is used for the agent-based Discovery for the target.

**Note:** For software installations \(cmdb\_sam\_sw\_install\), to avoid insertion of duplicate records, the same discovery source "ServiceNow" is being used for both push-based Discovery and horizontal IP-based Discovery.

## Requirements

-   **SAM basic metering and SAM total usage metrics**

    For SAM basic metering and SAM total usage metrics, the non-privileged servicenow user \(which the agent service logs on as\) must be configured with READ only access in the registry. This access allows for successful execution of the OSQuery against the UserAssist table to be successful. Go to regedit and allow the servicenow user to read UserAssist for a user account on the device \(for example: `HKEY_USERS\SID...\Software\\Microsoft\\Windows\\CurrentVersion\\Explorer\\UserAssist` for every user in `HKEY_USERS`\).

    **Note:** The **UserAssist** key does not inherit permissions from the **HKEY\_USERS\\SID...** parent key. Therefore, you must navigate to the **UserAssist** key and add permission directly on the key.

    To apply SAM basic metering or SAM total usage metrics, you need the following:

    -   SAM plugin \(com.snc.samp\) enabled
    -   System property \[**sn\_acc\_vis\_content.persist\_sam\_usage\_metrics**\] set to true. See [System properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more details.
    For details on SAM metering setup with the Agent Client Collector, see the Knowledge Base article [KB1642676](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1642676).


-   **Software edition information**

    To retrieve software edition information, you need the SAM plugin \(com.snc.samp\) enabled.


## SAM basic metering

**Note:** There is a configuration in the Windows operating system level that does not allow the correct detection of the data. Update the configuration so that the data can successfully be collected by the ACC-V agent and brought to the ServiceNow platform correctly. In the Registry Editor, create the following keys in the path:**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Explorer\\Advanced.**

-   Name: Start\_TrackProgs
    -   Base: Hexadecimal
    -   Value:1
-   Name: Start\_TrackProgsBase
    -   Base: Hexadecimal
    -   Value:1

For the list of software in the payload, query the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table to fetch the corresponding product and publisher. Once the product is fetched, check if the reclamation rule is enabled for that product to persist the last usage information in the Software Usage \[samp\_sw\_usage\] table. See the flowchart for details.

![Describes the flow how SAM works with ACC-V for basic metering](../image/sam_flow.png "SAM basic metering flowchart")

**Note:** In the target, query the last accessed time from the UserAssist table via the OSQuery by taking the application or software name as the input to the Query.

Use the **sn\_acc\_vis\_content.disable\_sam\_reclamation\_rules\_for\_licensable\_softwares** property to define reclamation rules for licensable software, as follows:

-   **True**: Disable invoking reclamation rules for licensable software. SAM usage continues for all licensable software and for non-licensable software with defined reclamation rules.
-   **False**: Store SAM usage according to defined reclamation rules.

Common applications supported include:

-   WinZip
-   Google Chrome
-   Sublime Text
-   Notepad++
-   Autodesk
-   Microsoft Office 365
-   Tableau

## SAM total usage metrics

SAM total usage metrics allows you to measure total usage time and total usage count on any application that has a software reclamation rule enabled.

Osquery provides a daemon executable which can run as a service, called Osqueryd. Osqueryd needs to be manually deployed for SAM total usage metrics to work properly. Each Osqueryd deployment requires the osquery.conf file, optional external packs, and initialization flags \(configured in osquery.flags file\) provided when starting the service. In return, the daemon service runs scheduled queries on the host and logs it into a local file system.

**Note:** Osquery supports filesystem-based logging by default. This configuration is provided in the osquery.conf file on any fresh Osquery installation.

Domain information can be collected during the data collection. This can help large organizations with multiple employee directories map software to the correct user. Currently, this is supported for Windows only. To map the software usage/assigned\_to with the correct user in a domain separated environment, use the system property \[sn\_acc\_vis\_content.column\_name\_for\_user\_mapping\] with a valid field name. By default, the value of this system property is empty which means it only validates the username and not the domain. You can use either of the following formats to validate username and domain: username@domain or domain\\username.

Using the list of processes, you can perform SAM normalization to map the processes for the relevant installed software records. This provides flexibility since installed software names and processes are not usually the same. For the list of processes in the payload, query the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table and Software Product \[samp\_sw\_product\] table to fetch the corresponding product and publisher. Once the product is fetched, check if the reclamation rule is enabled for that product to persist the total usage time in the Software Usage \[samp\_sw\_usage\] table. See the flowchart for details.

![Describes the flow how SAM works with ACC-V for total usage metering](../image/sam_total_usage_metrics.png "SAM total usage metrics flowchart")

install and configure Osqueryd for Windows using the following script.

```
# Install latest osquery

$msi = "osquery-5.7.0.msi"
$url = "https://pkg.osquery.io/windows/$msi"
$dst = "$PSScriptRoot\$msi"
Invoke-WebRequest -Uri $url -OutFile $dst
# msiexec /i "$dst" /quiet /qn /norestart
Start-Process msiexec.exe -Wait "/i $dst /quiet /qn /norestart"

# Configure osqueryd service

$flags = "--logger_rotate=true
--logger_rotate_size=26214400
--logger_rotate_max_files=1
--watchdog_level=-1
--config_path=C:\Program Files\osquery\osquery-sam.conf"
Set-Content -Path 'C:\Program Files\osquery\osquery.flags.default' -Value "$flags"

$conf = @'
{
  "options": {
    "config_plugin": "filesystem",
    "logger_plugin": "filesystem",
    "utc": "true"
  },
  "schedule": {
    "sam_process_info": {
      "query": "SELECT name, pid, elapsed_time, start_time, user_time, system_time, username FROM processes p JOIN users u ON u.uid = p.uid WHERE p.elapsed_time != -1 AND u.type != 'special';",
      "snapshot" : true,
      "interval": 300
    },
    "system_info": {
      "query": "SELECT hostname, cpu_brand, physical_memory FROM system_info;",
      "interval": 3600
    }
  },
  "decorators": {
    "load": [
      "SELECT uuid AS host_uuid FROM system_info;",
      "SELECT user AS username FROM logged_in_users ORDER BY time DESC LIMIT 1;"
    ]
  },
  "packs": {
  }
}
'@
Set-Content -Path 'C:\Program Files\osquery\osquery-sam.conf' -Value "$conf"

cd 'C:\Program Files\osquery'
.\manage-osqueryd.ps1 -uninstall
.\manage-osqueryd.ps1 -install
Restart-Service osqueryd


```

For details on Windows and macOS see [Configure Osqueryd schedule for SAM total usage metrics](../task/import-external-pack-file-for-sam-total-usage-metrics.md) and [Configure Osqueryd logs for SAM total usage metrics](../task/configure-osquery-logs-for-sam-total-usage-metrics.md).

## Collecting SAM metrics without osqueryd

Optionally, you can enhance efficiency by using non-osqueryd data collection when using push-based Discovery and Software Asset Management \(SAM\) together. When non-osqueryd data collection is invoked, data collection is automatically performed on all available agents, instead of invoking osqueryd on each agent individually.

To perform non-osqueryd data collection:

1.  Ensure that the following permissions are configured for the relevant OS:
    -   Windows: Either NT AUTHORITY\\SYSTEM or admin
    -   Linux and macOS: root
2.  On the System Properties page \(**All** &gt; **System properties** &gt; **All properties**\), set the **sn\_acc\_vis\_content.enable\_sam\_collection\_without\_osqueryd** property to **true**.

    **Note:** Enable this property only when all agents are version 4.1.0 or later.


## Software edition information

Starting in ACC-V version 2.3.0, edition information is supported for Adobe Acrobat and MS SQL server. In future releases, additional software will be supported. With this feature, SAM admins can get clear visibility into the editions of their installed software. Osquery commands are used to fetch the edition information which then shows in the Software Installation \[cmdb\_sam\_sw\_install\] table in the Edition Override column. For more details, see the support KB: [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0721360](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0721360)

-   **[Configure Osqueryd schedule for SAM total usage metrics](../task/import-external-pack-file-for-sam-total-usage-metrics.md)**  
SAM total usage metrics works by relying on the Osqueryd service running on the target host. Configure the Osqueryd service to run the required schedule Osquery on the host.
-   **[Configure Osqueryd logs for SAM total usage metrics](../task/configure-osquery-logs-for-sam-total-usage-metrics.md)**  
By default, Osquery supports log rotation based on size. To enable it for SAM total usage metrics and to configure the log size and rotation, you need to add specific flags for Osqueryd service.

**Parent Topic:**[Using Agent Client Collector for Visibility](acc-v-using-agent-client-collector-for-visibility.md)

