---
title: Edit the start and completion tag names and colors
description: You may prefer to edit the names and colors of the start and complete tags for the initiate malware scan and isolate host capabilities. The start and complete tags help you quickly identify which capabilities are invoked from ServiceNow AI Platform Security Incident Response \(SIR\) security incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/mcafee-epo-edit-security-tag.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Edit the start and completion tag names and colors

You may prefer to edit the names and colors of the start and complete tags for the initiate malware scan and isolate host capabilities. The start and complete tags help you quickly identify which capabilities are invoked from ServiceNow AI Platform Security Incident Response \(SIR\) security incidents.

## Before you begin

Role required: sn\_si.admin

## About this task

As a user with the sn\_si.admin role, you may prefer to edit the colors and names of the security tags that are displayed on SIR security incidents. You may also assign tags to security tag groups to help you organize them in your ServiceNow AI Platform® instance. For example, you can change the colors of tags so the start tag of a capability is one color, and the completion tag is another color. These different colors can help you quickly identify when scans start and are successfully completed. For more information on how to set up security tag groups and tags, see [Set up security tag groups and tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/create-class-group-and-tags.md).

## Procedure

1.  To edit the names and colors of the security tags, navigate to **McAfee EPO Capabilities**, and, in the Name column, select an item in the list.

    The record for the capability is displayed.

2.  To edit a tag, to the right of a tag name, select the information icon, and open the tag record.

    \[Omitted image "mcafee-edit-tag-im-5.png"\] Alt text: Information icon highlighted.

    In the record that is displayed, edit the fields.

<table id="choicetable_ohy_xpv_bgb"><thead><tr><th align="left" id="d89132e119">

Field

</th><th align="left" id="d89132e122">

Description

</th></tr></thead><tbody><tr><td id="d89132e128">

**Name**

</td><td>

Enter a name for the security tag.

</td></tr><tr><td id="d89132e137">

**Color**

</td><td>

Security tag color. Select a color from the choice list.

</td></tr><tr><td id="d89132e146">

**Security Tag Group**

</td><td>

Enter a name of the security tag group. Click the information icon to view the available groups. Default is Metatag group.

</td></tr><tr><td id="d89132e155">

**Enforce restricted access**

</td><td>

Select this check box to assign read and write roles needed by users to read or write to records that have this security tag. Default is cleared.

</td></tr><tr><td id="d89132e165">

**Order**

</td><td>

Specify the order the tag appears on forms or within a list. Default is 100.To set the order on the list, enter a value. For example, 100, 200, 300, 400. The tag with the lowest the number is displayed first on the list. The profile with the highest number is displayed last.

</td></tr><tr><td id="d89132e177">

**Active**

</td><td>

Turn the tag on or off.

</td></tr><tr><td id="d89132e186">

**Description**

</td><td>

A description for the tag.

</td></tr></tbody>
</table>3.  Choose one to continue.

    |Option|Description|
    |------|-----------|
    |**Update**|Update the page with new changes.|
    |**Delete**|Delete this tag record from the McAfee ePO capability.|


**Parent Topic:**[McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcaffee-epo-overview-arch.md)

**Previous topic:**[Test security incidents and approve requests for the isolate host](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcafee-epo-test-incident-ih.md)

**Next topic:**[McAfee ESM - Email Parser integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcafee-esm-emailparser-integration.md)

