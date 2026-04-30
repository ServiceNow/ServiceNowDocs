---
title: Task Intelligence for ITSM release notes
description: The ServiceNow Task Intelligence for ITSM application uses machine learning to set up, deploy, and track solution-based models to achieve important business outcomes. Task Intelligence for ITSM was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Task Intelligence for ITSM release notes

The ServiceNow® Task Intelligence for ITSM application uses machine learning to set up, deploy, and track solution-based models to achieve important business outcomes. Task Intelligence for ITSM was enhanced and updated in the Xanadu release.

## Task Intelligence for ITSM highlights for the Xanadu release

-   Set up and configure a new training similarity model that identifies similarities between the fields of an incident table and a selected training table.
-   Set up a similarity model using a similarity template card or the Incident Similarity model to provide recommendations for similar records on incident records and reduce handle time for agents.
-   Set up the prediction preferences for a similarity model, train it with your data, and deploy the model to predict similar records.
-   Track and monitor the performance of a deployed similarity model.
-   Edit, train, and redeploy a similarity model based on the performance results.
-   Manage how frequently the models are automatically retrained by setting the training frequency during model configuration.
-   Staring in version 7.0.0, you can do the following:
    -   Specify the purpose of a similar prediction model and configure the prediction preferences.
    -   Set up and configure a new similarity model- **Similar open Change Requests for Incidents** to predict similar change requests based on the fields configured.
    -   Set up and configure a new similarity model **Similar open Problems for Incidents** to predict similar problems based on the fields configured.
    -   Choose the set of records used for training the similar incident model by selecting the conditions on the training tables and training fields for training the similarity models.

See [Task Intelligence for ITSM](https://www.servicenow.com/docs/access?context=c-itsm-task-intelligence&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

**Important:** Task Intelligence for ITSM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Set up a similarity model](https://www.servicenow.com/docs/access?context=using-task-intelligence-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Set up and configure a similarity model that learns the patterns of similarity between two types of tables by comparing their fields.

    You can use the similarity template card to set up a new similarity model or select the Incident Similarity model available in the base system.

-   **[Metrics of similarity model](https://www.servicenow.com/docs/access?context=admin-console-ti&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    View the number of predictions made by a selected similarity model and the number of incidents records that provided predictions.

-   **[Edit and redeploy the model](https://www.servicenow.com/docs/access?context=edit-your-model&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    You can edit, retrain, and redeploy a similarity model to enhance the performance based on the model performance and impact.


## Changed in this release

-   **[Classification model renaming](https://www.servicenow.com/docs/access?context=create-incident-prediction-model&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The classification model available with the base system has been renamed from **ITSM OOTB TI Solution** to **Incident Categorization**.

-   **[Monitoring and Analytics](https://www.servicenow.com/docs/access?context=task-intel-monitor-analystics&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    You can now view the number of records predicted by the similarity models in the Task intelligence analytics page.


-   **[Updated Load Records icon](https://www.servicenow.com/docs/access?context=create-a-similar-records-prediction-model-in-task-intelligence-for-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Starting in version 7.0.0, you can now viw the updated **Load Records** icon on Train the model screen.


## Activation information

Install Task Intelligence for ITSM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    ServiceNow® Service Operations Workspace is a configurable workspace that provides a unified experience for multiple IT Service Management and IT Operations Management workflows. Configure your agent experience using the interface of Service Operations Workspace for ITSM.

-   **[Exploring Recommended Actions for ITSM in Service Operations Workspace](https://www.servicenow.com/docs/access?context=exploring-recommended-actions-for-itsm-in-service-operations-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    ServiceNow® Advanced Recommended actions for ITSM enables you to configure and display relevant actions to agents based on record context. Agents can use these actions to help customers and resolve issues.

-   **[Machine learning solutions for IT Service Management](https://www.servicenow.com/docs/access?context=machine-learning-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Machine learning in IT Service Management enhances business scalability and improves business operations for organizations.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

