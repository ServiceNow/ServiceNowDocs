---
title: Discovery for data-center virtualization
description: Discovery and Service Mapping Patterns identify and classify information about virtual machines discovered in a data-center.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-12-02"
reading_time_minutes: 1
keywords: [data center virtualization, virtual machine, vm discovery]
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Discovery for data-center virtualization

Discovery and Service Mapping Patterns identify and classify information about virtual machines discovered in a data-center.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

After upgrading to Discovery Admin Workspace version 1.3.1 \(August 2024 Store\), you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** and use the enhanced dashboard.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

|Label|Table Name|Field Name|
|-----|----------|----------|
|CPUs|cmdb\_ci\_vm\_instance|cpus|
|Disks|cmdb\_ci\_vm\_instance|disks|
|Disks size|cmdb\_ci\_vm\_instance|disks\_size|
|Image path|cmdb\_ci\_vmware\_instance|image\_path|
|Memory|cmdb\_ci\_vm\_instance|memory|
|Network adapters|cmdb\_ci\_vm\_instance|nics|
|State|cmdb\_ci\_vm\_instance|state|
|Template|cmdb\_ci\_vmware\_instance|template|
|vCenter Reference|cmdb\_ci\_vmware\_instance|vcenter\_ref|
|vCenter Reference UUID|cmdb\_ci\_vmware\_instance|vcenter\_uuid|

**Parent Topic:**[Operating systems discovery](../concept/c_Computers.md)

