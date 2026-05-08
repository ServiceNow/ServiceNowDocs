---
title: View CI attribute descriptions on CI forms
description: Now Assist answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CI attribute descriptions on CI forms

Now Assist answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace.

## Before you begin

To enable Now Assist to provide a detailed description, you must activate the External Content Connectors plugin, install the ServiceNow Product Documentation connector, and then crawl the product documentation. For configuration instructions, see [Configure the CI form contextual help skill](na-cmdb-skill-form-sense-config.md).

Role required: cmdb\_inst\_admin

## About this task

This procedure describes how to dig deeply into the details of CI information on any form while creating, viewing, or updating a CI record. In addition, you can view the information while working in the Explore CI view, as described in [View CI details on the Explore CI view](na-cmdb-skill-ci-form-help-explore.md).

## Procedure

1.  On any CI form \(while creating, viewing, or updating a CI record\) select the Now Assist icon ![](../image/icon-na-cmdb-ci-form.png) for a field.

    Now Assist displays the description of the attribute. In this example, while creating a CI record, the user views the description of the **MAC Address** attribute.

    ![Description of the CI attribute](../image/na-cmdb-ci-form-context-ex.png)

2.  Select **Ask a follow-up** to learn more about the attribute.

    The Now Assist panel opens. Select one of the suggested questions or enter a different question about any field or section of the form. Now Assist responds to your follow-up question. For more information, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

3.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d313189e163">

Option

</th><th align="left" id="d313189e166">

Procedure

</th></tr></thead><tbody><tr><td id="d313189e172">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up ![](../../configuration-management/image/icon-thumbs-up.png). If you think that it wasn’t helpful, select thumbs-down ![](../../configuration-management/image/icon-thumbs-down.png).This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d313189e187">

**Copy the summary**

</td><td>

Select the copy to clipboard icon ![](../../configuration-management/image/icon-clipboard.png) to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d313189e198">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon ![](../../configuration-management/image/icon-redo.png) to refresh the response information.

</td></tr></tbody>
</table>
**Related topics**  


[View CI details on the Explore CI view](na-cmdb-skill-ci-form-help-explore.md)

[Configure the CI form contextual help skill](na-cmdb-skill-form-sense-config.md)

