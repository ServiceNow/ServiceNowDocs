---
title: Upgrade planning checklist
description: Plan and track the activities related to your ServiceNow instance upgrade. To help ensure that you complete all the tasks for a successful upgrade, follow the step-by-step instructions in the upgrade planning checklist to track and plan the upgrade.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Prepare your upgrade, Australia release notes]
---

# Upgrade planning checklist

Plan and track the activities related to your ServiceNow instance upgrade. To help ensure that you complete all the tasks for a successful upgrade, follow the step-by-step instructions in the upgrade planning checklist to track and plan the upgrade.

Some optional steps may not be appropriate depending on the number of instances, customizations, and so forth. Mark the ones you do not need in the **N/A** column.

**Tip:** To download a PDF version of this checklist, click [here](https://downloads.docs.servicenow.com/enus/paris/upgrade/servicenow-upgrade-planning-checklist.pdf).

The process for completing steps for self-hosted customers may vary \(for example, requesting an instance clone or upgrades\). These differences must be considered during planning.

<table id="table_phq_dps_kx"><tbody><tr><td>

Customer name:

</td><td>

 

</td></tr><tr><td>

Product instance name:

</td><td>

https://\[instancename\].service-now.com

</td></tr><tr><td>

Other instance names

</td><td>

https://\[instancename\].service-now.com https://\[instancename\].service-now.com

</td></tr></tbody>
</table><table id="table_dsg_w5w_yt"><thead><tr><th>

 

</th><th>

Description

</th><th>

Yes

</th><th>

No

</th><th>

N/A

</th></tr></thead><tbody><tr><td class="sub-head" colspan="5">

Phase 1 - Read the release notes and plan your upgrade

</td></tr><tr><td>

[1](task/upgrades-phase-1.md)

</td><td>

Review the [Australia release notes](../family-release-notes.md) for the target ServiceNow feature release and patch, in addition to product and release documentation.

 For Australia -specific upgrade considerations, see [Pre- and post-upgrade tasks for various products](reference/upgrade-and-migration-tasks.md).

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td class="sub-head" colspan="5">

Phase 2 - Complete these planning tasks.

</td></tr><tr><td>

2

</td><td>

Confirm which ServiceNow instances are in-scope for upgrade.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

3

</td><td>

Confirm the instance hosting model. For example, ServiceNow cloud, on-premise, or off-premise.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

4

</td><td>

Based on the [Australia release notes](../family-release-notes.md) and other release materials, determine new functionality or notable changes that need to be validated after the upgrade.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

5

</td><td>

Confirm plans to enable or disable features introduced in the new product release.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

6

</td><td>

Review the [Browser support](../../administer/navigation-and-ui/reference/browser-support.md) to determine browser prerequisites. For example, versions and types supported, and additional requirements for new UI versions. Compare these supported browsers to your corporate standard and identify any gaps.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

7

</td><td>

Create a project plan for cloning, upgrading, and testing.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

8

</td><td>

Identify the core team of testers, power users, and key stakeholders required to validate functionality in the ServiceNow instances before and after the upgrade.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

9

</td><td>

Confirm whether there are any change freeze windows impacting the timing for environment clones or upgrades. For example, end quarter.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

10

</td><td>

Confirm which of the following situations applies to your ServiceNow non-production instances:1.  Development and testing can be frozen until the production upgrade is completed.
2.  Continued development \(and testing\) activities need to continue in a non-production instance while upgrade, remediation, and testing activities are performed in parallel on another instance.
3.  Once the final upgrade to your production instance is complete, the cloning of your final production instance to your non-production instance will wait until after the production upgrade is complete.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

11

</td><td>

Confirm the availability of other systems required for integration testing \(key resources and environments\).

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

12

</td><td>

Confirm whether there are any restrictions in which ServiceNow instances can be used for integration testing. For example, an interfacing system is only set up to access a specific ServiceNow test instance.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

13

</td><td>

Confirm the testing scope and approach.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

14

</td><td>

Create a comprehensive test plan including test cases for all core instance functionality and integrations.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

15

</td><td>

Confirm the method for tracking any defects identified during testing.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

16

</td><td>

Create a high-level implementation plan that covers:

-   the sequence and timing to upgrade non-production and production instances
-   the instances to be cloned
-   the instance to be used for integration testing.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

17

</td><td>

Confirm whether there are any change freeze windows impacting the timing for environment clones or upgrades. For example, end quarter.

Responsible: ServiceNow or Customer

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

18

</td><td>

Determine whether existing internal training materials, Knowledge Base articles in the customer instance, or other supporting documentation must be updated to align with the upgraded version. For example, changes in functionality or user interface.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

19

</td><td>

**Optional:** Schedule the [ServiceNow Configuration Review](http://www.servicenow.com/services/production-readiness-services.html), which provides recommendations to align the customer configurations with ServiceNow best practices. **Note:**

There may be a service charge and require professional services engagement.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[20](task/upgrades-phase-2.md#Phase3Step1Clone)

</td><td>

On your production instance, create a system clone and select your development instance as the **Target instance**. Notify impacted users and internal stakeholders of the scheduled date/time for cloning \(from production\) and upgrade of the non-production instance.

**Note:**

It is important to test on a system that reflects the production instance as closely as possible. If your non-production and production instances are the same size, include the production audit log and the attachment data, and ensure that you have deselected the exclude options.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td class="sub-head" colspan="5">

Phase 3 - Verify your upgrade configurations and schedule the development instance upgrade in Now Support

</td></tr><tr><td>

[21](task/upgrades-phase-3.md#Phase3Step1CheckUpgradeJob)

</td><td>

Check the configuration of the **Check distribution for possible upgrade** scheduled job to view how often and when it runs.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[22](task/upgrades-phase-3.md#Phase3Step2UpgradeSysTrigger)

</td><td>

Verify that the **Check distribution for possible upgrade** sys\_trigger is set properly for upgrading.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[23](task/upgrades-phase-3.md#Phase3Step3CheckUpgradeSysTrigger)

</td><td>

Verify that the **Check database for possible upgrade** sys\_trigger is set properly for upgrading.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[24](task/upgrades-phase-3.md#Phase3Step4ScheduleUpgrade)

</td><td>

Schedule the upgrade in Now Support.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[25](task/upgrades-phase-3.md#Phase3Step5RequestEnt)

</td><td>

If applicable, request a version entitlement.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td class="sub-head" colspan="5">

Phase 4 - Upgrade and validate the development instance

</td></tr><tr><td>

[26](task/upgrades-phase-4.md#Phase4Step1Validate)

</td><td>

Using the Upgrade Monitor, monitor the upgrade to your instance and validate that the upgrade to your development instance is complete.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[27](task/upgrades-phase-4.md#Phase4Step2SkippedList)

</td><td>

After the upgrade for your development instance is complete, [process the skipped records list](https://www.servicenow.com/docs/access?context=uc-process-skipped-records&version=australia&pubname=australia-platform-administration&ft:locale=en-US) in the Upgrade Monitor.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[28](task/upgrades-phase-4.md#Phase4Step3UpdateSets)

</td><td>

Identify your update sets.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[29](task/upgrades-phase-4.md#Phase4Step4FunctionalTesting)

</td><td>

Before and after upgrading, conduct smoke tests on your development instance. Use your comprehensive test plan to perform functional testing.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td class="sub-head" colspan="5">

Phase 5 - If applicable: Upgrade and validate your other non-production instances, such as your test instance

</td></tr><tr><td>

[30](task/upgrades-phase-2.md#Phase3Step1Clone)

</td><td>

On your production instance, create a system clone and select your development instance as the **Target instance**.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[31](task/upgrades-phase-5.md)

</td><td>

Schedule the non-production upgrade in Now Support and verify your upgrade configurations.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[32](task/upgrades-phase-5.md)

</td><td>

Validate that the upgrade to your non-production instance is complete.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[33](task/upgrades-phase-5.md)

</td><td>

Install any optional plugins that were installed on your development instance.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[34](task/upgrades-phase-5.md)

</td><td>

Install any custom applications and post-upgrade fix scripts that you need.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[35](task/upgrades-phase-5.md)

</td><td>

Install update sets.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[36](task/upgrades-phase-5.md)

</td><td>

Perform functional testing and monitor the performance of your instance.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td class="sub-head" colspan="5">

Phase 6 - Prepare to upgrade the production instance

</td></tr><tr><td>

37

</td><td>

Confirm sign-off from IT and Business stakeholders that all non-production instance defects have been fixed and validated in update sets.

Responsible: Customer

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

38

</td><td>

Confirm the core team of key stakeholders required to validate functionality in the ServiceNow instance after the production upgrade.

Responsible: Customer

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

39

</td><td>

Confirm coverage for Day 1 support post-upgrade.

Responsible: Customer

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

40

</td><td>

Create a Production Upgrade Implementation Plan that includes all upgrade steps, roles and responsibilities, communication plans, key contacts, support coverage for Day 1, and so forth.

Responsible: Customer

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

41

</td><td>

Schedule a walkthrough and sign-off of the Implementation Plan with key stakeholders and the core team.

Responsible: Customer

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

42

</td><td>

Submit and obtain approvals for change records as required by the organization change process.

Responsible: Customer

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

43

</td><td>

Send a communication to key stakeholders and end users with details for the production upgrade outage, new features, and so forth.

Responsible: Customer

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[44](task/upgrades-phase-6.md#Phase6Step1BenchmarkPerf)

</td><td>

Profile the performance of your instance before upgrading.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[45](task/upgrades-phase-6.md#Phase6Step2PerfDashboard)

</td><td>

Use the ServiceNow Performance homepage to document the performance of your instance before the upgrade.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[46](task/upgrades-phase-6.md#Phase6Step3FunctionalTesting)

</td><td>

On your clone, perform functional testing and monitor the performance of your instance.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td class="sub-head" colspan="5">

Phase 7 - Upgrade the production instance

</td></tr><tr><td>

[47](task/upgrades-phase-7.md#Phase7Step1ScheduleUpgrade)

</td><td>

Schedule the upgrade in Now Support.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[48](task/upgrades-phase-7.md#Phase7Step2RequestEntitlement)

</td><td>

If applicable, request a version entitlement.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[49](task/upgrades-phase-7.md#Phase7Step3VerifyUpgrade)

</td><td>

Monitor the upgrade to your instance and validate that the upgrade to your production instance is complete.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[50](task/upgrades-phase-7.md#Phase7Step4UpdateSets)

</td><td>

Apply any update sets and post-upgrade fix scripts that you have.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr><tr><td>

[51](task/upgrades-phase-7.md#Phase7Step5ValidateTest)

</td><td>

Validate and test your instance by conducting user acceptance testing \(UAT\). Verify with all key stakeholders that the system is performing properly after production upgrade, and key functionality is available.

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td><td>

![](../image/checkbox.png)

</td></tr></tbody>
</table>