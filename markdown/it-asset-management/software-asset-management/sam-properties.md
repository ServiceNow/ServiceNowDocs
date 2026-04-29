---
title: Software Asset Management properties
description: You can set default reconciliation properties such as grouping and reconciliation debugging.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Software Asset Management properties

You can set default reconciliation properties such as grouping and reconciliation debugging.

These properties are available for the Software Asset Management application.

To access these properties, navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Properties**.

<table id="table_ygc_2lb_dbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select the default Group setting for the weekly run of reconciliationcom.snc.samp.recon.group

</td><td>

Determines how rights and software installations are grouped during reconciliation.

 Values \(default is **None**\):

-   **Company**
-   **Cost Center**
-   **Country**
-   **Department**
-   **Region**

</td></tr><tr><td>

SAM Workspace License operations list count limitsn\_sam\_workspace.sam\_license\_operations\_list\_count

</td><td>

Enables setting up a threshold limit to show the count of software asset records on the License operations view. SAM administrator can set the value of the threshold limit as required.Value is set to **5000000**. If there are less than five million records, then the exact count of software installation records is shown. If there are more than five million records, then the count is shown as 5000000+.

</td></tr><tr><td>

Select the default Subgroup setting for the weekly run of reconciliationcom.snc.samp.recon.subgroup

</td><td>

Determines the secondary grouping for rights and software installations during reconciliation.

 Except for `None`, group and subgroup values must be different.

 Values \(default is **None**\):

-   **Company**
-   **Cost Center**
-   **Country**
-   **Department**
-   **Region**

</td></tr><tr><td>

Run reconciliation with all available custom license metricscom.snc.samp.recon.enablecustommetrics

</td><td>

Enables custom license metrics when running reconciliation. If you have a custom license metric configured, it is not applied when this property is set to **No**. The default is **Yes**.

</td></tr><tr><td>

Enable debugging of reconciliation results. Note that enabling debugging will have an impact on performance.com.snc.samp.debug

</td><td>

Enables debugging of reconciliation results to troubleshoot a result. The default is **No**.Additionally, this property also triggers logging for on-premise import debugging.

</td></tr><tr><td>

Automatically create software models for all 'licensable' productscom.snc.samp.automaticsmrcreation

</td><td>

Automatically creates a software model, in a non-compliant state, for any unlicensed installations, subscriptions, or options \(of licensable products\) in the Product Results list that don’t have an entitlement.The new software model and results are used to show the unlicensed count in the License Position Report.

 **Note:** For more information on automatically creating software models, see [Automatic creation of software models](../concept/duplicate-sw-models.md).

</td></tr><tr><td>

Automatically create software model results for unlicensed products during software asset reconciliationcom.snc.samp.unlicensed\_smr\_creation

</td><td>

Disables software model result creation for unlicensed software models. Software model results continue to be created for software models that have valid entitlements. The default value is **False**. You can modify the value using system properties configuration. When the property is set to **True**, the software model results get created for software models that don’t have entitlements.

</td></tr><tr><td>

Select the level of aggregation for reconciling licenses for Oracle databases and WebLogic servers on VMware com.snc.samp.oracle.reconlevel

 **Note:** This property is available only if you have activated the Software Asset Management publisher pack for Oracle.

 **Note:** This property supports domain separation using the domain separation application properties for Software Asset Management. See [Set up domain-specific reconciliation properties for Oracle](../task/define-application-properties-oracle.md) for more details.

</td><td>

Level of aggregation that is used for reconciling Oracle Database and WebLogic Server licenses on VMware virtualization technology. Software Asset Management supports the following aggregation levels:-   **ESX**: The **ESX** aggregation level considers all processor cores on the ESX host.
-   **ESX cluster** \(default value\): The **ESX cluster** aggregation level considers all processors on every ESX server within a cluster.
-   **vCenter\(s\)**: The **vCenter\(s\)** aggregation level considers all processor cores on every ESX server.

If you select this aggregation level, licensing calculations are based on the ESXi version that you’re using in your VMware virtual environment. See [Oracle Database and WebLogic Server licensing in soft-partitioned environments](../concept/oracle-licensing-soft-partitioned-environments.md) for more information on the supported ESXi versions.


</td></tr><tr><td>

Use host affinity for reconciling licenses for Oracle databases and WebLogic servers on VMware at the vCenter\(s\) aggregation levelcom.snc.samp.oracle.hostaffinityenabled

 **Note:** This property is available only if you have activated the Software Asset Management publisher pack for Oracle.

 **Note:** This property supports domain separation by using the domain separation application properties for Software Asset Management. See [Set up domain-specific reconciliation properties for Oracle](../task/define-application-properties-oracle.md) for more details.

</td><td>

Enables the Software Asset Management application to account for VM-Host affinity rules when reconciling Oracle Database and WebLogic Server licenses within VMware vCenter Server instances. This property is applicable only if you set the aggregation level for Oracle reconciliation to **vCenter\(s\)** in the **Select the level of aggregation for reconciling licenses for Oracle databases and WebLogic servers on VMware** property.VM-Host affinity rules enable you to specify the physical ESXi hosts on which your virtual machines can run. If provisions are made for VM-Host affinity rules in your Oracle license agreement, you can lower your licensing obligations by accounting for these rules when licensing your Oracle Database and WebLogic servers.

</td></tr><tr><td>

Automatically create software models for all 'not licensable' productscom.snc.samp.automaticsmcreation

</td><td>

Automatically creates a software model, in a non-compliant state, for any unlicensed installations \(of not-licensable products\) in the Product Results list.The new software model is used by Application Portfolio Management.

 Default is No.

</td></tr><tr><td>

Enter the name of the true/false field added to cmdb\_ci\_hardware table to exclude software installed on selected devices from Software Asset Managementcom.snc.samp.exclude\_device\_flag

</td><td>

Excludes the software installed on devices \(from the Software Asset Management application\) where the Exclude from SAM column is set to true when you enter the column name, exclude\_from\_sam.

</td></tr><tr><td>

Enter the license period \(in days\) to be considered during reconciliation, for applications published on Citrix environmentcom.snc.samp.citrix.app.license.period

 **Note:** This property is available only if you have activated the Software Asset Management publisher pack for Citrix.

</td><td>

Indicates the license period \(in days\) for Citrix applications to be considered during reconciliation. Default is 90 days.

</td></tr><tr><td>

Enter the timeout period \(in days\) to resolve reclamation errors before the reclamation flow moves to the Closed canceled statesam\_reclamation\_flow\_error\_timeout

</td><td>

Indicates the timeout period \(in days\) to resolve reclamation errors before the reclamation flow moves to the Closed canceled state.The default value is 30 days.

</td></tr><tr><td>

Enter the period \(in days\) to be considered for peak usage consumption, for engineering applications.com.snc.samp.eng.app.peak.usage.period

</td><td>

Indicates the period \(in days\) for engineering applications to be considered for peak usage consumption. The default value is 30 days and only a user with the sam\_admin role can update this field.

</td></tr><tr><td>

Enter the number of scheduled jobs to run in parallel for reconciliation.com.snc.samp.recon.max\_workers

</td><td>

Indicates the number of scheduled jobs that run in parallel to reconciliation. Several scheduled jobs run reconciliation for different publishers simultaneously.

</td></tr><tr><td>

Indicates whether Wide-Net Normalization is enabled on the instance. If enabled, Wide-Net Normalization rules/patterns are applied on discovery models that haven’t been fully normalized by regular package normalization rules.com.snc.samp.wide\_net\_normalization.enabled

</td><td>

Enables wide-net normalization to be performed on discovery models. This property is enabled by default. Wide-net normalization is performed only on discovery models that couldn’t be normalized using content rules.

 Only users with an admin role can modify the property.

</td></tr><tr><td>

Enable ML Normalization for discovered software.com.snc.samp.enable.ml\_normalization

</td><td>

Enables machine learning normalization to be performed on discovery models. This property is enabled by default. Machine learning normalization is performed only on discovery models that couldn’t be normalized using content rules.

 Only users with an admin role can modify the property.

</td></tr><tr><td>

Enter the threshold period \(in days\) after which billing data pulled from Cloud is considered old. This affects the license type confidence.com.snc.samp.sam\_ci\_billing\_threshold

</td><td>

Indicates the threshold period, based on the number of days after which the billing data that is pulled from Cloud Insights is considered old. Cloud Insights is used to determine the license type for SQL Server installed on AWS.​ The default value is 30 days and this property is activated by default.

</td></tr><tr><td>

Red Hat Enterprise Linux Server for Virtual Datacenters license cost optimization threshold**Note:** This property is available only if you have activated the Software Asset Management publisher pack for IBM.

</td><td>

Determines whether you should use RHEL Server or RHEL for Virtual Datacenters licenses for your RHEL deployment.

 The default threshold value is 3.2. This value is based on the ratio of the current RHEL Server subscription list price to the current RHEL for Virtual Datacenters subscription list price. If your entitlements contain different pricing for these products, you can calculate this value by dividing your RHEL for Virtual Datacenters subscription price by your RHEL Server subscription price.

 See [Software Asset Management for Red Hat Enterprise Linux](../concept/rhel-publisher-pack.md) for more information about how you can use this threshold value to determine the most optimal license type for your RHEL deployment.

</td></tr><tr><td>

Microsoft Windows Server for Datacenter license cost optimization threshold com.snc.samp.windowserver.license.threshold

**Note:** This property is available only if you have activated the Software Asset Management publisher pack for Microsoft.

</td><td>

Determines whether it’s more cost-effective to license the physical hosts or virtual machines \(VMs\) within your Microsoft Windows Server clusters based on the cost ratio between Microsoft Windows Server Datacenter Edition licenses and Microsoft Windows Server Standard Edition licenses.

 Based on the current list price of each license type, the default cost ratio value is 4.59. If your entitlements contain different pricing for these license types, you can modify this value by dividing the average price of your Microsoft Windows Server Datacenter Edition licenses by the average price of your Microsoft Windows Server Standard Edition licenses.

</td></tr><tr><td>

Default Region for IBM Devicessn\_samp\_ibm\_lic.default\_region

**Note:** This property is available only if you have activated the Software Asset Management publisher pack for IBM and installed the IBM License Compliance for Software Asset Management application. For details on how to install the application, see [Request the IBM License Compliance for Software Asset Management application for Authorized Software Asset Management Provider \(ASP\) integrations](../task/request-ibm-license-compliance-sam-application.md).

</td><td>

Automatically associates physical hosts with a default region if they aren’t already associated with one. IBM license usage can be calculated only for physical hosts that are associated with a region.

 The default value is **North America and South America**.

</td></tr><tr><td>

Connect to ILMT usingsn\_samp\_ibm\_lic.ilmt\_api\_version

**Note:** This property is available only if you have activated the Software Asset Management publisher pack for IBM.

</td><td>

Indicates which version of the IBM License Metric Tool \(ILMT\) or BigFix Inventory integration APIs you’re using to create a connection between your IBM servers and the ServiceNow AI Platform platform.

</td></tr><tr><td>

Ratio of the entitlement cost of a Microsoft SQL Server Standard with Software Assurance to the cost of Microsoft SQL Server Enterprise with Software Assurancecom.snc.samp.sqlserver.standard\_sa.to.enterprise\_sa.cost.ratio

**Note:** This property is available only if you have activated the Software Asset Management publisher pack for Microsoft.

</td><td>

Determines whether it’s more cost-effective to license the physical hosts or virtual machines \(VMs\) within your Microsoft SQL Server clusters based on the cost ratio between Microsoft SQL Server Standard Edition licenses with Software Assurance and Microsoft SQL Server Enterprise Edition licenses with Software Assurance.

 Based on the current list price of each license type, the default cost ratio value is 0.25. If your entitlements contain different pricing for these license types, you can modify this value by dividing the price of your Microsoft SQL Server Standard Edition licenses with Software Assurance by the price of your Microsoft SQL Server Enterprise Edition licenses with Software Assurance.

</td></tr><tr><td>

Ratio of the entitlement cost of a Microsoft Software Assurance entitlement to the cost of a Microsoft Non-Software Assurance entitlementcom.snc.samp.ms.sa.to.nonsa.cost.ratio

**Note:** This property is available only if you have activated the Software Asset Management publisher pack for Microsoft.

</td><td>

Determines whether it’s more cost effective to use licenses with or without Microsoft Software Assurance on your Microsoft SQL Server clusters. The Software Asset Management application makes this determination based on the cost ratio between Microsoft SQL Server licenses with Software Assurance and without Software Assurance.

 Based on the current list price of each license type, the default cost ratio value is 1.25. If your entitlements contain different pricing for these license types, you can modify this value by dividing the price of your Microsoft SQL Server licenses with Software Assurance by the price of your Microsoft SQL Server licenses without Software Assurance.

</td></tr><tr><td>

com.snc.samp.use\_lifecycle\_approximation

</td><td>

Determines whether to include approximate life cycle dates when generating the life cycle report. This property is enabled by default.

 When selected, this property includes Software Product Lifecycle records that have the **Lifecycle Code** field populated when the Software Lifecycle Report is generated.

</td></tr><tr><td>

com.snc.samp.generate.calculated.lifecycles

</td><td>

Creates calculated lifecyles. To enhance lifecycle coverage beyond approximated lifecycle data, the system calculates EOS, EOES, and EOL dates by applying software lifecycle averages, measured in months, from the GA dates.

 When selected, this property enables generating calculated lifecycle dates based on Lifecycle averages defined for either the product, publisher, or industry averages.

</td></tr><tr><td>

com.snc.samp.manage.published.products

</td><td>

Enables you to publish software products in the phase-wise Software Asset Management implementation and also remove the published software products. The default value of this property is **false**. By setting the value of this property to **true**, you can view reports and dashboards only related to the software products that you manage in a phase-wise implementation of Software Asset Management in the following views of the Software Asset Workspace:-   [Software asset overview](../concept/sam-workspace-landing.md)
-   [License usage view](../concept/sam-workspace-workbench.md)

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

