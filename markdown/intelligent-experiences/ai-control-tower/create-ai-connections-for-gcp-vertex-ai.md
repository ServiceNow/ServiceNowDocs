---
title: Create an AI connection for GCP Vertex AI \(v1.2.4\)
description: Create an AI connection for GCP Vertex AI in AI Control Tower using the  AI Service Graph Connector for GCP Vertex AI \(version 1.2.4\)
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-ai-connections-for-gcp-vertex-ai.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [GCP Vertex AI, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for GCP Vertex AI \(v1.2.4\)

Create an AI connection for GCP Vertex AI in AI Control Tower using the  AI Service Graph Connector for GCP Vertex AI \(version 1.2.4\)

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower workspace** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AI Connector for Google** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

4.  Check the option **I have read the setup instructions**.

5.  Select **Continue**.

6.  Create Credential with JSON file upload page appears \(Optional\).

    **Note:** If a MID Server isn't available, or you have already generated a certificate, skip this step and use the standard credential setup path instead.

7.  Enter the Credential name.

8.  Click Attach file to upload the JSON file.

9.  Select **Submit**.

    **Note:** Move to step 20.

10. Create **X.509** certificate.

11. Select **New**.

12. Enter the **Name**.

13. Enter the **Key store password**.

14. Select **+Add file** to attach JKS file.

15. Select **Upload** to upload the JKS file.

16. Select **Save**.

    The JKS file is added.

17. Select **Continue**.

    Setup page appears.

18. Enter the details on Create and test connection \(Without JSON file\):

    1.  Enter the **Connection Name**.

    2.  Enter the **Cloud region**.

    3.  Enter the **Service Account Email**.

    4.  Enter the **Keystore**.

    5.  Enter the **Keystore Password**.

    6.  Enter the **Organization Id**.

        **Note:** Selecting MID Server is an option step.

    7.  Select **Continue**.

19. Enter the details on Create and test connection \(With JSON file\):

    1.  Enter the **Connection Name**.

    2.  Enter the **Cloud region**.

    3.  Choose the **Select created credential**.

    4.  Enter the **Organization Id**.

        **Note:** This field is needed only if you're looking to discover agents related to one organization. This is valid only if the service account email has organization level access.

    5.  Select Mid Selection.

    6.  Enter the MID Application.

    7.  Select Create and test connection.

    8.  Select **Continue**.

20. Configure import schedule

    1.  Verify that both the parent scheduled jobs, Discovery and Execution are active as they are shipped out inactive.

        **Note:** Ensure to execute the Discovery scheduled job first.

    2.  Set the run frequency.

    3.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**.

21. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

