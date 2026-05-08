---
title: Configuring contract summarization for Contract Management Pro
description: Configure the smart documents skill in Now Assist in Document Management to generate a contract summary in Contract Management Pro.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Contract summarization, Summarize contract, Ask Now Assist]
breadcrumb: [Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configuring contract summarization for Contract Management Pro

Configure the smart documents skill in Now Assist in Document Management to generate a contract summary in Contract Management Pro.

You can summarize contracts, generate frequently asked questions \(FAQs\), and retrieve specific information from contracts in Contract Management Pro by using the Smart Documents feature.

To enable this feature in Contract Management Pro, do the following:

1.  Activate the smart documents skill in Now Assist in Document Management. For more information, see Configure the Smart Documents Skill for Now Assist in Document Management.
2.  To enable contract summarization for contract documents, supporting documents, and signed contracts, add the following tables in the **Define availability** tab of smart documents skill.
    -   Contract \[ast\_contract\]
    -   Contract Document Revision \[sn\_cm\_core\_document\_revision\]
    -   Legal Contracts Repository \[sn\_lg\_cnt\_repository\]
    -   Supporting File \[sn\_cm\_core\_supporting\_file\]
3.  To enable users to access the contract summarization feature, add the following roles in the **Define access** tab of the smart documents skill.
    -   Contracts Core administrator \[sn\_cm\_core.contract\_admin\]
    -   Contracts Core user \[sn\_cm\_core.contract\_user\]
    -   Contracts Core fulfiller \[sn\_cm\_core.contract\_fulfiller\]
    -   Contract reviewer \[sn\_cm\_core.contract\_reviewer\]
    -   Contract manager \[contract\_manager\]
    -   Legal contract fulfiller \[sn\_lg\_cnt.contract\_fulfiller\]
    -   Legal contract administrator \[sn\_lg\_cnt.contract\_admin\]
    -   Legal contract owner \[sn\_lg\_cnt.contract\_owner\]
4.  Enable the Now Assist panel for your instance. For more information, see Activate the Now Assist panel standard chat.

**Parent Topic:**[Configure additional features in Contract Management Pro](../concept/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace](../concept/cncore-conf-cntrct-wrkspc.md)

[Configure signature pause duration when modifying signatories](cncore-pause-sig-property.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Enable keyword search for contract templates](cncore-enable-search-cont-tmplts.md)

[Configure conditions to send reminder notifications for expiring contracts](cncore-config-rem-exp-cont.md)

[Copy fields from parent request to amendment request](cncore-cpy-fld-parent-amedreq.md)

[Manage notifications in Contract Management Pro](../concept/cmpro-manage-notifications.md)

