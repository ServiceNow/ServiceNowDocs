---
title: Additional information for onboarding DevOps tools and apps using the Service catalog
description: Use the onboarding catalog items as a self-service approach to onboard your DevOps tools and apps.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Additional information for onboarding DevOps tools and apps using the Service catalog

Use the onboarding catalog items as a self-service approach to onboard your DevOps tools and apps.

## Onboarding tools and apps

**Note:** This content pertains to the Classic Environment, which refers to working in lists of records and on record forms directly, not in the [Configurable Workspace interface](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US). You can work in the Classic Environment with Next Experience active, or with it inactive, which is referred to as Core UI, \(formerly known as UI16\).

Use the ServiceNow Service Catalog to request the onboarding of tools and apps. Fill out the onboarding form details for a tool or an app and submit the request. You can also import the DevOps data for the app that you are creating for swifter and easier onboarding.

Prior to the request creation, an automated workflow approves or rejects the request.

-   When the workflow is approved, a success message displays.
-   When rejected, an inbound event is created capturing error logs. By ensuring the log is error free, you can create a request again.

You can onboard DevOps tools and apps using self-service catalog items.

-   Navigate to **All &gt; Service Catalog &gt; Catalog Definitions &gt; Maintain Items &gt; DevOps App Onboarding**, and set the **Active** state to **True** to activate the **DevOps App Onboarding** maintain item. By default the catalog items \(App Onboarding\) is turned off.
-   Navigate to **All &gt; Service Catalog &gt; Catalog Definitions &gt; Maintain Items &gt; DevOps Tool Onboarding**, and set the **Active** state to **True** to activate the **DevOps Tool Onboarding** maintain item. By default the catalog items \(Tool Onboarding\) is turned off.
-   To add the DevOps catalog items in the Service Catalog categories in Service Portal, set the category of these items to **DevOps** and add the **Service Catalog** catalog. If the **DevOps** category is not available, you must create a new category called **DevOps** from the catalog item record itself and assign the **DevOps Onboarding** catalog to it.
-   To add the DevOps catalog items in Employee Service Center, add a new topic in the **Assigned Topics** related list with taxonomy as **Employee** in the **IT &gt; IT for IT** section. The Assigned Topics related list is not available in the Default view of the Catalog Item form. To add it, select **Additional icons &gt; Configure &gt; Related Lists** and move the **Connected Content → Catalog item** field to the selected section.
-   Navigate to **All &gt; Flow Designer &gt; Flows**, and activate the **Request for onboarding approval** flow, so that the tool or app onboarding requests are approved by default. If you want to request manual approval for onboarding catalog items \(i.e. from a user other than the DevOps system user\), you can update the rule set in the **Ask For Approval** action of the flow. You can configure manual request approval for such items by configuring the fulfillment process for the catalog item. For more information, see [Service Catalog request fulfillment](https://www.servicenow.com/docs/access?context=request-fulfillment&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
-   Customize roles for approvals of the request for onboarding approval flow from Flow Designer.

## Onboarding at scale

You can also use the onboarding APIs to onboard DevOps tools &amp; apps in bulk instead of onboarding one tool or app per request. In the request parameters for tools or apps, you can specify multiple values to onboard them in one go. For example:

```
{
    "tools":[
    {
        "name": "jira_revamp",
        "type": "Jira",
        "url": "http://jira1.sndevops.xyz",
        "username": "admin",
        "password": "DevOps1!",
        "useMidServer": false
    },
    {
        "name" : "azure_revamp",
        "type" : "Azure DevOps",
        "url"  : "https://dev.azure.com/ADOLightweight/Testing%20ADO%20On%20empmolugu",
        "username" : "devops.integration.user",
        "password" : "a5xvoea2osy3ld43p2biojcu6eog5y5q3xicqbbgxwuphjbbcu6a",
        "useMidServer" : false
    },
    {
        "name" : "jenkins_revamp",
        "type" : "Jenkins",
        "url"  : "http://jenkins5.sndevops.xyz/",
        "username" : "admin",
        "password" : "DevOps1!",
        "useMidServer" : false
    },
    {
        "name" : "github_revamp",
        "type" : "GitHub",
        "url"  : "https://api.github.com",
        "username": "admin",
        "password": "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",
        "useMidServer" : false
    },
    {
        "name" : "bitbucket_revamp",
        "type" : "Bitbucket",
        "url"  : "",
        "username" : "admin",
        "password" : "DevOps1!",
        "useMidServer" : false
    },
    {
        "name": "gitlab_revamp",
        "type": "GitLab",
        "url": "http://gitlab2.sndevops.xyz",
        "username": "admin",
        "password": "mYdAJQCLi6Qft4Nk3XvS",
        "useMidServer": false
    }],
    "credentials" : {
        "name" : "devops.integration.user",
        "password" : "devops"
    }
}
```

-   Onboard DevOps apps at scale by using the DevOps app onboarding API. The POST/devops/onboarding/app request creates an onboarding app event that is asynchronously processed by the DevOps service. For more information, see [POST/devops/onboarding/app](https://www.servicenow.com/docs/access?context=devops-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).
-   Onboard DevOps tools at scale by using the DevOps tool onboarding API. The POST/devops/onboarding/tool request creates an onboarding tool event that is asynchronously processed by the DevOps service. For more information, see [POST/devops/onboarding/tool](https://www.servicenow.com/docs/access?context=devops-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

-   **[Importing historical data for DevOps tools](import-historical-data-devops-catalog.md#)**  
Use the service catalog to onboard a new app and import historical DevOps data for that app. Enable polling to import data that is mapped to associated plans, repositories and pipelines on a scheduled frequency.

**Parent Topic:**[Managing DevOps Change Velocity](using-devops-change-velocity.md)

