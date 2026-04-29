---
title: Class criteria in Cloud vs Non-cloud resources chart in CMDB Workspace
description: The Cloud vs Non-cloud resources chart provides counts for several key classes. The chart uses different classes and relationship criteria for each class to determine which resources count as cloud and which count as non-cloud.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Reference, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Class criteria in Cloud vs Non-cloud resources chart in CMDB Workspace

The Cloud vs Non-cloud resources chart provides counts for several key classes. The chart uses different classes and relationship criteria for each class to determine which resources count as cloud and which count as non-cloud.

The Cloud vs Non-cloud resources chart shows in the CI overview tile in the [CMDB Workspace store app](../concept/cmdb-workspace.md).

<table id="table_qx1_pfn_nwb"><thead><tr><th>

 

</th></tr></thead><tbody><tr><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]:

-   Cloud:

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] -&gt; \(Hosted on::Hosts\) -&gt; Datacenter class \(one of the [configured cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\) -&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\]

-   Non-Cloud:

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] -&gt; \(Hosted on::Hosts\) -&gt; Datacenter class \(one of the [configured non-cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\)

-   Total: Equals the record count in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table \(unless there are Virtual Machine Instance records without any relationships\)

</td></tr><tr><td>

Server \[cmdb\_ci\_server\]:

-   Cloud:

Server \[cmdb\_ci\_server\] -&gt; \(Virtualized by::Virtualizes\) -&gt; Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] -&gt; \(Hosted on::Hosts\) -&gt; Datacenter \(one of the [configured cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\) -&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\]

-   Non-Cloud:

Server \[cmdb\_ci\_server\] -&gt; Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] -&gt; Datacenter class \(one of the [configured non-cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\)

OR

Server \[cmdb\_ci\_server\] has no relationships with Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

-   Total: Equals the record count in the Server \[cmdb\_ci\_server\] table \(unless there are Server records without any relationships\)

</td></tr><tr><td>

Application \[cmdb\_ci\_appl\]:

-   Cloud:

Application \[cmdb\_ci\_appl\] -&gt; \(Runs on::Runs\) -&gt; Server \[cmdb\_ci\_server\]-&gt; \(Virtualized by::Virtualizes\) -&gt; Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] -&gt; \(Hosted on::Hosts\) -&gt; Datacenter \(one of the [configured cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\) -&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\]

OR

Application \[cmdb\_ci\_appl\] -&gt; \(Hosted on::Hosts\) -&gt; Datacenter class \(one of the [configured cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\)-&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\]

-   Non-Cloud:

Application \[cmdb\_ci\_appl\] -&gt; Server \[cmdb\_ci\_server\] -&gt; Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] -&gt; Datacenter Datacenter class \(one of the [configured non-cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\)

OR

Application \[cmdb\_ci\_appl\] -&gt; Server \[cmdb\_ci\_server\] -&gt; no relationship with Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

-   Total: Equals the sum of Cloud + Non-Cloud \(not the record count in the Application \[cmdb\_ci\_appl\] table\)

</td></tr><tr><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]:

-   Cloud:

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] -&gt; \(Hosted on::Hosts\) -&gt; Datacenter \(cloud logical data center\) -&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\]

-   Non-Cloud:

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] -&gt; Datacenter \(non-cloud logical datacenter\)

OR

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] -&gt; no relationship with -&gt; Datacenter

-   Total: Equals the record count in the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table \(unless there are Kubernetes Cluster records without any relationships\)

</td></tr><tr><td>

Database Instance \[cmdb\_ci\_db\_instance\]:

-   Cloud:

Database Instance \[cmdb\_ci\_db\_instance\] -&gt; \(Runs on::Runs\) -&gt; Server -&gt; \(Virtualized by::Virtualizes\) -&gt; Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] -&gt; \(Hosted on::Hosts\) -&gt; Logical Datacenter \(one of the [configured cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\)-&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\]

OR

Database Instance \[cmdb\_ci\_db\_instance\] -&gt; Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] \(one of the [configured cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\)-&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\]

-   Non-Cloud:

Database Instance \[cmdb\_ci\_db\_instance\] -&gt; Server \[cmdb\_ci\_server\] -&gt; Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] -&gt; datacenter \(non-cloud logical datacenter\)

OR

Database Instance \[cmdb\_ci\_db\_instance\] -&gt; Server \[cmdb\_ci\_server\] with no relationship -&gt; Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

-   Total: Sum of Cloud + Non-cloud \(can be less than total number of records, subtracting the badly created records\)

</td></tr><tr><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]:

-   Cloud:

cmdb\_ci\_storage\_volume -&gt; \(Hosted on::Hosts\) -&gt; Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] \(one of the [configured cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\)-&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\]

-   Non-Cloud:

cmdb\_ci\_storage\_volume -&gt; Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] \(one of the [configured non-cloud datacenters](../task/cmdb-workspace-config-datacenter.md)\)

OR

cmdb\_ci\_storage\_volume -&gt; no relationships with Datacenter


</td></tr><tr><td>

Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]:

-   Cloud:

Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\] -&gt; \(Hosted on::Hosts\) -&gt; Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] -&gt; \(Hosted on::Hosts\) -&gt; Cloud Service Account \[cmdb\_ci\_cloud\_service-account\] \(requires [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md)\)

-   Non-Cloud:

N/A \(This table can never have non cloud records\)


</td></tr><tr><td>

Service Accounts \[cmdb\_ci\_cloud\_service\_account\]:

-   Cloud:

datacenter\_type attribute is populated with correct datacenter class

-   Non-Cloud:

N/A \(This table can never have non-cloud records\)


</td></tr></tbody>
</table>**Parent Topic:**[CMDB Workspace reference](../concept/reference-cmdb-workspace.md)

