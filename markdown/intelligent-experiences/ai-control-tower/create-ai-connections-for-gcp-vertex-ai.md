---
title: Create an AI connection for GCP Vertex AI
description: Create an AI connection for GCP Vertex AI in AI Control Tower using the  AI Service Graph Connector for GCP Vertex AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-ai-connections-for-gcp-vertex-ai.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [GCP Vertex AI, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for GCP Vertex AI

Create an AI connection for GCP Vertex AI in AI Control Tower using the  AI Service Graph Connector for GCP Vertex AI.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower workspace** &gt; **Configuration** &gt; **AI connections**.

2.  Click **Add**.

3.  Select **GCP Vertex AI** from all the available connectors.

4.  Click **Create connection**.

    Review setup instructions page displays

5.  Verify to follow all the prerequisite steps.

6.  Check the option **I have read the setup instructions**.

7.  Select **Continue**.

8.  Create Credential with JSON file upload page appears \(Optional\)

    **Note:** If you're uploading JSON file, ensure to configure MID server in the next steps.If you have JSON file, skip this step and move to step 12.

9.  Enter the Credential name

10. Click Attach file to upload JSON file.

11. Select **Submit**.

    **Note:** Move to step 21.

12. Create **X.509** certificate.

13. Select **New**.

14. Enter the **Name**.

15. Enter the **Key store password**.

16. Select **+Add file** to attach JKS file.

17. Select **Upload** to upload the JKS file.

18. Select**Save**.

    The JKS file is added.

19. Select **Continue**.

    Setup page appears

20. Create and test connection \(Without JSON file\)

    1.  Enter the **Connection Name**

    2.  Enter the **Cloud region**

    3.  Enter the **Service Account Email**

    4.  Enter the **Keystore**

    5.  Enter the **Keystore Password**

    6.  Enter the **Organization Id**

        **Note:** Selecting MID server is an option step.

    7.  Select **Update and test connection**.

    8.  Select **Continue**.

21. Create and test connection \(With JSON file\)

    1.  Enter the **Connection Name**

    2.  Enter the **Cloud region**

    3.  Choose the **Select created credential**.

    4.  Enter the **Organization Id**

        **Note:** This field is needed only if you're looking to discover agents related to one organization. This is valid only if the service account email has organization level access.

    5.  Select Mid Selection

    6.  Enter the MID Application

    7.  Click Create and test connection

    8.  Click **Continue**

22. Configure import schedule

    1.  Verify that both the parent scheduled jobs, Discovery and Execution are active as they are shipped out inactive

        **Note:** Ensure to execute the Discovery scheduled job first.

    2.  Set the run frequency

    3.  To run frequency by demand, select **Execute now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**.

    5.  Select **View all connections** to view the newly created connection.


## Result

The AI connection for GCP Vertex AI is created and configured.

