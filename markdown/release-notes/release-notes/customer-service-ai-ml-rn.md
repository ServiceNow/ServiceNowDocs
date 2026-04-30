---
title: Intelligence for CSM release notes
description: The ServiceNow Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
---

# Intelligence for CSM release notes

The ServiceNow® Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Xanadu release.

## Intelligence for CSM highlights for the Xanadu release

-   Create multiple Recommended Actions context records for the same table to create different experiences that are based on criteria such as user attributes or domains.
-   Restart a decision tree in a playbook and retain the history of previous decision tree executions.
-   Enable customers to add decision trees as catalog items in a service catalog.
-   Enable your users to search for decision trees by using keywords and open a decision tree from the search results.

See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) for more information.

**Important:** The following applications are available in the ServiceNow Store.

-   Guided Decisions Experience \(sn\_ga\_exp\)
-   Recommended Actions \(sn\_cs\_nb\_action\)
-   Task Intelligence for Customer Service \(com.snc.csm\_ml\_task\)

For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Recommended Actions - Task Intelligence similarity models integration](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Use similarity models that are integrated with the Task Intelligence \(TI\) admin console to configure, train, and deploy machine learning models.

    -   Resource Generator: The Recommended Actions framework supports a new resource generator that leverages TI similarity models to configure recommendations.
    -   Admin Configuration: Administrators can configure the resource generator to point to TI solutions for predictions and use the topN optional parameter to fetch top recommendations.
-   **Task intelligence for Customer Service - Dependent field predictions**

    Help improve the model performance by identifying the dependent fields in a model before displaying the predicted values.

-   **[Task intelligence for Customer Service - Records prediction](https://www.servicenow.com/docs/access?context=view-prediction-on-field-change&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Predict the configured fields on the case record after entering the short description or description and see the predicted values without saving the case form.

-   **[Task intelligence for Customer Service - On change predictions for interaction record](https://www.servicenow.com/docs/access?context=view-prediction-on-field-change&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Predict the configured fields on the interaction record after entering the short description or description and see the predicted values without saving the form.

-   **[Task Intelligence for Customer Service - Implement Task Intelligence for the CSM Similarity Model:](https://www.servicenow.com/docs/access?context=view-similar-case-recommendations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**
    -   Similar cases recommendations:  Install the Task Intelligence for Customer Service plugin to view the preconfigured open and closed cases that are automatically trained and deployed as recommendations.
    -   Major case recommendations: Install the major issue management plugin and activate the feature as needed to get recommendations.
-   **[Recommended Actions - Create multiple contexts for a single record entity](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Support multiple contexts for the same table, such as the Case table, with one active context record that can be configured for the Recommended Actions component by using a UI Builder input property. By creating multiple contexts, you can create different experiences that are determined by criteria such as user attributes or domains. The recommendations and AI Search results adjust dynamically according to the configured active context.

-   **[Recommended Actions - Attach knowledge article guidance](https://www.servicenow.com/docs/access?context=ra-csm-guidances&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US#section_jgl_1lv_bdc)**

    Enable agents to view and attach knowledge articles to task records and chat interaction records and share articles with customers by using the following guidances:

    -   Attach and share article: Enables the agent to share a recommended knowledge article in a comment, work note, or an email.
    -   Share article in chat interaction: Enables the agent to share a recommended knowledge article in a customer chat.
-   **[Guided Decisions - Run a guidance as a system user](https://www.servicenow.com/docs/access?context=components-installed-with-guided-decisions&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Enable the **guidance\_honor\_subflow** system property to run a guidance in a decision tree as the user that is specified in the guidance action subflow properties. If this property is set to false, the guidance runs as the current user.

-   **[Guided Decisions - Decision Tree as a catalog item content type](https://www.servicenow.com/docs/access?context=service-def-config-catalog-items&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Enable customers to add decision trees as catalog items in a service catalog. From the Customer Service Portal, customers can select the decision tree and open it in a new tab.

-   **[Guided Decisions - Search for decision trees on portal](https://www.servicenow.com/docs/access?context=search-service-portal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Enable portal users to search for decision trees with keywords. Selecting a decision tree in the search results opens a page with the decision tree widget.

-   **[Guided Decisions - Enable a start node to contain only task input](https://www.servicenow.com/docs/access?context=guided-decision-tree-node-types&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Create start nodes for a decision tree that start directly from a task input and create paths that are derived from the data in the task reference. You have the option to create a start node from a question or from task input.

-   **[Guided Decisions - Restart a decision tree in a playbook](https://www.servicenow.com/docs/access?context=add-guided-decision-playbook&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Restart the execution of a decision tree. When a user completes the execution of a decision tree in a playbook, they can start and complete the decision tree again if desired. Restarting the playbook retains the history of the previous decision tree executions.


## Changed in this release

-   **[Guided Decisions - Question field updated to type HTML](https://www.servicenow.com/docs/access?context=guided-decision-tree-node-types&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The **Question** field has been updated from type=string to type=HTML. When adding a question to a decision node, decision tree authors can include the text, formatted text, and images in the **Question** field.


## Activation information

Install the Guided Decisions, Recommended Actions, and Task Intelligence applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Provide the service and support that your external customers need with Customer Service Management.

-   **[Now Assist for CSM](../analytics-intelligence-reporting/now-assist-rn.md)**

    Summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes with the ServiceNow® Now Assist for CSM application.

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Extract the data from documents and integrate the data into automation workflows to save time and resources by using the Document Intelligence artificial intelligence \(AI\) solution.

-   **[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Improve processes across the platform, such as automatically populating fields during case creation, categorizing and routing work, and recommending resolutions for cases through the Predictive Intelligence artificial intelligence.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

