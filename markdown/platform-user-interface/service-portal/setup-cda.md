---
title: Set up Cloud Deployment Automation
description: Set up the Cloud Deployment Automation application by configuring the Service Portal page to use the default catalog items.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cloud Deployment Automation, Configure a catalog in Service Portal, Create a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Set up Cloud Deployment Automation

Set up the Cloud Deployment Automation application by configuring the Service Portal page to use the default catalog items.

## Before you begin

-   Request Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).
-   Activate and configure the AWS CloudFormation spoke.
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

        ![Decision record.](../image/cda-decision.png)

    5.  Select the required group, user, or subflow in **Answer**, depending on what the decision table is used for.

        ![Answer record.](../image/cda-answer.png)

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

    ![Select the global value.](../../../build/service-portal/image/global.png)

    1.  Navigate to **Service Portal** &gt; **Portals**.

    2.  Open the **Service Portal** record.

    3.  Click the **Catalogs** tab.

    4.  Click **Edit**.

    5.  Add **Cloud Deployment Automation** to the **Service Portal** list.

        ![Add Cloud Deployment Automation.](../image/cda-add-sp.png)

    6.  Click **Save**.


## What to do next

-   To view the catalog items, navigate to **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Catalogs** and click **Cloud Deployment Automation**.
-   To request a catalog item:

    **Note:** User must have the sn\_acc\_mgmt\_sc.access\_mgmt\_user, ITIL, and Catalog Admin roles to create and submit catalog items.

    1.  Navigate to the Service Portal.
    2.  Click the **Catalog** tab.
    3.  Click **Browse by Categories**.
    4.  Select **Cloud Deployment Automation**.![Cloud Deployment Automation category.](../image/cda-sp-cat.png)
    5.  Select the required action and submit the catalog item. When the request is approved, the associated flow is triggered and the required user can provide the approval. Activities are logged in the catalog item.

        ![Cloud Deployment Automation catalogs.](../image/cda-catalogs.png)


**Parent Topic:**[Cloud Deployment Automation](../concept/cloud-dep-auto.md)

