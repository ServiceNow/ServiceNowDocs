---
title: Create an AI connection for IBM
description: Create an AI connection for IBM in AI Control Tower using the  AI Service Graph Connector for IBM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-ai-connection-for-ibm.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [IBM, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for IBM

Create an AI connection for IBM in AI Control Tower using the  AI Service Graph Connector for IBM.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **SGC Central** &gt; **Create Connection**.

2.  Select **IBM Watsonx AI** from the list of connectors, and then select **Create connection**.

3.  On the  Review setup instructions  page, select **I have read the setup instructions**, and then select **Continue**.

4.  Select the IBM watsonx AI services.

    1.  Select the services that you want to discover.

        -   **IBM WatsonX Runtime **: Discovers Runtime agents, prompts, and models.
        -   **IBM WatsonX Orchestrate **: Discovers Orchestrate agents, tools, prompts, models, and usage traces.
        **Note:** You can select both services, if required.

    2.  Select **Submit**.

5.  Configure the selected services.

    1.  For Runtime: In the Regions and Deployment spaces activity, enter the region and deployment space ID, and then select **Submit**.

        Alternatively, select **Skip** to discover all accessible regions and spaces.

    2.  For Orchestrate: In the Orchestrate Instances activity, enter a comma-separated list of instance GUIDs \(tenant IDs\) for which discovery should be run.

        Alternatively, select **Skip** to discover all accessible Orchestrate instances.

6.  Configure and test the connection.

    1.  Enter the **Connection name**.

    2.  Enter the **IBM Cloud API Key**.

    3.  Select **Create and test connection** to validate that the API key is working.

    4.  Select **Continue**.

7.  Configure the import schedule.

    1.  Verify that the parent scheduled jobs are active.

        These jobs are shipped as inactive and must be activated manually.

        -   **SG-IBMRuntime-Discovery ** for Runtime .
        -   **SG-IBMOrchestrate-Discovery ** for Orchestrate .
    2.  Set the run frequency for the scheduled import jobs.

        Alternatively, select **Execute now** to execute the import schedule immediately.

    3.  Select **Continue**.

8.  Select the **Confirm connection setup** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

**Note:** The Discovery scheduled job must be executed before viewing discovered data in the CMDB.

