---
title: Scan Engine definitions: Upgradeability
description: Scan Engine upgradeability definitions assess the ease of enhancing a ServiceNow instance or application with new features, improvements, security patches, or compatibility adjustments.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 4
breadcrumb: [View and modify Scan Engine definitions, Scan Engine definitions, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine definitions: Upgradeability

Scan Engine upgradeability definitions assess the ease of enhancing a ServiceNow instance or application with new features, improvements, security patches, or compatibility adjustments.

## Australia definitions

The following upgradeability definitions have been added for the Australia 2026 release:

|Number|Active|Level of Finding|Unique ServiceNow Product|Short Description|Business Impact|Steps to Resolve|Supporting Documentation|
|------|------|----------------|-------------------------|-----------------|---------------|----------------|------------------------|
|sn\_SE10007|1|Act| |Update Sets should contain at maximum 500 records|The risk of unsuccessful deployments will increase. This may result in unknown bugs in the production instance.|Create a new update set to continue development.|[Documentation](https://www.servicenow.com/docs/csh?topicname=system-update-sets.html)|
|sn\_SE10008|1|Suggest| |Warning: This update set is approaching the maximum allowed number of update records \(500\)|The risk of unsuccessful deployments will increase. This may result in unknown bugs in the production instance.|Consider creating a new update set and continuing development in the new update set.|[Documentation](https://www.servicenow.com/docs/csh?topicname=system-update-sets.html)|
|sn\_SE10050|1|Act| |Update Sets should not contain multiple updates to the same record|Deployment may be impacted and cause issues in production.|Set the update set value to Default on the oldest duplicate update record within the update set.|[Documentation](https://www.servicenow.com/docs/csh?topicname=get-started-update-sets.html)|
|sn\_SE10051|1|Suggest| |Update Sets should contain a meaningful description of the work contained within|Increased troubleshooting/investigation time.|Add a detailed description to the update set.|[Documentation](https://www.servicenow.com/community/developer-blog/servicenow-update-set-leading-practices-part-1/ba-p/3246473)|
|sn\_SE10064|1|Suggest| |Scoped Certification: Unintended List Layout Modification|Scoped Application certification may be delayed.|Delete the **sys\_ui\_list** record from the application that isn't intended to be promoted with the scoped application.|[Documentation](https://www.servicenow.com/community/developer-forum/best-practice-update-sets-scoped-applications-or-a-combination/m-p/2403713/page/2)|
|sn\_SE10087|1|Act| |Production instance setup as a clone target|It is possible to clone over your Production instance.|Delete the record where your Production instance is listed as the target.|[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateACloneTarget.html)|
|sn\_SE10102|1|Suggest| |Upgrade Detail records marked as Skipped|Existing functionality is more likely to produce errors and not function as expected.|Review all the upgrade detail records marked as skipped. Determine if the record can be reverted to out of box or if the custom modifications should be kept. Set the resolution field and comments \(if necessary\).|[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ResolveASkippedUpdate.html)|
|sn\_SE10117|1|Act| |Mid Servers should have unique names|Configuration data may not be updated as discovery may not run correctly.|Update the mid server name to be unique.|[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0535145)|
|sn\_SE10236|1|Suggest| |Credentials should be set to active if test is successful|Discovery schedules reliant upon the credential will not successfully return complete Configuration Item findings.|Open credential, set active to **true**, save record.|[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateCredential.html)|
|sn\_SE10239|1|Suggest| |MID Server OS - Windows|Utilization of a singular server type allows broader reach. Note if MID is in a Linux only environment, this is not applicable.|Redeploy MID on windows host.|[Documentation](https://www.servicenow.com/docs/csh?topicname=r_MIDServerSystemRequirements.html)|
|sn\_SE10246|1|Recommend| |Avoid writing business rules for event \[em\_event\] tables|Business rules that are written for alert tables \[em\_alert\] must be highly efficient or they may result in performance degradation. Instead of writing a business rule, consider whether it is more appropriate to write a job. An inefficient business rule can cause incident creation for an alert to fail and the alert impact calculation to fail.|Replace business rules targeting the **em\_event** tables with scheduled jobs, or ensure rule efficiency.|[Documentation](https://www.servicenow.com/docs/csh?topicname=r_EMBestPractice.html)|
|sn\_SE10247|1|Act| |Do not write async business rules for alert tables|Alerts may be missed, or sent later, causing critical issue resolution to be delayed|Replace async business rules targeting alert tables with before or after rules.|[Documentation](https://www.servicenow.com/docs/csh?topicname=r_EMBestPractice.html)|
|sn\_SE10262|1|Act| |Update Sets should have a unique name|Ambiguous deployment plan that may lead to production bugs.|Duplicate update sets should be removed or renamed if being used for active development.|[Documentation](https://www.servicenow.com/docs/csh?topicname=create-select-update-set.html)|
|sn\_SE10303|1|Suggest| |Enable Scripted REST API versioning|Adverse changes made to a scripted REST API can impact existing integrations and may be difficult to revert.|Enable Versioning on this Scripted Rest API using the related link on the form. Write access is required to see the link.|[Documentation](https://www.servicenow.com/docs/csh?topicname=scripted-rest-good-practices.html)|
|sn\_SE10318|1|Suggest| |Search for Package Dependencies| |Research the Update Set for its' package dependencies and determine if dependencies are available in the instance.|[Documentation](https://www.servicenow.com/docs/csh?topicname=r_CustomerUpdatesTable.html)|
|sn\_SE10417|1|Recommend| |Scan update set for updates with multiple scopes|May cause unexpected issues when promoting to higher instances.|Create a parent update set within the Global Scope, then create your children update sets within their own respective applications. Move the updates to respective applications.|[Documentation](https://www.servicenow.com/docs/csh?topicname=create-select-update-set.html)|
|sn\_SE10543|1|Suggest| |ACLs on PA tables have changed|Since Performance Analytics ACLs are preconfigured, additional attention will be required if they are changed.|Revert the ACL back to out-of-box.|[Documentation](https://www.servicenow.com/docs/csh?topicname=access-control-rules.html)|
|sn\_SE10583|1|Act| |Use of deprecated API RESTMessage \(V1\)|The API is deprecated and no longer supported.|Replace RESTMessageV1 with RESTMessageV2.|[Documentation](https://www.servicenow.com/docs/csh?topicname=c_RESTMessageV2API.html)|
|sn\_SE10615|1|Review| |Ownership Metrics|Knowledge articles without an author or group ownership can lead to a poor user experience and difficulty in maintaining article quality.|Assign an Ownership Group or Author to the knowledge articles.|[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)|

