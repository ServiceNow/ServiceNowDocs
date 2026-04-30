---
title: Troubleshooting issues of Jira integration with Agile Development 2.0
description: Resolve common issues that you might face while working with the integration of Jira and Agile Development 2.0.
locale: en-US
release: xanadu
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: reference
last_updated: "2024-09-06"
reading_time_minutes: 4
breadcrumb: [Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Troubleshooting issues of Jira integration with Agile Development 2.0

Resolve common issues that you might face while working with the integration of Jira and Agile Development 2.0.

<table id="table_gsp_wdx_hkb"><thead><tr><th>

Issue

</th><th>

Action

</th></tr></thead><tbody><tr><td>

The export action is not working.

</td><td>

-   Review your custom map configuration.

If your custom map configuration is invalid or if the custom field configured is not added to the default screen scheme of the issue, export does not work.

-   Ensure that the **Enable Export** check box is selected in the project integration settings for this Jira project or board.
-   Check if your Jira password has expired.

</td></tr><tr><td>

The sprint is not associated to the imported stories.

</td><td>

Verify if the sprint is started in Jira. If the sprint that is associated with the stories is a future sprint, then it is not associated to the stories in Agile Development.

 Sprint data from Jira is updated in Agile Development only if the sprint is active in Jira.

</td></tr><tr><td>

The sprint is not imported into Agile Development 2.0.

</td><td>

-   Ensure that your sprint in Jira has dates.
-   Ensure that the dates of a sprint in Jira does not overlap with another sprint in the same assignment group in Agile Development 2.0.

</td></tr><tr><td>

A value from a field in Jira is not populated in Agile Development 2.0.

</td><td>

Verify if the custom field map is configured.

</td></tr><tr><td>

The value of **Priority** or **State** fields from Jira is not populated in Agile Development 2.0.

</td><td>

Verify if the custom workflow state map is configured.

</td></tr><tr><td>

An update by a user in Jira is not updated in Agile Development 2.0.

</td><td>

Ensure that the user credentials that are used to set up the integration of Jira with Agile Development are not used to perform record updates.

</td></tr><tr><td>

The issue is deleted in Jira and not deleted in Agile Development 2.0.

</td><td>

Ensure that the **Can Delete** field in the Application access of the respective tables is set to true.

</td></tr><tr><td>

For Jira cloud users, when you import, you see duplicate comments.

</td><td>

Verify the cyclic payload. Ensure that the privacy settings should be enabled for the connection user \(used in http connection in Agile Development 2.0\) to make the Email address visible in webhook events.

</td></tr><tr><td>

Deleting a project or board in Jira does not result in any action in Agile Development 2.0.

</td><td>

After deleting the project or board in Jira, the Jira administrator must manually delete the associated stories in the Agile Development 2.0.

</td></tr><tr><td>

Using rich text in Jira results in garbled text in Agile Development 2.0.

</td><td>

The wiki text format that is used in Jira is not supported.

</td></tr><tr><td>

For a Next-gen Jira project, when a story is created for an epic in Jira, the relation between story and epic is not imported to Agile Development 2.0.

</td><td>

In Jira, make a nominal update to the story which would send the epic relation along with this update to the Agile Development 2.0.

</td></tr><tr><td>

Sub tasks information is neither imported nor exported between Jira and Agile Development 2.0.

</td><td>

To enable import of sub tasks from Jira to Agile Development 2.0, you must manually configure custom mapping for this task type. For more information, see [Customize your table map configuration](../task/custom-table-map-configuration.md).

</td></tr><tr><td>

For a Next-gen Jira project, scrum tasks are not exported from Agile Development 2.0 to Jira.

</td><td>

The application supports only the import of sub tasks from Jira to the Agile Development 2.0 but not the export of these tasks to Jira.

</td></tr><tr><td>

After discovering and importing projects, map configuration is not generated for a project.

</td><td>

Ensure that the user for whom the connection alias is created has access to all Jira projects.

</td></tr><tr><td>

The UI actions for Connect, Disconnect, and Validate and Fix result in an error when using for the first time.

</td><td>

This is a known issue. Retry the UI action.

</td></tr><tr><td>

While fetching Jira project metadata, the API call fails in the Flow designer, with a **API response size exceeded** error.

</td><td>

Reduce the value of the batch size property by setting it to any value between 1 and 50. For more information, see [Define batch size for Jira project metadata](../task/define-batch-size.md).

</td></tr><tr><td>

Import Issues are staying in 'Processing' state forever.

</td><td>

Import requests are stuck because Reset mapping in't working as server type, as it was incorrectly set as 'cloud' instead of 'server'. Few customers will not setup connection attributes, and therefore 'server type' and 'server verions' are defaulted to 'cloud' and '8' respectively. Set guidelines for Jira on-prem customers to use proper connection attributes.

</td></tr><tr><td>

Bulk importing of work items data fails with a **API response size exceeded** error.

</td><td>

Reduce the value of **MAX\_LIMIT** in the JiraConstants Script Include and then try to bulk import the work items data again.

</td></tr></tbody>
</table>## Enabling detailed project logs

To view all the details on project logging, enable the integration project logging property. For more information, see [Enable detailed project logging in Jira Integration with Agile Development](../task/enable-integration-logs-jira.md).

