---
title: Legacy - Set default branch
description: Set a default branch when you want to use a branch other than main for new changes or for your main development repository.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Set default branch

Set a default branch when you want to use a branch other than main for new changes or for your main development repository.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin
-   [Legacy - Link an application or application-customization to source control](t_LinkAnApplicationToSourceControl.md)

## Procedure

1.  Follow the steps to [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

2.  Add the **glide.source\_control.default\_branch\_name** property, and specify the default branch name of the GIT source control repository to work from \(pull requests, code commits, etc.\).


## Result

Application developers' work is managed from and saved into the default branch if not otherwise specified. If not changed, this value defaults to sn\_instances/&lt;instance\_name&gt;.

**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

