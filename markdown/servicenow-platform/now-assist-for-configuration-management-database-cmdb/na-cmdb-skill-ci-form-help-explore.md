---
title: View CI details on the Explore CI view
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

# View CI details on the Explore CI view

Now Assist answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace.

## Before you begin

To enable Now Assist to provide a detailed description, you must activate the External Content Connectors plugin, install the ServiceNow Product Documentation connector, and then crawl the product documentation. For configuration instructions, see [Configure the CI form contextual help skill](na-cmdb-skill-form-sense-config.md).

Role required: cmdb\_inst\_admin

## About this task

In addition to using Now Assist on the Explore CI page, Now Assist provides detailed information on any CI form while you create, view, or update a CI record, as described in [View CI attribute descriptions on CI forms](na-cmdb-skill-ci-form-help.md).

## Procedure

1.  While viewing a CI on the Explore CI view, select **Ask Now Assist for help**.

    The Now Assist panel opens. Enter a question about any field or section on the view. For more information, see Working in the Now Assist panel.

    ![Description of the CI attribute](../image/na-cmdb-ci-form-help-explore-ci-ex.png)

2.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d602168e143">

Option

</th><th align="left" id="d602168e146">

Procedure

</th></tr></thead><tbody><tr><td id="d602168e152">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up ![](../../configuration-management/image/icon-thumbs-up.png). If you think that it wasn’t helpful, select thumbs-down ![](../../configuration-management/image/icon-thumbs-down.png).This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d602168e167">

**Copy the summary**

</td><td>

Select the copy to clipboard icon ![](../../configuration-management/image/icon-clipboard.png) to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d602168e178">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon ![](../../configuration-management/image/icon-redo.png) to refresh the response information.

</td></tr></tbody>
</table>
**Related topics**  


[View CI attribute descriptions on CI forms](na-cmdb-skill-ci-form-help.md)

[Configure the CI form contextual help skill](na-cmdb-skill-form-sense-config.md)

[Manage CI details using CI Form in CMDB Workspace](../../configuration-management/concept/ci-form-cmdb-workspace.md)

