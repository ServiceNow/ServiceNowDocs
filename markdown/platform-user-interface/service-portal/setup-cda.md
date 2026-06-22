---
title: Set up Cloud Deployment Automation
description: Set up the Cloud Deployment Automation application by configuring the Service Portal page to use the default catalog items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/service-portal/setup-cda.html
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cloud Deployment Automation, Configure a catalog in Service Portal, Create a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Set up Cloud Deployment Automation

Set up the Cloud Deployment Automation application by configuring the Service Portal page to use the default catalog items.

## Before you begin

-   Request Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).
-   Activate and configure the [AWS CloudFormation spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/aws-cloudformation.md).
-   Activate the Cloud Deployment Automation app
-   Role required: admin

## Procedure

1.  Configure the decision tables to perform the required tasks.

    The flows in this application use decision tables to enable admins to configure approvers, assignments, and subflow routing without modifying any of the flows in Workflow Studio. In each decision table by default, you can modify the decision record to select an option \(group, user, or subflow\) that applies to all catalog items in the application. If you want to have different assignments, approvers, or subflows per catalog item, you can add new decisions for each catalog item within the decision tables.

    1.  Navigate to **System Definition** &gt; **Decision Tables**.

    2.  Open the required Cloud Deployment Automation decision table record.

        These steps should be repeated for each decision table.

    3.  Click the **Decisions** tab.

    4.  Click the decision record.

        \[Omitted image "cda-decision.png"\] Alt text: Decision record.

    5.  Select the required group, user, or subflow in **Answer**, depending on what the decision table is used for.

        \[Omitted image "cda-answer.png"\] Alt text: Answer record.

        **Note:** Configure these seven decision tables and assign **Answer** as per your requirements.

        -   CDA Catalog Task Group Assignment Policy
        -   CDA Catalog Task User Assignment Policy
        -   CDA Failed Automation Flow Policy
        -   CDA Incident Group Assignment Policy
        -   CDA Incident User Assignment Policy
        -   CDA Requested Item Group Approval Policy
        -   CDA Requested Item User Approval Policy
2.  Configure the Service Portal page.

    **Note:** Ensure that you select **Default \[Global\]** and **Global** for current update set and application.

    \[Omitted image "global.png"\] Alt text: Select the global value.

    1.  Navigate to **Service Portal** &gt; **Portals**.

    2.  Open the **Service Portal** record.

    3.  Click the **Catalogs** tab.

    4.  Click **Edit**.

    5.  Add **Cloud Deployment Automation** to the **Service Portal** list.

        \[Omitted image "cda-add-sp.png"\] Alt text: Add Cloud Deployment Automation.

    6.  Click **Save**.


## What to do next

-   To view the catalog items, navigate to **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Catalogs** and click **Cloud Deployment Automation**.
-   To request a catalog item:

    **Note:** User must have the sn\_acc\_mgmt\_sc.access\_mgmt\_user, ITIL, and Catalog Admin roles to create and submit catalog items.

    1.  Navigate to the Service Portal.
    2.  Click the **Catalog** tab.
    3.  Click **Browse by Categories**.
    4.  Select **Cloud Deployment Automation**.\[Omitted image "cda-sp-cat.png"\] Alt text: Cloud Deployment Automation category.
    5.  Select the required action and submit the catalog item. When the request is approved, the associated flow is triggered and the required user can provide the approval. Activities are logged in the catalog item.

        \[Omitted image "cda-catalogs.png"\] Alt text: Cloud Deployment Automation catalogs.


**Parent Topic:**[Cloud Deployment Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/service-portal/cloud-dep-auto.md)

