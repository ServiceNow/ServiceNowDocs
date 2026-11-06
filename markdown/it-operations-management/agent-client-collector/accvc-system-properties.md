---
title: ACC-VC system properties
description: System properties that control how Agent Client Collector for Visibility Content \(ACC-VC\) discovers, collects, and stores data on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/accvc-system-properties.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-10-15"
reading_time_minutes: 12
keywords: [Agent Client Collector for Visibility, ACC-VC, system properties, sn\_acc\_vis\_content]
breadcrumb: [ACC-VC reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# ACC-VC system properties

System properties that control how Agent Client Collector for Visibility Content \(ACC-VC\) discovers, collects, and stores data on your instance.

All properties in this topic belong to the ACC-VC \(`sn_acc_vis_content`\) application. To view or update a property, navigate to All and enter `sys_properties.list` in the filter, and then search for the property name.

The properties are grouped by the area of ACC-VC that they affect.

## General discovery and logging properties

<table id="table-accvc-general-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.enable\_discovery\_on\_agent\_up**

</td><td>

-   Type: true \| false
-   Default value: false

 Runs discovery when an agent comes up \(the Agent Up event\).

 **Warning:** Enabling this property might cause performance issues, especially with many agents or if agents frequently go offline and come back online. The impact is greater if all agents come online at the same time.

</td></tr><tr><td>

**sn\_acc\_vis\_content.logging.verbosity**

</td><td>

-   Type: string
-   Default value: info

 Controls the logging verbosity for the ACC-VC application. Valid values are `debug`, `info`, `warn`, and `error`.

</td></tr></tbody>
</table>## File-based discovery properties

For additional file-based discovery \(FBD\) properties and how they work together, see [Agent Client Collector File-Based Discovery properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/file-based-discovery-configuration-properties.md).

<table id="table-accvc-file-discovery-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.file\_discovery.enable\_fbd\_fullscan**

</td><td>

-   Type: true \| false
-   Default value: false

 Controls which files ACC-VC sends to the instance during FBD.

 -   When `false`, ACC-VC ignores the extensions set in the configuration console table and sends only the files specified in the `sn_acc_vis_content_file_config` tableto the instance.
-   When `true`, ACC-VC recognizes the extensions set in the configuration console, even if they aren't specified in the `sn_acc_vis_content_file_config` table. If no files are listed in that table, ACC-VC retrieves all files of the specified extension type. If files are listed in that table, ACC-VC retrieves only those files.

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.fbd\_process\_scan\_enabled**

</td><td>

-   Type: true \| false
-   Default value: false

 Enables process-based FBD discovery. When set to `true`:

 -   The FBD Software Asset Management \(SAM\) Process Scan agent policy is activated. The `fbd_process_scan.rb` script runs every 5 minutes and collects the directories of running processes into the `ProcessScanPaths.ndjson` file.
-   The `processScanEnabled=true` setting is synced into the `AgentFBDWindowsParameters.json` and `AgentFBDUnixParameters.json` files, so that the `files_background.rb` script includes the process-discovered directories in its daily scan.

 For details, see [Running process-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/running-process-based-discovery.md).

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.archive\_scan\_enabled**

</td><td>

-   Type: true \| false
-   Default value: false

 Enables scanning inside ZIP and JAR archive files during FBD. When true, the agent reads the internal index of the ZIP and JAR archives in the configured scan paths and reports the files inside them, using the same SAM and File Management filtering rules as for regular files. ACC-VC doesn't extract or decompress any file content. It collects only metadata: the file name, size, extension, and path.

 The agent automatically skips archives that are larger than 500 MB, contain more than 50,000 entries, or take longer than 30 seconds to scan. It doesn't scan nested archives, which are archives inside other archives. For details, see [Archive file scanning filtering rules and limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/archive-file-scanning-reference.md).

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.enable\_glas\_hw\_collection**

</td><td>

-   Type: true \| false
-   Default value: false

 Enables the collection of Oracle hardware data for the Oracle GLAS report.

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.enable\_java\_discovery**

</td><td>

-   Type: true \| false
-   Default value: true

 Enables Java discovery in ACC-VC file-based discovery.

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.encode\_swid\_tag\_content**

</td><td>

-   Type: true \| false
-   Default value: true

 Enables Base64 encoding of SWID tag content before ACC-VC stores it on the instance.

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.fresh\_scan\_frequency\_by\_delta\_count**

</td><td>

-   Type: integer
-   Default value: 5

 Defines how often, in number of delta payload processing cycles, ACC-VC performs a fresh \(full\) scan. For example, a value of 5 means that a full scan runs after every 5 delta payloads.

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.additional\_swid\_extensions**

</td><td>

-   Type: string
-   Default value: empty

 Defines additional file extensions that FBD treats as SWID tag files, along with the built-in defaults \(`.swid`, `.swidtag`, and `.cmptag`\). The agent scans files that match these extensions for SWID tag content, instead of evaluating them for SAM or File Management discovery. The extensions that you configure are added to the defaults and never replace them.

 Separate multiple extensions with a pipe character \(`|`\). You can enter each extension as `*.ext`, `.ext`, or `ext`. ACC-VC normalizes all formats automatically. For example: `*.tag|.customtag|customtag`

 To use only the default SWID extensions, leave the value empty.

 **Warning:** Add extensions with caution. The agent scans any file that matches a configured extension only as a SWID tag file, and no longer evaluates it for SAM or File Management discovery. An extension that is too broad can cause unrelated files to be misclassified and increase the scan overhead. Don't add common, general-purpose extensions, such as `.xml`, `.txt`, or `.log`. These extensions match a very large number of unrelated files on a typical endpoint, which significantly increases the scan time and can cause performance issues on the instance.

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.mime\_type.unix**

</td><td>

-   Type: string
-   Default value: empty

 Defines the list of MIME types to scan on Unix platforms. Separate multiple MIME types with a colon \(`:`\). Don't include spaces or quotation marks. For example: `application/x-pie-executable:application/x-sharedlib:text/x-shellscript:text/x-script.python`

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.version\_skip\_extension\_list.unix**

</td><td>

-   Type: string
-   Default value: A predefined list of file extensions

 Defines the file extensions for which ACC-VC doesn't query the file version on Unix platforms. For a file with an extension in this list, ACC-VC collects the name and size and automatically skips the version.

 Separate multiple extensions with a pipe character \(`|`\). For example: `*.so|*.py|*.sh`

</td></tr><tr><td>

**sn\_acc\_vis\_content.file\_discovery.version\_skip\_extension\_list.windows**

</td><td>

-   Type: string
-   Default value: A predefined list of file extensions

 Defines the file extensions for which ACC-VC doesn't query the file version on Windows platforms. For a file with an extension in this list, ACC-VC collects the name and size and automatically skips the version.

 Separate multiple extensions with a pipe character \(`|`\). For example: `*.txt|*.var|*.json`

</td></tr></tbody>
</table>## License key discovery properties

<table id="table-accvc-license-key-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.enable\_license\_key\_discovery**

</td><td>

-   Type: true \| false
-   Default value: false

 Turns license key discovery on or off. When set to `true`, ACC-VC processes and stores license key data collected from the Windows registry and license key files discovered by file-based discovery \(FBD\) scans. For details, see [License key discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/license-key-discovery.md).

</td></tr></tbody>
</table>## Host and network properties

<table id="table-accvc-host-network-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.persist\_os\_user\_type**

</td><td>

-   Type: string
-   Default value: `local,system`

 Defines which types of operating system user data ACC-VC discovery stores. Valid values are `local` and `system`. Separate multiple values with a comma and no spaces.

</td></tr><tr><td>

**sn\_acc\_vis\_content.windows\_model\_number\_filter\_enabled**

</td><td>

-   Type: true \| false
-   Default value: false

 Controls whether ACC-VC uses the `model_number` value collected from a Windows server when it performs the Make and Model lookup to identify the hardware product model of the CI.

 -   When `false`, `model_number` is included in the lookup.
-   When `true`, `model_number` is excluded from the lookup, which helps prevent invalid product model records from being created.

 A change to the value takes effect on the next ACC-VC discovery run.

 This property affects only Windows CIs. CIs that run Linux, macOS, or any other operating system aren't affected.

</td></tr><tr><td>

**sn\_acc\_vis\_content.network\_adapter\_exclusion\_list**

</td><td>

-   Type: string
-   Default value: empty

 Defines regular expressions for the network adapter names and IP addresses to exclude from the Network Adapter and IP Address tables. For details, see [Setting exclusion lists for IPs and NICs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-v-set-exclusion-lists-for-ips-and-nics.md).

 Enter the network adapter expressions and the IP address expressions on separate lines, using `nic` and `ip_addr` as the keywords. Separate multiple expressions on the same line with a comma. Don't use a comma inside a regular expression. For example:

 ```
nic = bond0
ip_addr = 10\.196\.\d+\.\d+
```

 The regular expressions and keywords are case-sensitive. A value that doesn't follow this format is treated as an invalid regular expression, which leads to incorrect exclusion or persistence issues.

</td></tr></tbody>
</table>## User mapping and assignment properties

<table id="table-accvc-user-mapping-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.set\_assigned\_to**

</td><td>

-   Type: true \| false
-   Default value: false

 Controls whether ACC-VC overrides the **Assigned to** value of a computer CI.

 -   When `true`, ACC-VC overrides the **Assigned to** value.
-   When `false`, the existing **Assigned to** value is unchanged.

</td></tr><tr><td>

**sn\_acc\_vis\_content.assigned\_to\_user\_order**

</td><td>

-   Type: string
-   Default value: `computer_system_username,logged_in_users`

 Defines the priority order of the username sources that ACC-VC uses to set the **Assigned to** value of a computer CI. The username from the first source in the list takes precedence. Separate sources with a comma.

 Valid sources are:

 -   `computer_system_username`: The username that ACC-VC derives from the native command on a Windows machine.
-   `logged_in_users`: The logged-in users that ACC-VC gets from the osquery table.

</td></tr><tr><td>

**sn\_acc\_vis\_content.column\_name\_for\_user\_mapping**

</td><td>

-   Type: string
-   Default value: empty

 Maps a user \(the **Assigned to** value\) to an agent CI, and maps SAM usage to a user, based on the Active Directory \(AD\) domain. The value is the name of the column in the `sys_user` table that ACC-VC uses to verify the username and domain and map them to the right CI.

 -   If the value is empty, ACC-VC maps the **Assigned to** value by username only, not by domain.
-   The column can be a base system column or a custom column in the `sys_user` table.
-   The supported username and domain formats are `username@domain` and `domain\username`.
-   The domain is case-sensitive.

</td></tr></tbody>
</table>## Software discovery and usage metrics properties

<table id="table-accvc-software-usage-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.enable\_sam\_collection\_without\_osqueryd**

</td><td>

-   Type: true \| false
-   Default value: false

 When set to `true`, ACC-VC collects Software Asset Management \(SAM\) metering information without requiring configuration on Windows and macOS machines.

</td></tr><tr><td>

**sn\_acc\_vis\_content.persist\_sam\_usage\_metrics**

</td><td>

-   Type: true \| false
-   Default value: true

 Controls whether ACC-VC stores SAM-related usage information. When set to `true`, ACC-VC stores the information.

</td></tr><tr><td>

**sn\_acc\_vis\_content.sw\_categorization.enabled**

</td><td>

-   Type: true \| false
-   Default value: false

 Turns software categorization on or off. When set to `true`, ACC-VC matches newly discovered software packages against install signatures and categorizes them. For details, see [Software packages categorization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-software-categorization.md).

</td></tr><tr><td>

**sn\_acc\_vis\_content.disable\_sam\_reclamation\_rules\_for\_licensable\_softwares**

</td><td>

-   Type: true \| false
-   Default value: false

 Controls whether reclamation rules apply to licensed software when ACC-VC stores SAM usage.

 -   When `true`, ACC-VC stores SAM usage for all licensed software, with or without a defined reclamation rule. It also stores usage for any non-licensed software that has a reclamation rule defined.
-   When `false`, ACC-VC stores SAM usage according to the defined reclamation rules.

</td></tr></tbody>
</table>## SaaS usage metrics properties

<table id="table-accvc-saas-usage-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.enable\_full\_monitoring**

</td><td>

-   Type: true \| false
-   Default value: false

 Enables full monitoring for all URLs. For details on web usage collection, see [Collect web usage data using Agent Client Collector for Visibility Content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/collect-web-data-usage-accvc.md).

</td></tr><tr><td>

**sn\_acc\_vis\_content.max\_daywise\_aggregation\_domains**

</td><td>

-   Type: integer
-   Default value: 500

 Maximum number of top domains, ranked by page views, for which ACC-VC aggregates day-wise page visit data.

</td></tr><tr><td>

**sn\_acc\_vis\_content.full\_url\_discovery\_daily\_max\_rows**

</td><td>

-   Type: integer
-   Default value: 200

 Maximum number of distinct domain rows that Full URL Discovery stores each day in the agent-local `url_monitoring` table. The first domains that the agent sees each day are the ones stored. After the limit is reached for a day, ACC-VC drops new domains, and existing rows continue to update.

</td></tr><tr><td>

**sn\_acc\_vis\_content.acc\_vis\_targeted\_url\_metric\_daily\_max\_rows**

</td><td>

-   Type: integer
-   Default value: 200

 Maximum number of distinct URL rows that ACC-VC stores each day in the agent-local `acc_vis_targeted_url_metric_daily` table. The first URLs that the agent sees each day are the ones stored. After the limit is reached for a day, ACC-VC drops new URLs, and existing rows continue to update.

</td></tr><tr><td>

**sn\_acc\_vis\_content.web\_usage\_retention\_days**

</td><td>

-   Type: integer
-   Default value: 7

 Number of days that ACC-VC retains web usage data.

</td></tr><tr><td>

**sn\_acc\_vis\_content.saas\_metric\_tables\_retention\_period**

</td><td>

-   Type: integer
-   Default value: 2678400

 Retention period, in seconds, for the SaaS usage metrics tables. The default value is 31 days.

</td></tr></tbody>
</table>For the tables that ACC-VC uses to store web usage data, see [Web usage data collection tables and fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/web-usage-collection-tables.md).

## Browser extension discovery properties

<table id="table-accvc-browser-extension-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.full\_browser\_extension\_discovery**

</td><td>

-   Type: true \| false
-   Default value: false

 Controls the browser extension discovery mode. For details, see [Browser extension discovery and categorization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-browser-extension-discovery.md).

 -   When `false`, ACC-VC uses signature mode. The agent matches the discovered extensions against the active signatures and reports only the matched extensions, so the tables receive only known extensions that have a signature.
-   When `true`, ACC-VC uses full discovery mode. The agent reports every discovered browser extension. Extensions that match a signature are classified. Extensions that don't match are added to the catalog with empty classification fields.

</td></tr><tr><td>

**sn\_acc\_vis\_content.collect\_extended\_browser\_extension\_metadata**

</td><td>

-   Type: true \| false
-   Default value: false

 Controls whether agents collect extended browser extension metadata, such as manifest permissions, host access, install source and timestamps, and sideload signals, and the basic identifier, name, version, and status fields.

 -   When `false`, agents report only the basic fields. They don't fetch extended metadata, which keeps the payload smaller.
-   When `true`, agents also collect and report the extended fields, and ACC-VC stores them in the `sn_acc_vis_content_browser_extension_metadata` table.

 This property is independent of **sn\_acc\_vis\_content.full\_browser\_extension\_discovery**. That property controls which extensions are reported. This property controls whether the reported extensions include the extended fields.

</td></tr></tbody>
</table>## TLS/SSL certificate discovery properties

<table id="table-accvc-tls-ssl-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.tls\_ssl\_scanner\_ports**

</td><td>

-   Type: string
-   Default value: `443,8443,9443,636,993,995,989,990,25,110,143,389,21,587`

 Ports that ACC-VC scans for SSL certificates.

</td></tr><tr><td>

**sn\_acc\_vis\_content.tls\_ssl\_scan\_all\_open\_ports**

</td><td>

-   Type: true \| false
-   Default value: false

 Enables certificate discovery on all available open ports.

</td></tr><tr><td>

**sn\_acc\_vis\_content.tls\_ssl\_keep\_original\_cert**

</td><td>

-   Type: true \| false
-   Default value: false

 Whether the agent TLS/SSL certificate discovery returns the original certificate.

</td></tr></tbody>
</table>## Non-persistent VDI properties

The following properties apply only to Windows non-persistent virtual desktop infrastructure \(NPVDI\) endpoints. For the full description of each property, see [ACC-VC NPVDI system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/accvc-npvdi-properties.md).

|Property|Description|
|--------|-----------|
|**sn\_acc\_vis\_content.np\_vdi.cache\_installed\_software\_enabled**|Caches the full installed software scan on NPVDI endpoints so that it runs only one time for each golden image.|
|**sn\_acc\_vis\_content.np\_vdi.enhanced\_discovery\_skip\_modules**|Lists the **Enhanced Discovery** modules to skip on NPVDI endpoints.|

**Parent Topic:**[Agent Client Collector for Visibility Content reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/agent-client-collector-for-visibility-references.md)

