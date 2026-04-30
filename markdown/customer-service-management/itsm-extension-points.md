---
title: Extension points for CSM integration with IT Service Management
description: Use the extension points available with CSM integration with IT Service Management to extend the functionality of your application.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [CSM integration with IT Service Management overview, Integrating with IT Service Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Extension points for CSM integration with IT Service Management

Use the extension points available with CSM integration with IT Service Management to extend the functionality of your application.

Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.

## Using an extension point to map the Incident field

Customers can create the logic for mapping the **Incident** field by using the sn\_cs\_sm.CSMIncidentIntegrations extension point.

For more information about mapping fields, see the [How to map or copy field values from Case to Incident when using CSM Integration with Incident Management \[KB0817494\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0817494) article in the HI Knowledge Base.

## Using an extension point to map the Problem field

Customers can create the logic for mapping the **Problem** field by using the sn\_cs\_sm.CSMProblemIntegrations extension point.

## Using an extension point to map the Change Request field

The Customer Service with Service Management plugin \(com.sn\_cs\_sm\) adds the CSMChangeIntegrations extension point, which exposes generic APIs that are used for Case to Change integration.

**Note:** The CSMChangeIntegrations extension point is read only. To modify this extension point, contact ServiceNow Customer Support.

The Customer Service with Service Management plugin also adds an implementation of the CSMChangeIntegrations extension point. This implementation can be modified and deactivated. However, this isn’t recommended.

If it’s necessary to modify the APIs within the CSMChangeIntegrations extension point, the system administrator can:

-   Create an implementation of an extension point.
-   Make the necessary changes in the implementation.
-   Update the order of the implementation to a lower number. The system executes the implementation with the lowest order number.

**Note:** API names used in the implementation must remain the same, otherwise the extension point won’t be able to identify the implementation, causing an error.

For example, the CSMChangeIntegrations extension point includes the following copyFieldsFromCaseToChange API for creating a change from a case record.

```
copyFieldsFromCaseToChange: function(changeGr, caseGr) {
		changeGr.short_description = caseGr.short_description;
		changeGr.cmdb_ci = caseGr.cmdb_ci;
		changeGr.impact = caseGr.impact;
		changeGr.urgency = caseGr.urgency;
		changeGr.priority = caseGr.priority;
		changeGr.company = caseGr.account;
		changeGr.sys_domain = caseGr.sys_domain;
},
```

To modify this API, create an implementation of the extension point and make the desired changes without changing the API name.

```
copyFieldsFromCaseToChange: function(changeGr, caseGr) {
		changeGr.abcd = caseGr.abcd;		
},
```

## Using an extension point to map the Request field

Customers can create the logic for mapping the **Request** field by using the sn\_cs\_sm\_request.CSMRequestIntegrations extension point.

## Using an extension point to approve changes and requests from the Customer Service Portal

This feature includes an extension point that can be used to configure approval entities: **global.CSMApprovalsManagement**. Use this extension point to extend the approval functionality to any other entity, such as a problem.

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

