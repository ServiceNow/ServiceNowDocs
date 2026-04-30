---
title: Generate group approvals for domain separated requests
description: Configure Workflow Studio to generate approvals for all members of a group or to restrict approvals to only group members who are visible from the domain of the request.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Domain separation and Workflow Studio, Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Generate group approvals for domain separated requests

Configure Workflow Studio to generate approvals for all members of a group or to restrict approvals to only group members who are visible from the domain of the request.

## Before you begin

Role required: admin

## About this task

By default, Workflow Studio generates approvals for all group members who can access the parent request regardless of domain visibility. This configuration allows requests from members of a child domain to generate approvals for members of a parent domain who are not otherwise visible from lower in the domain hierarchy. You can use this procedure to restrict the generation of approvals to only those group members who are visible from the domain of the parent request. For information about domain hierarchies, see [Understanding domain separation](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US). For more information about visibility and contains domains, see [Visibility domains and contains domains](https://www.servicenow.com/docs/access?context=c_DomainVisibility&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Procedure

1.  [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

2.  For the system property name, enter `com.glide.hub.flow.approval.group_member.use_query_no_domain`.

3.  For the system property type, select **true\|false**.

4.  For the system property value, enter one of these values.

<table id="choicetable_j55_c14_t4b"><tbody><tr><td id="d46787e101">

**true**

</td><td>

Generate approvals for all members of the group who have access to the domain of the parent request. Select this option to exclude domain visibility from the approval generation query. For example, generate approvals for users who belong to domains higher in the domain hierarchy. This is the default value.

</td></tr><tr><td id="d46787e110">

**false**

</td><td>

Generate approvals only for group members who are visible from the domain of the parent request. Select this option to include domain visibility in the approval generation query. For example, do not generate approvals for users who belong to domains higher in the domain hierarchy.

</td></tr></tbody>
</table>    **Note:** Workflow Studio only generates approvals for users who can access the domain of the request.


## Result

Workflow Studio only generates approvals for group members who belong to the same domain or child domains of the parent request.

**Parent Topic:**[Domain separation and Workflow Studio](../concept/flow-designer-domain-separation.md)

