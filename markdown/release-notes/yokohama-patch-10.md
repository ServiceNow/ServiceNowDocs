---
title: Yokohama Patch 10
description: The Yokohama Patch 10 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 52
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 10

The Yokohama Patch 10 release contains important problem fixes.

-   **Yokohama Patch 10 was released on December 09, 2025.**
    -   Build date: 12-04-2025\_1911
    -   Build tag: glide-yokohama-12-18-2024\_\_patch10-11-20-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y010.00.xlsx).

## Overview

Yokohama Patch 10 includes 174 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp10.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 10 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 10, refer to [KB2631466](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2631466).

## Changes in Yokohama Patch 10

-   **[Sensitive data filters](https://www.servicenow.com/docs/access?context=sensitive-data-filters&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The Discovery Sensitive Data Filters \[discovery\_sensitive\_data\_filter\] table provides a way to help prevent sensitive information from being exposed in the Configuration Management Database \(CMDB\) by applying redaction rules during data collection.

-   **[Exploring Federated ID](https://www.servicenow.com/docs/access?context=federated-id&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    By using the `roles` of the user across the instances, the Federated ID is created and displayed in the **sys\_user\_role** table.

    **Note:**

    -   Role is required for generating Federated IDs in the **sys\_user\_role** table.
    -   The Federated IDs in the **sys\_user\_role** table can be used to the over usages of the roles.
    -   Updating ID fields and Regenerate Federated IDs options are not available for Role type. There's a scheduled job that runs periodically to generate ID for roles in case its empty.
-   **[TRM Category form](https://www.servicenow.com/docs/access?context=trm-category-form&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Data certification in the Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-explore-data-cert&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Data certification is a governance process that ensures the accuracy, completeness, and reliability of critical data within an organization. It is essential for data integrity, compliance, decision-making, and risk reduction. Ensures accurate data for application portfolio decisions. Certified data strengthens enterprise modeling and visualization.

-   **[Working with data certification](https://www.servicenow.com/docs/access?context=eaw-work-with-data-cert&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Create a certification policy](https://www.servicenow.com/docs/access?context=eaw-create-policy&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Edit a certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-edit-policy&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[View certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-view-policy&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Publish a certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-publish-policy&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Run certification for a policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-run-certification&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Track progress of a certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-track-progress&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Activate a certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-activate&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Deactivate a certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-deactivate&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Delete a certification policy](https://www.servicenow.com/docs/access?context=eaw-delete-data-cert&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Export business portfolio data to Excel or CSV](https://www.servicenow.com/docs/access?context=eaw-export-business-portfolio-data&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Rationalization of business applications](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    \[Target &lt;fig&gt; was unhandled by content reference generator.\]

    \[Target &lt;fig&gt; was unhandled by content reference generator.\]

-   **[Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Analyze applications using the bubble chart](https://www.servicenow.com/docs/access?context=eaw-analyze-applications-by-capability&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    ![image.bubble-chart-group]

-   **[Create a demand using the bubble chart](https://www.servicenow.com/docs/access?context=eaw-create-a-demand-using-the-bubble-chart&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Select **Bubble chart**.

    Select the bubble for the relevant application that you want to create a demand for perform the following.

-   **[Set the planned disposition of a business application](https://www.servicenow.com/docs/access?context=eaw-set-planned-disposition-of-a-business-application&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Add business application lifecycle data using the bubble chart](https://www.servicenow.com/docs/access?context=eaw-add-business-application-lifecycle-data&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Select **Bubble chart**.

    Select the bubble for the relevant application that you want to add business application life-cycle data for and perform the following.

-   **[Edit business application details in bubble chart view](https://www.servicenow.com/docs/access?context=eaw-edit-ba-details-in-bubble-chart&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    You can make updates to the business application record directly from the list, without leaving the bubble chart view.

-   **[List view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-list-view&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Create a demand using the list view](https://www.servicenow.com/docs/access?context=eaw-create-a-demand-using-the-list-view&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Add business application lifecycle data using the list view](https://www.servicenow.com/docs/access?context=eaw-add-business-application-lifecycle-data-listview&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Edit business application details in list view](https://www.servicenow.com/docs/access?context=eaw-edit-business-application-details&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Edit a demand associated with a business application](https://www.servicenow.com/docs/access?context=eaw-edit-a-demand-associated-with-a-business-application&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Edit a project associated with a business application](https://www.servicenow.com/docs/access?context=eaw-edit-a-project-associated-with-a-business-application&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Export application rationalization data to Excel or CSV](https://www.servicenow.com/docs/access?context=eaw-export-app-rat-list-data&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Export the application rationalization list view data to Microsoft Excel or CSV so that you can use the data to obtain insights, share with stakeholders, and prepare for analysis.

-   **[Apply filters on the Application Rationalization page](https://www.servicenow.com/docs/access?context=eaw-apply-filters-app-rat&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    You can apply filters on the Application Rationalization page in the Enterprise Architecture Workspace. Based on the applied filters, the bubble chart and list view are updated so that you can view data for a specific business application. Your filter preferences are saved and applied the next time you visit the page.

-   **[Managing the Technology Reference Model in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-managing-the-technology-portfolio&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Export Technology Reference Model product category data to Excel or CSV](https://www.servicenow.com/docs/access?context=eaw-export-trm-prod-cat-data&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-tpm&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Update TPM data for a business application or application service](https://www.servicenow.com/docs/access?context=update-tpm-data&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Run a scheduled job to populate Technology Portfolio Management lifecycle record identifier](https://www.servicenow.com/docs/access?context=eaw-run-job-to-populate-tpm-lifecycle-identifier&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Add AI systems to business applications](https://www.servicenow.com/docs/access?context=eaw-add-ai-systems&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Remove AI systems associated with business applications](https://www.servicenow.com/docs/access?context=eaw-remove-ai-systems-assoc-ba&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Exploring the AI Portfolio](https://www.servicenow.com/docs/access?context=eaw-exploring-the-ai-portfolio&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   **AI System Digital Asset**: AI system digital asset represents a software artifact that integrates one or more AI models and datasets. It answers the question, 'Where is the AI system running and how is it configured?'.
    -   **AI Model Digital Asset**: AI model digital asset represents the metadata and configurations of an AI model used by an AI system to generate its output. It answers the question, 'Where is this model running and how is it configured?'.
    -   **AI Dataset Digital Asset**: AI dataset digital asset represents the actual collection of data that is used to train and validate particular AI models. It answers the question, 'Where is this dataset running and how is it configured?'.
    -   **AI Prompt Digital Asset**: AI prompt digital asset represents the structured input instruction provided to an AI model to elicit a specific response or behavior. It answers the question, 'Where is this prompt running and how is it configured?'.
    -   **AI System Product Models**: AI system product model represents the system that delivers the AI outcomes. It orchestrates models, data, runtime service, and interfaces to deliver AI functionality. It answers the question, 'Which AI system do you use and why?'.
    -   **AI Model Product Models**: AI model product model represents a structured record that catalogs an AI model's specifications and lifecycle details. It enables traceability between the AI model and the AI system that consumes it, as well as associated datasets and prompts. It answers the question, 'Which model do you use and why?'.
    -   **AI Dataset Product Models**: AI dataset product model represents the overall datasets that are available to train and evaluate AI models and systems. It answers the question, 'Which dataset do you use and why?'.
    -   **AI Prompt Product Models**: AI prompt product model represents the structured record that catalogs governed prompt templates used by AI models and systems and its intended use and conformance state. It answers the question, 'What prompts do you use and why?'.
-   **[View all AI System Product Models](https://www.servicenow.com/docs/access?context=eaw-view-all-ai-system-product-models&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[View all AI Model Product Models](https://www.servicenow.com/docs/access?context=eaw-view-all-ai-model-product-models&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[View all AI Dataset Product Models](https://www.servicenow.com/docs/access?context=eaw-view-all-ai-dataset-product-models&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[View all AI Prompt Product Models](https://www.servicenow.com/docs/access?context=eaw-view-all-ai-prompt-product-models&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
-   **[Add or edit a TRM category](https://www.servicenow.com/docs/access?context=eaw-create-new-trm-category&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    \[Target &lt;context&gt; was unhandled by content reference generator.\]

-   **[General information form](https://www.servicenow.com/docs/access?context=eaw-data-cert-gen-info-form&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Learn about the fields of the General information form. Use this form to provide details for the new policy.

-   **[Options form](https://www.servicenow.com/docs/access?context=eaw-data-cert-options-form&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    The options that appear depends on whether they are relevant to the selected policy type. Therefore, some of the following options don't appear on your form.

-   **[Schedule form](https://www.servicenow.com/docs/access?context=eaw-data-cert-schedule-form&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Learn about the fields of the Schedule form. Use this form to define the timing and frequency for executing the certification task.

-   **[Data filter form](https://www.servicenow.com/docs/access?context=eaw-data-filter-form&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Learn about the fields of the Data filter form. Use this form to define which records need certification.

-   **[Sensitive data filters](https://www.servicenow.com/docs/access?context=sensitive-data-filters&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The Discovery Sensitive Data Filters \[discovery\_sensitive\_data\_filter\] table provides a way to help prevent sensitive information from being exposed in the Configuration Management Database \(CMDB\) by applying redaction rules during data collection.

-   **[Exploring Federated ID](https://www.servicenow.com/docs/access?context=federated-id&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    \[/ul/li/p/ph/title \{"- topic/title "\}\)Federated ID for Roles\(title\]    By using the `roles` of the user across the instances, the Federated ID is created and displayed in the **sys\_user\_role** table.
    
        **Note:**
    
        -   Role is required for generating Federated IDs in the **sys\_user\_role** table.
        -   The Federated IDs in the **sys\_user\_role** table can be used to the over usages of the roles.
        -   Updating ID fields and Regenerate Federated IDs options are not available for Role type. There's a scheduled job that runs periodically to generate ID for roles in case its empty.
    


## Notable fixes

The following problems and their fixes are ordered by potential impact to customers, starting with the most significant fixes.

<table id="notable-fixes" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Audit History

 PRB1938364

 [KB2531096](https://hi.service-now.com/kb_view.do?sysparm_article=KB2531096)

</td><td>

Large amount of history \(audit\) data can lead to node memory contention on node when loading form

</td><td>

When loading a form for the first time, the node may run out of memory and crash. This happens if the history set has to be built to load the activity stream and if there's a lot of data to be loaded.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1947882

</td><td>

After upgrading within Yokohama, the email MFA option is missing and only TOTP is shown

</td><td>

After upgrading, users are no longer able to see the email multi-factor authentication option during login. Only the Authenticator App \(TOTP\) is displayed, even after selecting 'Try another way to verify.'

</td><td>

1.  Make sure both email and the Authenticator App \(TOTP\) are configured.
2.  Log in.
3.  Observe that only the TOTP appears as a multi-factor authentication option.
4.  Select **Try another way to verify**.

 Observe that only TOTP appears. The email option is still missing.

</td></tr><tr><td>

Encryption

 PRB1931988

 [KB2481838](https://hi.service-now.com/kb_view.do?sysparm_article=KB2481838)

</td><td>

A data migration job fails when there are no context keys and EFC's in the migration\_pending state

</td><td>

The job state changes to 'Error', with the following summary: 'Error creating job handler for type all\_data\_to\_kmf: \[The KMF cryptographic module to encryption context relationship table is empty. The 'Migrate Key Context to Module' job might not have been run or has failed.\].'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1941990

</td><td>

Trigger inputs aren't accessible after a do-until loop execution

</td><td>

This issue is caused by the changes to GlideFlowStages Updater.java \(older name GlideStage UpdateListener.java\). It's observed that, in this specific flow structure, the 'in.request\_item' flow input isn't passed to the 'Create Catalog Task' action. Querying the sys\_flow\_value table, there are 2 entries for 'in.request\_item' one for the flow input and another with the parent loop associated. As the same key 'in.request\_item' is now associated with parent loops, it can only be accessed in the loop body \(and for the specific iteration\). All other references to it out side the loop aren't available.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1938123

</td><td>

Flows using base instance actions related to the plugin 'Customer Service Spoke' fail after upgrading to Yokohama

</td><td>

The flows in question are base instance actions related to 'Customer Service Spoke': Add Work Note to Task and Add Comment To Task.

</td><td>

 

</td></tr><tr><td>

List Editor

 PRB1842085

 [KB1803766](https://hi.service-now.com/kb_view.do?sysparm_article=KB1803766)

</td><td>

A 'Discard your changes?' modal displays when quick editing and the record was already saved

</td><td>

This issue isn't reproducible in Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## All other fixes

<table id="AllOtherFixes" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Activity Stream

 PRB1902133

</td><td>

Draft text is lost after switching tabs in the Service Operations Workspace

</td><td>

The draft text entered in the activity stream in an Overview tab is lost after switching tabs in the Service Operations Workspace.

</td><td>

1.  Navigate to the Service Operations Workspace.
2.  Open any incident record from the Incident List.
3.  Enter text in a field, such as Work Notes or Additional Comments.
4.  Use the global search to look up a keyword like 'server' or 'Linux'.
5.  Open any record from the search results.
6.  Observe that it opens in a new SOW tab.
7.  Return to the original incident record tab.

 Expected behavior: Text is retained after switching tabs in SOW.

 Actual behavior: The previously entered draft text is no longer present. Text disappears after switching tabs in SOW.

</td></tr><tr><td>

Activity Stream

 PRB1928872

</td><td>

The CanReadRepo class encounters a ConcurrentModification Exception

</td><td>

This concurrency issue arises because the class uses a HashMap, which is not thread-safe. The HashMap should be replaced with a ConcurrentHashMap to help ensure thread-safe operations and prevent the exception.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1938976

</td><td>

ACLs prevent system administrators from running GlideActivity scriptable methods

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1947683

 [KB2631388](https://hi.service-now.com/kb_view.do?sysparm_article=KB2631388)

</td><td>

Activity stream caches excessive records, causing sys\_activity table growth and performance degradation

</td><td>

Instead of caching only viewed entries, the platform may proactively cache all work notes and events generated on monitored tables, including those that are never accessed through the UI. This behavior results in rapid growth of the sys\_activity table, sometimes reaching tens or hundreds of millions of records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1955936

</td><td>

The user is unable to route chats landing on external queues if agents are available on a different domain

</td><td>

The requester gets a 'No agents available' message even though there's an agent available.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1959396

</td><td>

AWA workitemResponder onChange published message causes a work item card to disappear in the workspace

</td><td>

Work items disappear from the inbox even though they're still pending for acceptance.

</td><td>

1.  Log in to one browser as an agent.
2.  Have multiple sessions as the requester.
3.  Start chatting with the agent.
4.  In the agent browser, observe the multiple work items pending for accept in the inbox.
5.  Navigate to the awa\_work\_item table.
6.  Update one of the pending accept work items.

 Expect behavior: The agent receives an AMB message about the updated work item, but all the pending accept work items remain the same.

 Actual behavior: All the other work items disappear from the inbox even though they're still pending for acceptance. Only the one that was just updated remains in the inbox.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1913578

</td><td>

Search sources are inadvertently deleted when the indexed source is missing

</td><td>

The search source entry should remain in place. Any search profile using the search source should continue to function without throwing any error that stops the search. However, the search source entry is automatically deleted when the cleanup job runs if the underlying source is no longer accessible.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1944944

</td><td>

RAG corrupted AIS results send back the wrong sys\_id and text in results

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1953003

</td><td>

The **Enable hybrid search** field is editable on list view, but it should be read-only

</td><td>

 

</td><td>

1.  Open a Yokohama or Zurich instance.
2.  Open SAC in list view.
3.  Add the **Enable hybrid search** field to list view.

 Observe that the field is editable.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1953364

</td><td>

Users without permissions find truncated/dropped results and the ext\_content\_none\_access field is set to 'true'

</td><td>

This issue was found with AI Search version 104.0.0.9.

</td><td>

1.  Add two users to the Glide instance.
2.  Use External Content Connector for SharePoint Online.
3.  Restrict crawling to a Sharepoint URL.
4.  Start a Full document crawl.
5.  Start a User-mapping crawl.
6.  Wait for the completion of both crawls.

 Expected behavior: The active user can find all documents from the site, but the deactivated user can find no documents from the site and hasn't been mapped.

 Actual behavior: The deactivated user isn't mapped, but searching as that user returns documents that shouldn't be returned.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1954113

</td><td>

In RegressionSolutionStore, add support for enabling/disabling deprecation and setting minimum records required

</td><td>

RegressionSolutionStore currently uses a sys property to manage deprecation and minimum records required for training. Support should be added for enabling or disabling deprecation, as well as setting minimum records required for training without relying on a sys property.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1954989

</td><td>

activateDatasource\(\) fails to create entries into the sys\_update\_xml table

</td><td>

 

</td><td>

1.  In any store app, create index source configuration and semantic index configuration in inactive state.
2.  Write a fix script to activate the index source using sn\_ais.AisUtil. activateDatasource\(\).
3.  Make sure the post-install index source is active and there's no entry in sys\_update\_xml for the updates done via API.
4.  Reinstall the store app.

 Observe that the indexed sources are marked as inactive.

</td></tr><tr><td>

AI Search

 PRB1949749

</td><td>

AI search doesn't return results on latest znowassist instances

</td><td>

AI search doesn't return any results because the following properties aren't set to true: gs.setProperty \('sn\_ais\_assist. dpr\_ingestion\_completed', 'true'\); and gs.setProperty \('sn\_ais\_assist. passage\_format \_ingestion\_completed', 'true'\);.

</td><td>

1.  Enable AI search on a recent Zurich instance.
2.  Try to fetch any results.

 Expected behavior: AI search returns results properly.

 Actual behavior: AI search doesn't return any results because the following properties aren't set to true: gs.setProperty \('sn\_ais\_assist. dpr\_ingestion\_completed', 'true'\); and gs.setProperty \('sn\_ais\_assist. passage\_format \_ingestion\_completed', 'true'\);.

</td></tr><tr><td>

AI Search UX

 PRB1952630

</td><td>

Malformed URLs in the streaming chunks for a synthesized response cause the UI to hang

</td><td>

The URL renders standalone and sometimes isn't clickable.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1963505

</td><td>

URLs towards the end of the streaming are rendered as plain text

</td><td>

 

</td><td>

1.  Open an instance where synthesized answers are working.
2.  Search a query that would have a URL towards the end of the answer.

 Observe that the URL is rendered as plain text.

</td></tr><tr><td>

AI Search UX

 PRB1963984

</td><td>

Streaming fails when there's a response with numerous citations

</td><td>

When the user searches for a term with 10 or more citations, streaming sometimes gets stuck. It indirectly pushes component into halt and doesn't show feedback options.

</td><td>

1.  Provision an instance with Synth GR.
2.  Search for a term that would result in 10 or more citations.

 Observe that the streaming is intermittently stuck, indirectly pushing component into halt and not showing feedback options.

</td></tr><tr><td>

Analytics Data API

 PRB1920837

</td><td>

Platform Analytics dashboard displays 'No data available' when 'Enable Data Cache' is enabled for Indicator Scorecard visualizations

</td><td>

After an upgrade, dashboards widgets of type 'Indicator Scorecard' aren't loading as expected. The error message says 'No Data Available. No content available for the selected criteria'. This issue occurs for both new visualizations and saved visualizations.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1956759

</td><td>

An app manager install pop-up should display instructions to sign new company-level terms and conditions in Store

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Rationalization

 PRB1898811

</td><td>

Remove functionality doesn't work for architectural artifact-related lists

</td><td>

Architectural artifacts can't be removed for Digital integration, Digital interface, TRM Product, and Business Process Lists.

</td><td>

1.  Log in as an APM user.
2.  Navigate to **Enterprise Architecture Workspace** &gt; **Portfolio** &gt; **Business process/Digital integration/Digital interface/TRM Product**.
3.  Add an architectural artifact.
4.  Select and remove the artifact.

 Expected behavior: The linked artifact is removed.

 Actual behavior: The linked artifact isn't removed.

</td></tr><tr><td>

Application Rationalization

 PRB1921023

</td><td>

EA indicator framework generates the wrong score for the minimize indicator

</td><td>

When the absolute value is empty or not available, the EA indicator framework generates the wrong score for the minimize indicator.

</td><td>

1.  Navigate to a business application without any incidents.
2.  Generate the score for the incident indicator.

 Expected behavior: The expected score is 10 because there are no incidents for the business application for the given fiscal period and the incident indicator is minimize.

 Actual behavior: It generates 0.

</td></tr><tr><td>

Application Rationalization

 PRB1942817

</td><td>

Issues with Dependency View in Enterprise Architecture Workspace

</td><td>

In the Enterprise Architecture Workspace, the action **Open Dependency View** doesn't respond. No modal/tab opens, there's no redirection, and no error message is displayed. The page remains unchanged.

</td><td>

1.  Navigate to the Enterprise Architecture Workspace.
2.  In the left menu, navigate to **Portfolio** &gt; **Business Architecture** &gt; **Business Process**.
3.  Open any Business Process record.
4.  In the form, select **Open Dependency View** under the **More Actions \(⋯\)** icon.

 Observe that nothing happens. Nothing loads and there's no message.

</td></tr><tr><td>

Application Rationalization

 PRB1945947

</td><td>

Deletion of TRM product doesn't delete the associate life-cycle record

</td><td>

 

</td><td>

1.  Navigate to the life-cycle product table \(sn\_apm\_trm\_ standards\_product\).
2.  Create a record and populate the mandatory fields.
3.  Use the related list TRM Product Lifecycle \(sn\_apm\_trm\_ standards\_product\_lifecycle\).
4.  Select **New**.
5.  Populate the mandatory fields.
6.  Submit.
7.  Open the sn\_apm\_trm\_ standards\_product record that was created.
8.  Use the **Delete UI** action.
9.  Navigate to the sn\_apm\_trm\_ standards\_product\_lifecycle table.
10. Search for the record that was originally associated with the sn\_apm\_trm\_ standards\_product that you deleted.

 Observe that the record is there, but its **TRM Product** field \(mandatory\) is empty.

</td></tr><tr><td>

Application Rationalization

 PRB1961778

</td><td>

The **info** icon doesn't work properly with filters

</td><td>

The overall score for a business application is missing in the Application Rationalization grid and in the size drop-down list in bubble settings.

</td><td>

1.  Apply a filter \(BC - Leaf node is false\).
2.  Select the **Info** icon.
3.  Observe that attendance management BA is shown on the side panel, which is expected.
4.  Apply an indicator score filter \(overscore is empty\).
5.  Select the **Info** icon.
6.  Observe that attendance management BA is still shown on side panel, and the first record in the grid isn't expected.
7.  Select a BA bubble in the Bubbles page.
8.  Open the side panel.
9.  Navigate to the List page.
10. Return to the Bubbles page.
11. Observe that the side panel BA information disappears from the Bubbles page.
12. Scroll inside the Info panel.
13. Select another BA.

 Observe that the Info panel opens at the previously scrolled position instead of resetting to the top.

</td></tr><tr><td>

Asset Management

 PRB1957067

</td><td>

In Yokohama, update the base instance app version for the Asset Management common app to address slowness

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1936797

</td><td>

The SMS Twilio OTP message is broken

</td><td>

It should say 'Send from your Twilio trial account - Your 6-digit verification code is XXXXXX, it expires in 5 minutes. Enter the code to complete the authentication. Thank you.' Instead, it says 'Send from your Twilio trial account- Multifactor.OTPMessage'.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1943178

</td><td>

OAuth JWT Token Refresh token flow doesn't work for public client

</td><td>

OAuthTokenProcessor\#isPKCERequest should return 'true' for the JWT refresh\_token with the client ID with **public client** checked.

</td><td>

1.  Get the OAuth client.
2.  Set the public client to 'true'.
3.  Set the token format to JWT.
4.  Get the access token or refresh the token using authz PKCE.
5.  Send the refresh\_token grant request.

 Notice that it's 401, when it should be 200.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1941169

</td><td>

ATF reusable test input/output variables don't have a default form layout

</td><td>

After navigating to atf\_input\_variable \_callable.do or atf\_output\_variable \_callable.do, new form layout records are generated.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1951520

</td><td>

RCAs to support the 'HR case' table as input in NASK

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1955464

</td><td>

Sentiment analysis isn't determined for ER cases

</td><td>

 

</td><td>

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** &gt; **Employee** &gt; **HRSD**.
2.  Open the 'Sentiment Analysis for HR Case' skill and activate it.
3.  Open 'HR Agent Workspace'.
4.  Open any ER case.

 Expected behavior: Sentiment is determined.

 Actual behavior: Sentiment isn't determined.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1956191

</td><td>

RCA records for attachment summarization

</td><td>

 

</td><td>

Ship RCA records for attachment summarization after new changes.

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1955881

</td><td>

sn\_cmdb.\_\_rel\_type\_cache holds a lot of memory

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1860666

</td><td>

The **condition value** field inside the condition builder doesn't take input when the user selects **Run** without removing the focus

</td><td>

A conditional builder feature should be implemented to filter the list based on the condition formed.

</td><td>

1.  Create a TD on track/dataanalytics.
2.  Navigate to Indicators from the All menu.
3.  Observe that the indicator management page is displayed
4.  Open the condition builder from the list view \(the list is coming from a DB view - pa\_indicator\_ management\_db\_view\).
5.  Apply some condition with the 'is one of' operator.
6.  After entering text in the field, select **Run**.

 Observe that the **input** field doesn't shift focus and therefore doesn't take the input value.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1871451

</td><td>

Query business rules aren't honored in GraphQueryExecutors

</td><td>

Knowledge Graph queries don't execute query business rules associated with a table. A query through Now Assist about incidents assigned to the user includes resolved incidents, whereas a query on incident assigned to the user through list view doesn't show resolved incidents.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1922171

</td><td>

CONTAINS query interferes with with the RLQUERY in hybrid table

</td><td>

 

</td><td>

1.  Provision a RaptorDB instance with the following plugins installed with demo data:
    -   Human Resources Scoped App: Core Human
    -   Resources Scoped App: Lifecycle Events
2.  Log in as an admin user.
3.  Navigate to HR Case Management &gt; All HR Cases &gt; All. Open a record.
4.  Select Add Task in Related Links.
5.  Change the state to 'Ready'.
6.  Assign to a user.
7.  Enter something in the description.
8.  Select Submit.
9.  Impersonate the assigned user.
10. Navigate to /esc?id=hrm\_todos\_page.
11. Observe the task you just created.
12. Check if the HR Task table 'sn\_hr\_core\_task' on sys\_db\_object.list has the Extension Model field value as 'Table per class'.
13. If the HR Task table is TPC, impersonate as the user again and navigate to /esc?id=hrm\_todos\_page.

 Expected Behavior: The HR Task is visible under 'My tasks'.

 Actual Behavior: The HR Task isn't visible.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1925389

</td><td>

Glide queries that use a search term query in conjunction with an order-by on a **date-time** field return a null pointer exception

</td><td>

For instances running on RaptorDB, Glide queries using search term query in conjunction with an order-by on a **date-time** field return null pointer exception for matching records that have a null order field value.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1930031

</td><td>

The user doesn't get results from a child table \(sn\_lg\_cnt\_repository\) of Parent \(ast\_contract\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1938585

</td><td>

Creating edges between two WDF tables in KG designer results in an error

</td><td>

The error reads: 'Could not find source key column field account\_id in table u\_df\_co\_licenses for edge u\_account\_id.'

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1845793

</td><td>

Queries with query rewrites and force index hints run into syntax errors

</td><td>

Post RaptorDB migration, queries with query rewrites and force index hints run into syntax errors for the production instance.

</td><td>

1.  Migrate the Xanadu instance from MariaDB to Postgres, which has active query rewrites enabled.
2.  Try to execute the SQL queries with query rewrite hints \(like force index\).

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1942175

</td><td>

Thread goes into an infinite loop on DBQueryExecutor. executeStatement for broken queries that were rewritten

</td><td>

When the broken query is executed, StackOverflowException is thrown and com.glide.db.DBQueryExecutor. executeStatement goes into an infinite loop. Instead, SQLException should be thrown.

</td><td>

1.  Create the table u\_test with u\_test\_column.
2.  Create any valid query rewrite for the 'select u\_test\_column from u\_test' query.
3.  Drop the column u\_test\_column.
4.  Execute the query 'select u\_test\_column from u\_test' via DBQuery, or use a script with GlideRecord equivalent.

 Expected behavior: SQLException is thrown and com.glide.db.DBQueryExecutor .executeStatement doesn't go into an infinite loop.

 Actual behavior: StackOverflowException is thrown and com.glide.db.DBQueryExecutor .executeStatement goes into an infinite loop.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1951095

</td><td>

Set a replica pool's in-memory heartbeat to null upon failure to get heartbeat

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1959979

</td><td>

Get connections from secondary pool doesn't retry more than once

</td><td>

Retry count is capped because failImmediate is always set to true for secondary pools. This causes some issues with read replica routing.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1785169

</td><td>

ACC-V execution for Oracle GLAS Data Collection is failing because the pattern is removing 'ct\_cpuq.sh' and 'db\_queries\_ to\_csv.sql' as part of the 'Target Cleanup' process

</td><td>

The files 'ct\_cpuq.sh' and 'db\_queries\_ to\_csv.sql' are removed as part of the 'Target Cleanup' process, while 'db\_queries\_ to\_csv\_11g.sql' is ignored. This causes the step 23 run Ora LMS script UNIX with SID to fail.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1843017

</td><td>

For patterns on agent, add all available assets that start with 'pattern-execution' to OnTheFlyCheck

</td><td>

Currently, the system looks for 3 plugins \(pattern-execution, pattern-execution-mapping, pattern-execution-content\) when sending a check to ACC. This can become a problem with increasing number of content Store apps as each Store app may want to ship their own ACC plugin with the script files. The current mechanism only supports 3.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1848353

 [KB2260579](https://hi.service-now.com/kb_view.do?sysparm_article=KB2260579)

</td><td>

If HTTP calls on a pattern fail, all subsequent steps in the pattern are executed by MID Server instead of ACC Agent

</td><td>

When executing a pattern using an agent, if there's a pattern making HTTPs calls and the calls fail, all subsequent steps in the pattern are executed by MID Server instead of ACC Agent. For the WindowsHttpCommand, if the response returned is null or an exception is thrown, the agent\_id parameter isn't inserted back.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1901498

</td><td>

The sysevent script action 'Update application CIs install\_status' is no longer firing business rules

</td><td>

When the 'Update application CIs install\_status' sysevent script action is executed, 'Delete entities for absent/retired appl' isn't fired. Marking the install status as 'Absent' on cmdb\_ci\_appl records should delete the associated software install records.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1951333

</td><td>

Hybrid use cases should be selectable in the 'Create a Document Task' flow action

</td><td>

 

</td><td>

1.  Create a use case in the 'Extract information from documents' skill.
2.  Add a target table and integration for the created task.
3.  Open the integration in flow designer.

 Observe that the created use case isn't listed in the 'Task Definition' drop-down list of the 'DocIntel - Create a Document Task' action.

</td></tr><tr><td>

Document Management

 PRB1941267

</td><td>

Unable to remove document references and users for a document from scoped apps

</td><td>

 

</td><td>

1.  Create a document and version.
2.  Link this document to a core-company record.
3.  Grant access to multiple users. \(This is an optional step.\)

 Observe that users are unable to delete the users/association from a scoped app via server scripts.

</td></tr><tr><td>

Dynamic Scheduling

 PRB1951019

</td><td>

Dynamic scheduling doesn't assign tasks to agents

</td><td>

When the user runs dynamic scheduling, one agent's workblock appears in both the sorted and response sections. If the user assigns a second task to one of the agents that overlaps with the original task's time window, the task isn't reassigned.

</td><td>

Scenario 1:

 1.  Enable the following features:
    1.  Dynamic Scheduling
    2.  Workforce Optimization \(WFO\)
    3.  Territory Management
2.  Create a task with a short time window that's eligible for assignment to two agents.
3.  Create entries in wm\_agent\_schedule \_attribute\_plan for both agents.
4.  Ensure that each agent has distinct start and end locations.
5.  Generate schedules for both agents.
6.  Make sure that each agent is able to do the following within the defined schedule window:
    1.  Travel to the task location from start location.
    2.  Complete the task.
    3.  Return to their respective end locations.
7.  Run dynamic scheduling.

 Expected behavior: The dynamic scheduling report shows sorted workblocks and a response section with workblocks for both agents.

 Actual behavior: Only one agent's workblock appears in both the sorted and response sections.

 Scenario 2:

 1.  Repeat steps 1 through 6 from Scenario 1.
2.  Assign a second task to one of the agents that overlaps with the original task's time window.
3.  Run dynamic scheduling.

 Expected behavior: The pending dispatch task is assigned to the other agent.

 Actual behavior: The task isn't reassigned.

</td></tr><tr><td>

Embedded Help

 PRB1942884

</td><td>

Unable to view the 'Help center' content for different roles when there's an uppercase character in the RoleName

</td><td>

 

</td><td>

1.  Try to create the embedded help.
2.  Add the roles, except admin, and have the role\_name have an uppercase character.
3.  Check on the page.

 Observe that the content isn't displaying in the 'Help center' panel.

</td></tr><tr><td>

Enterprise Architecture

 PRB1768310

</td><td>

Inconsistent behavior when the user tries to send assessments

</td><td>

Sometimes it sends assessments, and other times it throws the error 'Select a User Group that has users, move a few users to the selected list, and send assessments'.

</td><td>

1.  Navigate to the apm\_metric table.
2.  Select any assessment indicator.
3.  Select **Generate assessment**.
4.  Add a user.
5.  Check the preview.
6.  Select **Send assessments**.

 Observe that sometimes it sends assessments, and other times it throws the error 'Select a User Group that has users, move a few users to the selected list, and send assessments'.

</td></tr><tr><td>

Enterprise Architecture

 PRB1945436

</td><td>

When creating a business application, the model\_id is set to 'Unknown'

</td><td>

The business rule 'Populate Application Model' is skipped.

</td><td>

Create a business application \(cmdb\_ci\_business\_app\).

 Observe that the model\_id is set to 'Unknown'.

</td></tr><tr><td>

Event Management

 PRB1927888

</td><td>

Make date selection more flexible to improve PRC data selection performance

</td><td>

The CR selection should support the actual start date in addition to the change time. Use a single joined query with a filter instead of two separate queries.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1939558

</td><td>

Get-related CIs should support parameters for limits and have consistent and meaningful logs for effective troubleshooting

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1939564

</td><td>

If there's a change request on the same CI as in the alert, the reason for the PRC should always be 'Change on CI'

</td><td>

Even if the change request is on the same CI as in the alert, the reason for the PRC is 'Change on application service'. Instead, the reason for the PRC should be 'Change on CI'.

</td><td>

1.  Add application service \(S1\).
2.  Add a change request \(CR\).
3.  Make S1 a configuration item of the CR.
4.  Add S1 as an impacted service of the CR.
5.  Send an alert to S1.

</td></tr><tr><td>

Event Management

 PRB1941171

</td><td>

Slow query in Event Management - Process Events

</td><td>

At the time observed of the slow query, the runtime was 27 ms on average. A replacement query is averaging 2.3 seconds or around 85x slower.

</td><td>

 

</td></tr><tr><td>

Fenix \(Family\)

 PRB1934205

</td><td>

In the Fenix plugin, scope accessibility issue in getJobStatuses ByDeployments

</td><td>

Unlike other batch mode APIs, this one doesn't support cross-scope access. It supports invocation only from the global scope. For consistency and usability, it would be helpful if this could be made accessible from the global scope.

</td><td>

1.  Create a scope.
2.  Create a batch manifest in that scope.
3.  Execute it a few times so that there are records in the fenix\_job\_status table.
4.  Run a script to get the job\_statuses, but be sure to execute the script from the new scope.

 See that it generates the following error: 'script execution error: Script Identifier: null.null.script, Error Description: invalid return type: org.json.JSONArray, Script ES Level: 200 Evaluator.evaluateString\(\) problem: java.lang.RuntimeException: invalid return type: org.json.JSONArray: com.glide.script.fencing. ScopedFunction ObjectTypeHandler .coerceReturnValue \(ScopedFunction ObjectTypeHandler .java:338\)'.

</td></tr><tr><td>

Field Service Task Bundling

 PRB1952595

</td><td>

Scheduling subtasks takes longer than expected

</td><td>

Scheduling subtasks and updating the Scheduled Start field on subtasks takes longer than expected.

</td><td>

1.  Create a bundle a task with at least 500 subtasks.
2.  Notice that the bundle task is in a pending dispatch state.
3.  Assign the created bundle task to an agent.
4.  Notice that the bundle assignment takes a lot of time.
5.  Check the subtask schedule start date and the time that it took to update the subtask schedule start date info.

 Notice that the UI is stuck or takes a long time \(5 to 6 minutes\).

</td></tr><tr><td>

Flow Engine

 PRB1936210

</td><td>

High Priority events aren't cached to the same node due to Yield Check

</td><td>

An event isn't cached to the correct node.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1950344

</td><td>

Capability metrics are executed in a Skill Role Masking session

</td><td>

Auto evaluation breaks with the application of role masking on 'Evaluate API'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1958181

 [KB2606177](https://hi.service-now.com/kb_view.do?sysparm_article=KB2606177)

</td><td>

Flows are intermittently not triggered after upgrade in a domain separation-enabled instance

</td><td>

After upgrading a domain separated instance, some flows are no longer triggered. This is because some of the flow's records are in the domain that the flow was defined in, and other records in a different domain.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1960705

</td><td>

Create a scriptable API and global script includes for getting execution data

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Form Controller

 PRB1862546

</td><td>

Form with a single field of the type 'HTML' can't be aligned with the title because it has margin that can't be removed

</td><td>

The form component doesn't align with the stylized text component.

</td><td>

1.  Create a page in UI Builder.
2.  Add a stylized text component.
3.  Add a form component pointing to a table + view that shows only one field of the type 'HTML'.

 Expected behavior: The form component left aligns with previous component.

 Actual behavior: The form component doesn't align.

</td></tr><tr><td>

GlideRecord

 PRB1946744

</td><td>

Querying against the 'numeric value' variable silently fails because casting to 'signed' isn't supported in postgres

</td><td>

The process silently fails and doesn't return any data.

</td><td>

1.  Create a 'Numeric value' variable for a catalog item.
2.  Using a catalog item, create a request item.
3.  Run a filter on sc\_req\_item table with the filter on a variable with either of these filters:
    1.  'is empty'
    2.  'is not empty'
    3.  'greater'
    4.  'less than'

 Expected behavior: The created sc\_req\_item is returned.

 Actual behavior: The process silently fails and doesn't return any data.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1881376

</td><td>

BytesOut is inaccurate

</td><td>

 

</td><td>

1.  Set up a Kafka producer on a local machine using Kafka Java APIs.
2.  Produce a single, large batch of messages.
3.  Wait until the hourly aggregation job runs to populate hermes\_usage\_metrics.
4.  Check in the corresponding value 'Total MB Value Per Hour'.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1888169

</td><td>

Unnecessary logging in syslog by KafkaConsumerRegistry and GlideHermes TopicManager

</td><td>

There are unnecessary 'Information' type logs in the syslog table by the com.glide.hermes. KafkaConsumerRegistry, com.glide.hermes. TopicSynchronizer and com.glide.hermes. GlideHermes TopicManager packages.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1905820

</td><td>

Dashboard accuracy issues

</td><td>

There are two issues with the Application ID 'All' filter: 1. The 'Total Megabytes In' value is doubled with the 'All' filter. 2. When there's a singular day spike in metrics, and all other values are 0, the graph itself reports a 0 value on the spike date despite the graphic implying otherwise.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1944311

</td><td>

Setting glide.sys.date\_format to dd-MMM-yy triggers 'GlideDateTime: Invalid date time' for xmlstats.do? include=hermes

</td><td>

'getLastRunTime' uses 'getDisplayValue\(\)', which can change from the non-default date-time format yyyy-MM-dd when 'glide.sys.date\_format' is updated.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1934992

</td><td>

RCAs for the 'Predict and transfer' AI workflow

</td><td>

Related to ER case summarize, both in Now Assist Portal \(NAP\) and the 'Form' view.

</td><td>

1.  Impersonate as an ER case writer user.
2.  Select the **Summarize** button on the 'ER case' form page.
3.  Select the **Summarize a record** button on the ER case from NAP.

 Expected behavior: RCAs shouldn't be generated.

 Actual behavior: RCAs are generated.

</td></tr><tr><td>

HR Service Delivery

 PRB1942339

</td><td>

Use case chaining isn't happening in case of prediction failure

</td><td>

 

</td><td>

1.  Create a case.
2.  Notice that the Prediction/Transfer agent is called in case prediction fails.

 Expected behavior: Another use case is triggered.

 Actual behavior: Chaining doesn't occur.

</td></tr><tr><td>

HR Service Delivery

 PRB1955226

 [KB2634960](https://hi.service-now.com/kb_view.do?sysparm_article=KB2634960)

</td><td>

Missing Sentiment Analysis Fields / RCA errors from Platform AI Agents and Skills

</td><td>

An RCA error appears within HR Agent Workspace on an HR Case if that Case belongs to one of the following COEs: HR Benefits Case, HR Compensation Case, HR Corporate Communications Case, and HR Global Mobility Case. The RCA is requesting access to the HR Case COEs on behalf of Platform AI Agents and Skills, specifically from the source of the Script Include called SentimentAnalysisProcessor.

</td><td>

1.  Navigate to the COE Configuration module.
2.  Navigate to the HR Cases list view.
3.  Create a case based on one of these COEs \(for example, a Compensation HR Case\).

 On the newly created HR Case page, observe that the **Sentiment** and **Sentiment trend** fields are missing and the RCA error at the top of the page.

</td></tr><tr><td>

HR Service Delivery

 PRB1956115

</td><td>

AIA can't access the HR agents unless the attached RCAs are allowed

</td><td>

RCAs are created while running HR AI Agents with a recent release of NAP. Check if these RCAs have already been added by someone before adding.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1956763

</td><td>

Federated ID for roles \(Regulated Market\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Inbound IP Address Access Control

 PRB1931553

</td><td>

Database connections Pool Exhaustion issue

</td><td>

DBIs fail to establish new connections after approximately 2.5 hours.

</td><td>

 

</td></tr><tr><td>

Integration Authentication

 PRB1960124

</td><td>

Verbose JWT logs use opaque tokens when AuthLog is enabled

</td><td>

There should be helpful logs that trace token validation. Instead, there's a misleading log that says 'AuthLog SEVERE \*\*\* ERROR \*\*\* Auth: \[OAuthJWTTokenService\] Failed to parse JWT token for ServiceNow check'.

</td><td>

1.  Create a client with token\_format as opaque.
2.  Enable the 'glide.auth.debug.enabled' property.
3.  Generate a token from the client.
4.  Send an /api request using that token.
5.  Get the logs.

 Expected behavior: There are helpful logs that trace token validation.

 Actual behavior: There's a misleading log that says 'AuthLog SEVERE \*\*\* ERROR \*\*\* Auth: \[OAuthJWTTokenService\] Failed to parse JWT token for ServiceNow check'.

</td></tr><tr><td>

Integration Hub

 PRB1933193

</td><td>

Configuration data is missing in REST step

</td><td>

The HTTP operation relies upon an output from the IntegrationResolverOp. If it doesn't exist, it falls through and throws an exception.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1948377

</td><td>

KBversioning\(\) script isn't accessible from another scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Licensing Entitlement Engine

 PRB1952965

</td><td>

Long-term fix for the Licensing Engine Job OOM issue related to the unconfirmed users logic

</td><td>

 

</td><td>

1.  Provision an instance with over 500,000 user\_has\_role records and over 100 sys\_group\_has\_role records.
2.  Run the LE job.

</td></tr><tr><td>

Lifecycle Events

 PRB1955284

</td><td>

Bulk Task approvals aren't being generated

</td><td>

BulkTaskMgmtRejectUIIT fails when run in the Zurich branch.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1844590

</td><td>

Fixed queries don't work on 'My list' in workspace

</td><td>

When the user creates 'My List' and adds a condition, the list results don't change and the fixed filter isn't visible. It's working on backend view.

</td><td>

1.  Navigate to SOW or HR workspace.
2.  Navigate to the 'My List' tab.
3.  Add a new list.
4.  Use 'Start from existing' or 'Create your own' to create 'My List' without conditions.
5.  After 'My List' is created, navigate to the 'sys\_ux\_my\_list' table.
6.  Open the list.
7.  Add the 'Fixed query' condition 'Active=True' \(or any other condition\).

 Expected behavior: The list has fixed filters and filtered results.

 Actual behavior: The list results don't change and the fixed filter isn't visible \(but it's working on backend view\).

</td></tr><tr><td>

List Administration

 PRB1911269

</td><td>

SHOW\_ALL event is dispatched on every context action click

</td><td>

 

</td><td>

1.  Create an experience.
2.  Add the record list bundle.
3.  Open the page.
4.  Select the **Row edit** icon.

 Expected behavior: The SHOW\_ALL event isn't dispatched.

 Actual behavior: The SHOW\_ALL event is dispatched.

</td></tr><tr><td>

MID Server

 PRB1944968

</td><td>

'ReferenceError: 'RP' is not defined.' error appears when the MID Server form is used in any workspace

</td><td>

When the user opens a page containing the MID Server form in UI builder, error alerts appear with the message: 'ReferenceError: 'RP' is not defined'. This is because RP is only supported in legacy UI.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1951413

</td><td>

Search cards based on external content can't be configured on fields created on the external content table

</td><td>

Creating a search card based on an external connector-based table allows only certain fields to be visible. After the configuration of the mobile search card, find that the created field for **mobile\_url** can't be used in the card for navigation.

</td><td>

1.  Navigate to the instance.
2.  Impersonate a user.
3.  Navigate to the portal.
4.  In the global search, search for the keyword 'lays'.
5.  Notice that the results are displayed.
6.  Navigate to the 'News' tab to view the results.
7.  Open the Now mobile app.
8.  Log in to the mobile app.
9.  Impersonate Abel Tuter in Now mobile.
10. Search for 'lays' in global search.

 Notice that no results are seen under the 'News' tab.

</td></tr><tr><td>

Now Assist Panel

 PRB1867538

</td><td>

Copy for synthesized responses \(auto-start\) on Now Assist panel \(NAP\) doesn't work and copies 'undefined'

</td><td>

When using the Now Assist panel \(NAP\) and entering 'Summarize a record', the **Copy** icon on the auto-started synthesized response doesn't copy the content, and instead, 'undefined' is copied. When 'Undefined' is copied instead of the content and the synthesized response isn't auto-started, there's no **Copy** icon and **Like/dislike** is shown instead.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1943530

</td><td>

High frequency one\_extend\_rate\_ limit\_violation\_cache flushes, causing system slowness

</td><td>

During routine operations, multiple nodes experienced high memory usage and glide.cs.worker thread pressure, resulting in frequent node restarts. Investigation indicates that the one\_extend\_rate\_ limit\_violation\_cache flush events were triggered at an unusually high frequency \(over 5000 times within a 30-minute window\), which may have contributed to the observed slowness. Analysis suggests that excessive cache flushes can create significant memory and performance pressure on the system.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1959167

</td><td>

Support copy action for synthesized response in legacy NAP

</td><td>

Currently there's no copy option for SR.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1955917

</td><td>

Implement cache for sys\_generative\_ai \_request\_validator

</td><td>

Cache is missing for sys\_generative\_ai \_request\_validator.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1948407

</td><td>

Error message appears when duplicating a Platform Analytics dashboard

</td><td>

When duplicating a Platform Analytics dashboard, the error message 'Duplicating dashboard failed. Please try again' appears, even if the dashboard is actually duplicated. This happens when par\_dashboard\_user\_metadata .cache\_expiration\_time is set to -1.

</td><td>

1.  In a Yokohama instance, create a Platform Analytics dashboard.
2.  Navigate to the par\_dashbaord\_user\_metadata table.
3.  Update the column cache\_expiration\_time =-1.
4.  Duplicate the dashboard.

 Observe that the error message 'Duplicating dashboard failed. Please try again.' is shown, even though the dashboard is duplicated.

</td></tr><tr><td>

Process Mining

 PRB1951278

</td><td>

Uppercase sys\_ids for cases break the log collection

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Procurement

 PRB1962139

 [KB2625821](https://hi.service-now.com/kb_view.do?sysparm_article=KB2625821)

</td><td>

Enable stockroom receiving for assets which are part of PO

</td><td>

The script include POReceiveManager is essential for receiving Purchase Orders \(PO\), but in pre-Zurich releases, it's restricted to global scope. Due to this limitation, assets associated with a PO can't be received using the Stockroom Receiving feature. When attempting to receive assets, the following error is displayed: 'Unable to receive the asset. Use the Procurement module or update to the Zurich release or later to continue.'

</td><td>

1.  On a Xanadu or Yokohama instance, provision an instance with the following applications installed:
    1.  Hardware Asset Management 13.0
    2.  Asset Management Common 13.0
2.  Create a PO for a hardware model.
3.  Import the assets using ASN.
4.  Attempt to receive the assets using one of the following UI actions on the stockroom form:
    1.  Receive assets
    2.  Import assets

 Expected behavior: Assets are received successfully.

 Actual behavior: The error message appears, and the asset can't be received.

</td></tr><tr><td>

Project Management

 PRB1940869

</td><td>

Cost plans aren't visible in the EAC widget for the role it\_project\_manager

</td><td>

Only actuals are visible in the EAC/forecast widget. Planned cost values aren't considered, so the widget shows the incorrect value. An error message also appears.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1943581

</td><td>

An error message appears when creating a project from demand

</td><td>

The error message reads: 'An investment for this project already exists. You cannot create a duplicate investment for a project'.

</td><td>

 

</td></tr><tr><td>

Resource Diagnostics

 PRB1941814

</td><td>

Cross scope restriction on adding the record into the Planned task Recalculation Exclusions table

</td><td>

The record can only be added when the scope is switched to GRC: Audit Management.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1910117

</td><td>

Multi-select default values don't populate a field in the right way

</td><td>

When the UI component is associated with a sys\_id, the display value isn't being fetched and set to the field. When a preview of the item is opened, the value is available in the UI.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1930648

</td><td>

The **excel row** field isn't populated for standard import

</td><td>

The **excel\_row** field should be populated with information from the row in an imported file corresponding to that import error, but it's empty.

</td><td>

1.  Import a standard import document from the samp\_bulk\_import table.
2.  Open an import error record generated from the import.
3.  Check the **excel\_row** field from the XML.

 Expected behavior: The **excel\_row** field should be populated with information from the row in the imported file corresponding to that import error.

 Actual behavior: The **excel\_row** field is empty.

</td></tr><tr><td>

Software Asset Management

 PRB1957179

</td><td>

Enhancement of the DocuSign integration

</td><td>

This enhancement supports subscription and envelope consumption data retrieval at the organization level using the Data feed API, addressing demands for aggregated metrics across multiple subaccounts. As a result, DocuSign now has two integration options: account level \(existing integration\) and organization level.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Workspace \(Glide\)

 PRB1945089

</td><td>

Filter out installs requiring action if they have an insufficient rights unlicensed reason and vice versa

</td><td>

 

</td><td>

1.  Create per user entitlement with insufficient rights.
2.  Create per core entitlement.
3.  Create some installs with missing CI infrastructure details, like core count.
4.  Run recon.

 Observe that installs get double counted.

</td></tr><tr><td>

Software Asset Management Workspace \(Glide\)

 PRB1945093

</td><td>

Unlicensed install progress indicators don't show records on the parent product result

</td><td>

Unlicensed installs, installs requiring action, and ignored installs filter by the current product result. However, when running recon with grouping, the parent product result isn't stamped on any install directly. Installs should be linked with all child product results when selecting from the top parent product result indicators.

</td><td>

1.  Provision an instance with SAMP and workspace installed.
2.  Load demo data.
3.  Run recon with grouping company.
4.  Navigate to the parent product result level in the LWB tree.

 Expected behavior: All installs from child product results are shown on the top level.

 Actual behavior: There are 30 installs in 'Unlicensed installs'. When you select it, no records show. The same is true for 'installs requiring action' and 'ignored installs' for any top-level product result.

</td></tr><tr><td>

Software Asset Management Workspace \(Glide\)

 PRB1948990

 [KB2566943](https://hi.service-now.com/kb_view.do?sysparm_article=KB2566943)

</td><td>

In Yokohama, Health Check links redirect to a 'samp\_scan\_finding' table that doesn't exist

</td><td>

The '\# issues found through health check' link redirects to a 'samp\_scan\_finding' table that doesn't exist. The table is added in the 3.x.x version of the ITAM Health Check application, but 3.x.x isn't compatible with the Yokohama release.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Normalization

 PRB1857676

 [KB2472347](https://hi.service-now.com/kb_view.do?sysparm_article=KB2472347)

</td><td>

Discovery model's Discovered Product doesn't match the software install's Display Name

</td><td>

Discovery model's Discovered Product doesn't match the software install's Display Name when override edition \(or any other primary key related field\) is updated on a software install after the install has already been at least partially normalized.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reclamation

 PRB1870503

</td><td>

The error message 'Cannot find the profile type configuration in the script routing table' should be reworded

</td><td>

When the user tries to reclaim a candidate, the error message says 'Cannot find the profile type configuration in the script routing table'. Related reclamation candidates aren't removed. Instead, the error message should clearly state how to reclaim the subscription.

</td><td>

 

</td></tr><tr><td>

System Export Sets

 PRB1926120

</td><td>

Node errors due to messages sent when Hermes/Kafka is unavailable or slow

</td><td>

When Hermes/Kafka clusters are down or running slowly, LES can't check their health before sending messages. As a result, the producer client keeps retrying, and without any pause or queue in place, these repeated attempts can eventually push the node into an error state.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1962239

</td><td>

When the territory model is active, the MP auto push events are generated endlessly

</td><td>

When the territory model is active and auto push in MP is enabled, duplicate auto push events are generated endlessly.

</td><td>

1.  Enable the territory model.
2.  Create WO and WOT.
3.  Make sure that auto push is enabled and progressive push is disabled.
4.  Qualify the WOT to update the state from **Draft** &gt; **Pending dispatch** \(this triggers the task filter\).

 Expected behavior: One event per WOT is created for auto push

 Actual behavior: Duplicate auto push events are created endlessly.

</td></tr><tr><td>

UI Field Administration

 PRB1870246

</td><td>

In SOW, the user is unable to add the date in the start and end date fields using numeric input in the change request page under Schedule

</td><td>

The user isn't able to add the dates using numeric input in the Start and End date field. The characters are immediately removed, and keyboard users are forced to use the datepicker to select a date.

</td><td>

 

</td></tr><tr><td>

User Criteria for Service Catalog

 PRB1867417

</td><td>

User criteria take an extended amount of time to evaluate user roles when there are duplicate CS

</td><td>

When end users have a large number of roles, User Criteria iterates through all of them regardless of whether they're duplicate roles or not. This causes performance issues with loading KB Articles. It also intermittently impacts the first time that you load a KB article because the results of the UC are cached for some time after that.

</td><td>

1.  Impersonate a user with over 1,000 roles.
2.  Navigate to a specific KB article in a portal.

 Observe that the initial load is slow.

</td></tr><tr><td>

UX Framework

 PRB1886937

</td><td>

Issue with QCO closing out without 'click' of mouse

</td><td>

The QCO modal should stay open unless a click is initiated from outside of the dialogue box.

</td><td>

1.  Check out an item using QCO.
2.  In any free text box \(e.g. 'Reason for Purchase'\), highlight the entered value without releasing the mouse button.
3.  Navigate outside of the dialogue box and release.

 Expected behavior: The QCO modal stays open unless a click is initiated from outside of the dialogue box.

 Actual behavior: The QCO modal disappears and all info is lost.

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB1946310

</td><td>

Jobs don't always resume on AHA v3

</td><td>

When transferring to AHA 2.0, the job restarts.

</td><td>

1.  Create an on-demand job that runs for at least 5 minutes.
2.  Start the job.
3.  Initiate an AHA 2.0 transfer.

 Notice that after the transfer completes, the on-demand job automatically restarts.

</td></tr><tr><td>

Virtual Agent

 PRB1849670

</td><td>

Serialization of RichControl.UiMetadata includes the Asynchronous Message Bus \(AMB\) API

</td><td>

The AMB API shouldn't be serialized. AMBMessagePublisher gets serialized because it's stored as a field in ChatbotLogger.java. It gets serialized because something tries to serialize RichControl.UiMetadata, which has ChatbotLogger as a field.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1891918

</td><td>

The Now Assist panel shows misleading notifications indicator

</td><td>

The Now Assist chat window shows incorrect unread history. The count should be 0 when all closed chats are read. It also looks like the Now Assist panel isn't showing all the chat history records for the user, even though the icon shows that there are active chats.

</td><td>

1.  Impersonate the user System Admin on an instance.
2.  Open the Now Assist panel from the header bar.
3.  Select the **All Chats** button.
4.  Observe that many closed chats show the blue 'new' indicator, even though they're multiple weeks old.
5.  Select an old chat with a blue indicator.

 Observe that the count doesn't decrease even after reading the older chat. Selecting the **Close all chats** button also doesn't seem to do anything.

</td></tr><tr><td>

Virtual Agent

 PRB1920893

</td><td>

Suggestion message is only displayed in French after English input

</td><td>

If the VA detects English input from a French profile, it suggests switching to English. However, the suggestion message is only displayed in French, not in both languages. It works correctly with an English profile and French input.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1926973

</td><td>

Links data aren't included in a synthesized response in a transcript

</td><td>

 

</td><td>

1.  Start a Now Assist conversation.
2.  Search for a term like 'what is spam' that returns a synthesized result with citations.
3.  Let the conversation complete.

 Observe that the transcript includes synthesized responses with numbers like \[1\], \[2\]. It should include links as well.

</td></tr><tr><td>

Virtual Agent

 PRB1928402

</td><td>

Virtual Agent Enhanced chat translation doesn't work on Chat menu items

</td><td>

When enhanced Chat is enabled in Virtual Agent and the user's language is set to anything other than English, the submenu labels—Activities, Updates, and Closed—don't get translated when accessed.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1936445

</td><td>

Instance is getting 'session out' because the AI user doesn't work properly

</td><td>

During the agentic workflow, the instance calls the image processor agent and asks to upload an image. After some time, the session times out. This only happens for the AI user. It works correctly for the dynamic user.

</td><td>

1.  Log in to an instance.
2.  Navigate to AI Studio.
3.  Select **Create Work Order**.
4.  Save it.
5.  Try to create a work order with a description.
6.  Say yes to create a work order.
7.  When it asks to upload an image, select the link.
8.  Attach an image from local.

 Expected behavior: It doesn't session out. Ideally, it should attach the image to the work order.

 Actual behavior: The instance says 'session out' and logs out the user. Every time the user attempts to log in again, it immediately logs out.

</td></tr><tr><td>

Virtual Agent

 PRB1937033

</td><td>

Agent statements containing URLs aren't translated for a chat user when DTAC is active

</td><td>

The One API Service Plan Feature Invocation call shows that translation takes place, but the translated text isn't incorporated into the sys\_cs\_message and isn't displayed to the chat user.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1939997

</td><td>

Non-actionable notifications in Virtual Agent aren't cleared when load\_active\_only is set to true

</td><td>

Non-actionable notifications in Virtual Agent appear to only get cleared when skip\_load\_history is true.

</td><td>

1.  Log in to a Yokohama instance.
2.  Impersonate an ITIL User.
3.  On one tab, navigate to incident.list.
4.  Assign any incident record to ITIL User.
5.  On another tab, navigate to /sp.
6.  Open the VA.

 Observe that the non-actionable notifications remain present.

</td></tr><tr><td>

Virtual Agent

 PRB1941596

</td><td>

Synthesized output isn't captured in the interaction transcript for Employee Center Pro Plus \(EC Pro Plus\)

</td><td>

The synthesized output from the Now Assist Virtual Agent \(NAVA\) conversation isn't found in the transcript.

</td><td>

1.  Start a Now Assist Virtual Agent \(NAVA\) conversation.
2.  Enter, 'What is a cookie?' into the conversation.
3.  End the conversation.
4.  Open the interaction\_list table.
5.  Open the interaction created in step 1.

 Expected behavior: In the Transcript section, the synthesized response is found.

 Actual behavior: The synthesized output isn't captured in interaction transcript.

</td></tr><tr><td>

Virtual Agent

 PRB1942112

</td><td>

unreadMessage API fails in NASS / NAVA

</td><td>

unreadMessage API shouldn't fail in NAVA.

</td><td>

1.  Launch NAVA from chat launcher on the 'Home' screen.
2.  Complete a request for a loaner laptop.
3.  Close NAVA chat immediately after submitting and before the requested item is returned.

 Notice that unreadMessage API fails in NAVA.

</td></tr><tr><td>

Virtual Agent

 PRB1942159

</td><td>

Conversations that already have diverted to Live Agent are timing out

</td><td>

 

</td><td>

1.  Start a NAVA chat with a search phrase.
2.  While waiting for the result, select the **Contact Live Agent** \(Contextual Action\) button.
3.  Conduct a live agent chat.
4.  Within 30-60 seconds, the conversation times out.

</td></tr><tr><td>

Virtual Agent

 PRB1943087

</td><td>

AI Search for semantic filters shouldn't be executed if no filters are returned

</td><td>

With semantic filters enabled, no filters are configured for the assistant. AI Search is getting executed for semantic filters.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1943158

</td><td>

Dynamic topic block switch should ignore the scope for system topics

</td><td>

 

</td><td>

Scenario 1:

 1.  Create and publish a topic block in some scope A \(not global\).
2.  Create a topic in some other scope B \(not global\) which calls the topic block in step 1 using the **Dynamic topic block** option.
3.  Execute the topic from step 2.

 Expected behavior: An error.

 Actual behavior: An error \(the chat says 'Sorry, ...'\).

 Scenario 2:

 1.  Add the 'system' category to the topic block from step 1 and republish.
2.  Execute the topic from step 2.

 Expected behavior: The topic block runs successfully.

 Actual behavior: An error \(chat says 'Sorry, ...'\).

</td></tr><tr><td>

Virtual Agent

 PRB1944247

</td><td>

Remove skillID check in sendInteractiveViewControl to support AI Agent

</td><td>

sendInteractiveViewControl needs be improved to support AI Agent. AI Agent doesn't have a skill ID.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1947698

</td><td>

Only one agentic workflow executes successfully when the same trigger fires simultaneously

</td><td>

When a workflow trigger fires simultaneously multiple times, only one of the resulting agentic workflows executes successfully. The other workflows terminate immediately with an error indicating that no session ID could be found. Each trigger correctly creates an execution plan and a new conversation record, but only one conversation proceeds, while the others fail at the start.

</td><td>

1.  Create the agentic workflow named 'Test multiple case executions'.
2.  Select three or more case records.
3.  Update them simultaneously so that the trigger fires for all at once.
4.  Notice that the three execution plans \(sn\_aia\_execution\_plan\) and three conversation records are created. Only one conversation and execution plan executes successfully. The other conversations don't continue after the first task with the error 'No session ID found'.

 Expected behavior: Each triggered workflow should independently create or resolve its own valid session so that all conversations execute successfully, even under concurrent trigger conditions.

 Actual behavior: Only one conversation executes successfully. The other conversations either terminate immediately or don't continue after the first task with 'No session ID found' error.

</td></tr><tr><td>

Virtual Agent

 PRB1952827

</td><td>

Slot filling is duplicated in the 'Analysis' tab on the VAD 'Test' panel

</td><td>

 

</td><td>

1.  Navigate to Virtual Agent designer.
2.  Open test assistant with the standard chat.
3.  Execute the 'Order coffee' topic until the final step.
4.  Verify slot filling on the 'Analysis' tab.

 Notice that one execution is complete. The summary in the 'Analysis' tab displays slot fills being duplicated.

</td></tr><tr><td>

Virtual Agent

 PRB1956231

</td><td>

vaVars or vaInputs variables set in a script include from an LLM input script area aren't unwrapped

</td><td>

The value should be unwrapped and stored as base type \(i.e. java.lang.String\) in task context. Instead, the value is sent as NativeJavaObject, which leads to an xstream serialization exception.

</td><td>

1.  Create a script include that takes vaVars as a variable.
2.  In that script include, set a variable on vaVars: vaVars.time = global.VAClickMetrics. getCurrentTime\(\); from an LLM input node script area \(like Dynamic Choice Picker\).
3.  Create an instance of this object.

 Expected behavior: The value is unwrapped and stored as base type \(i.e. java.lang.String\) in task context.

 Actual behavior: The value is sent as NativeJavaObject, which leads to an xstream serialization exception.

</td></tr><tr><td>

Virtual Agent

 PRB1960129

</td><td>

Conversation abruptly ends after a cold start conversation with pre-chat survey enabled

</td><td>

The conversation ends after the survey is complete.

</td><td>

1.  Enable pre-chat survey.
2.  Navigate to Teams.
3.  Type 'what is spam'.
4.  Complete the pre-chat survey.

 Expected behavior: The user should get a response related to the query from step 3.

 Actual behavior: The conversation ends after the survey is complete.

</td></tr><tr><td>

Virtual Agent

 PRB1967329

</td><td>

QnA utterances in NAVA are missing 'Let me look up information related to ...' before it generates the response

</td><td>

In NAVA, when the user enters the utterance 'What is spam?', the user should see 'Let me look up information related to ...' before a response is generated. However, it goes directly to 'View AI Steps' followed by the actual response.

</td><td>

 

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1956730

</td><td>

Live agent only mode doesn't work for third-party channels

</td><td>

The user messages aren't received by the agent. This message appears in the log: 'Couldn't find rich control, dropping current message'.

</td><td>

1.  Set up VA and a third-party channel \(for example, Teams\).
2.  Set up VA to live-agent only mode \(for example, by having a custom greeting topic that directs to LA\).
3.  Start the conversation.
4.  Accept as an agent.
5.  Attempt to send messages as a user.

 Observe that the user messages aren't received by the agent with this message in the log: 'Couldn't find rich control, dropping current message'.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1944963

</td><td>

Support more markdown for text messages and synthesized response

</td><td>

 

</td><td>

1.  Create a KB that has a relative URL in the content.
2.  Send an utterance to Enhanced Chat that results in content from that article.
3.  See an error in the response.

 Expected behavior: The markdown relative URL is rendered correctly.

 Actual behavior: The HTML is broken.

</td></tr><tr><td>

Work Order Management

 PRB1921416

</td><td>

When the 'Populate Agents Daily Schedule' table is executed, it isn't generating records in the 'agent\_daily\_schedule' table

</td><td>

The code should honor both the time formats \[24 and 12 hour formats\] while comparing the start and end time for an agent schedule in the 'Populate Agents Daily Schedule Table' schedule job for scheduled offline downloads in mobile.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1949306

</td><td>

Handle invalid Work Order Task \(WOT\) data when loading it uses more load and fails in Dispatcher Workspace \(DWS\)

</td><td>

The end\_gdt is empty, which is invalid. Performing the add with an invalid GlideDateTime results in an error: 'Cannot invoke 'java.util.Date.getTime\(\)' because'this.fDate' is null: org.mozilla.javascript .JavaScriptException: java.lang .NullPointerException: Cannot invoke 'java.util.Date.getTime\(\)' because'this.fDat' is null. This error occurs because of the invalid date setup. The **actual\_trave\_start** field is empty on the WOT an 'Accepted' state and an 'On Route' substate.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 9 Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2647079)
-   [Yokohama Patch 9 Hotfix 1](yokohama-patch-9-hf-1-PO.md)
-   [Yokohama Patch 9](yokohama-patch-9.md)
-   [Yokohama Patch 8 Hotfix 2](yokohama-patch-8-hf-2-PO.md)
-   [Yokohama Patch 8](yokohama-patch-8.md)
-   [Yokohama Patch 7 Hotfix 6](yokohama-patch-7-hf-6-PO.md)
-   [Yokohama Patch 7 Hotfix 5](yokohama-patch-7-hf-5-PO.md)
-   [Yokohama Patch 7 Hotfix 2b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2612262)
-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

