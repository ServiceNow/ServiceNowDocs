---
title: Intelligence for CSM release notes
description: The ServiceNow Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Intelligence for CSM release notes

The ServiceNow® Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Zurich release.

## Intelligence for CSM highlights for the Zurich release

-   Get enhanced visibility of knowledge base articles by marking and displaying a lock icon for articles that aren’t accessible to the case requester within the CSM Configurable Workspace.
-   Gain insights to the root causes of case service level agreement \(SLA\) breaches and view the suggested improvements to optimize process performance.

See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) for more information.

**Important:** The following applications are available in ServiceNow Store:

-   Guided Decisions Experience \(sn\_ga\_exp\)
-   Recommended Actions \(sn\_nb\_action\)
-   Recommended Actions for Customer Service \(sn\_cs\_nb\_action\)
-   Task Intelligence for Customer Service \(com.snc.csm\_ml\_task\)

For details, see the "Activation information" section of these release notes.

## New in the Intelligence for CSM release

-   **[Guided Decisions - Enable Guided Decisions as a Playbook Activity with Inputs and Outputs](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Added support for the Guided Decision with Inputs and Outputs activity in Playbook. Use this activity to embed decision trees that accept inputs and generate outputs, guiding users through complex decisions within your playbooks.

-   **[Recommended Actions - View the relevancy score of the AI search results](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    View the relevancy score on the search result recommendation cards in the Search tab of the Recommended Actions panel for the default guidance for search results, Attach and share article, Share KB in chat interactions, and all no-code \( Link incident to current case, Link problem to current case, and Link change request to current case\) guidances. To enable this feature, you must enable the Show relevancy score for results check box in the Context form.

-   **[Recommended Actions – Limit the number of search results for more precise output](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Limit the number of search results \(Top N\) that appear in the AI search tab in the Recommended Actions context side panel. To configure top N search results, you must enable the Top N check box in the Context form and then define the Search Results Limit in the Search Application Configuration.

-   **[Recommended Actions - Filter search results across multiple sources in the Contextual side panel](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Filter search results corresponding to multiple sources in the AI search tab of the Recommended Actions contextual side panel. You can also filter the search results at the facet-level.

-   **[Recommended Actions – Track the AI search usage trends with the AI search analytics dashboard](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Track and analyze the AI search usage in Recommended Actions using the AI search analytics dashboard. The AI search events and actions performed by the agent are captured in the Search Events, Search Source Events, Search Signal Events, Search Result Event, and Search Result Event Action tables. This data is used in the AI search analytics dashboard.

-   **[Recommended Actions - Read-only access to TI solutions for the Resource Generator author role](https://www.servicenow.com/docs/access?context=ra-csm-installed-components&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Access Task Intelligence \(TI\) solution definitions in read-only mode as a Resource Generator author \[sn\_nb\_action.resource\_generator\_author\] to configure recommendations with Machine Learning \(ML\) solutions from TI models. In other words, the sn\_ti\_admin.tia\_user role is added to the Resource Generator author role.

-   **[Recommended Actions - Filter search results across multiple sources on the Search page](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Filter search results corresponding to multiple sources on the Search page. You can also filter the search results at facet-level.

-   **[Recommended Actions - Optimize the Recommended Actions refresh behavior by excluding non-critical field updates](https://www.servicenow.com/docs/access?context=ra-csm-contexts-create&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Exclude the non-critical fields from triggering a Recommended Actions refresh on the record pages by adding the non-critical fields to the **Exclude fields** field on a context record. In a child context, you can also include the field exclusions of the parent context. You can enhance a user’s UI experience when you prevent excessive UI updates and still ensure that relevant updates trigger as intended.

-   **[Recommended Actions - Trigger Refresh for Recommendations explicitly or based on UI events](https://www.servicenow.com/docs/access?context=ra-csm-config-data-broker&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Trigger recommendations refresh in the Recommended Actions tab on the contextual side panel when a UI or back-end event update is made. This provides dynamic and more contextually relevant recommendations based on the outcome of UI and back-end events. To trigger a recommendations refresh:

    -   configure UI component’s Data Broker in the UI builder for UI events
    -   execute the ForceRefreshRecommendationsscript include for back-end events
-   **[Recommended Actions - Configure dynamic JSON-based context inputs](https://www.servicenow.com/docs/access?context=ra-csm-create-context-inputs&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Configure JSON-based context inputs in a context to populate accurate recommendations corresponding to dynamically changing contexts. You can conﬁgure parameters associated with the context table along with context table parameters. To support scenarios where a single workflow may leverage multiple active contexts simultaneously to generate recommendations. This uses the context inputs in rule condition builders, resource generators, and recommendation-action mappings, with minimal performance impact and backward compatibility.

-   **[Recommended Actions - Enhanced KB article sharing for Agents](https://www.servicenow.com/docs/access?context=ra-csm-guidances-attach-share-article&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Identify the Knowledge Base \(KB\) articles that are not accessible to the case requester with the help of a Lock icon. In the recommendations on the contextual side panel of the CSM Configurable Workspace, a Lock icon on a recommendation card denotes that the recommended KB article cannot be accessed by the case requester.

-   **[Process Mining - SLA breach analysis](https://www.servicenow.com/docs/access?context=csm-integration-po&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Identify and analyze cases where service level agreements \(SLAs\) have been violated. The SLA breach analysis project provides insights into the root causes of breaches, highlights bottlenecks, and recommends improvements to optimize the performance of your processes.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


## UI changes

-   **[Recommended Actions - The primary call-to-action changes on the KB article recommendation card](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    The primary call-to-action \(CTA\) on a recommended knowledge base article is determined by the source channel of the case. If the case originates from an email, the primary CTA displayed is Attach and share link in the email. For all the other channels, the primary CTA is Attach and add link in comments. If the article isn’t accessible to the requester, the primary CTA is set to Read article. Accessible articles display the full set of actions \(Attach and add link in comments, Add link in work note, and so on\). Inaccessible articles are limited to internal-use actions only \(Read article, Share link in work notes, and so on\).

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Provide the service and support that your external customers need with Customer Service Management.

-   **[Now Assist for CSM](../analytics-intelligence-reporting/now-assist-rn.md)**

    Summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes with the ServiceNow® Now Assist for CSM application.

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Extract the data from documents and integrate the data into automation workflows to save time and resources by using the Document Intelligence AI solution.

-   **[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Improve processes across the platform, such as automatically populating fields when a case is created, categorizing and routing work, and suggesting case resolutions through Predictive Intelligence AI.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

