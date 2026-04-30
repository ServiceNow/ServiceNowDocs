---
title: Set up ServiceNow Spotlight
description: Set up ServiceNow Spotlight to start using and getting the benefits of this feature. The Spotlight feature automatically calculates the execution priority of the automation requests.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with ServiceNow Spotlight feature, Configure, Automation Center, Workflow Data Fabric]
---

# Set up ServiceNow Spotlight

Set up ServiceNow Spotlight to start using and getting the benefits of this feature. The Spotlight feature automatically calculates the execution priority of the automation requests.

## Before you begin

Install ServiceNow® Spotlight. For more information, see the ServiceNow Spotlight documentation.

Role required: admin, pa\_spotlight

## Procedure

1.  Turn on the usage of ServiceNow Spotlight by setting the system property, **sn\_ac.use.spotlight.score.for.requests**, to **True**.

    `/sys_properties.do?sys_id=2df8d6a3c3651110995486d91840dd65`

2.  If there are existing automation requests, execute the fix script: Initial setup of Automation Request Rank.

    /sys\_script\_fix\_list.do?sysparm\_query=nameLIKEsetup%20of%20automation%20request

    **Note:** At the end of this step, ideally there should be no records in this URL: `/sn_ac_automation_request_list.do?sysparm_query=rankISNOTEMPTY%5EstateNOT%20IN3000%2C6000`

3.  Execute the Spotlight group: **Automation request group**.

    To do so, select the **Execute Now** button in the Spotlight group page. This action populates the Spotlights related list at the bottom of that Spotlight group page. `/spotlight_groups.do?sys_id=e037711dc3a11110995486d91840dd03`

4.  Copy the initially computed scores to the requests using the scheduled script execution: **Automation Center: Copy spotlight score into request**.

    To do so, select the **Execute Now** button in the Scheduled Script Execution page. `/sysauto_script.do?sys_id=d361d79dc3a11110995486d91840dd37`


**Parent Topic:**[Working with ServiceNow Spotlight feature](../concept/spotlight-ac.md)

