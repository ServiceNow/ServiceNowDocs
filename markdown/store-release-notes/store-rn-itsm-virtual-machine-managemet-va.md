---
title: Virtual Machine Management for Virtual Agent release notes
description: Version history for the Virtual Machine Management for Virtual Agent on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-virtual-machine-managemet-va.html
release: store
topic_type: reference
last_updated: "2021-08-19"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Virtual Machine Management for Virtual Agent release notes

Version history for the Virtual Machine Management for Virtual Agent on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.2 - August 2021**
    -   New: Topics to describe, start, stop and terminate a VM for the customers who are not using Cloud Provisioning and Governance. The new topics leverage Cloud Access Interface \(CAI\) to take action on VM provisioned on AWS.
        -   New Topics: Start VM - CAI \(Template\), Describe VM - CAI \(Template\), Stop VM - CAI \(Template\), and Terminate VM - CAI \(Template\)
        -   New Role: New role \(sn\_managevm\_va.cai\_vm\_user\) has been added to allow users to access these topics from a Virtual Agent conversation and control unauthorized actions.
    -   Changed:
        -   Provision VM: Users are only shown the type of VM instances that are available for them to request.

