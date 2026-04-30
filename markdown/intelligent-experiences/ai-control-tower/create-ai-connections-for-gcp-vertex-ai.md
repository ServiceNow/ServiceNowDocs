---
title: Create AI connections for GCP Vertex AI
description: Create an AI connection for GCP Vertex AI in AI Control Tower using the  AI Service Graph Connector for GCP Vertex AI.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-02"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [GCP Vertex AI, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Create AI connections for GCP Vertex AI

Create an AI connection for GCP Vertex AI in AI Control Tower using the  AI Service Graph Connector for GCP Vertex AI.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower workspace** &gt; **Configuration** &gt; **AI connections**.

2.  Select **Add**.

3.  Select **GCP Vertex AI** from all the available connectors.

4.  Click **Create connection**.

    Review setup instructions page displays

5.  Verify to follow all the prerequisite steps.

6.  Check the option **I have read the setup instructions**.

7.  Click **Continue**.

8.  Create **X.509** certificate.

9.  Select **New**.

10. Enter the **Name**.

11. Enter the **Key store password**.

12. Click **+Add file**.

13. Select the JKS file.

14. Select **Upload** to upload the JKS file.

15. Click **Save**.

    The JKS file is added.

16. Select **Continue**.

    Setup page appears

17. Create and test connections

    1.  Enter the **Connection Name**.

    2.  Enter the **Cloud region**.

    3.  Enter the **Service Account Email**.

    4.  Enter the **Keystore**.

    5.  Enter the **Keystore Password**.

    6.  Enter the **Organization Id**.

        **Note:** This field is needed only if you're looking to discover agents related to one organization. This is valid only if the service account email has organization level access.

    7.  Click **Create and test connection**.

    8.  Click **Continue**.

18. Configure import schedule

    1.  Ensure that both the parent scheduled jobs, Discovery and Execution are active as they are shipped out inactive.

        **Note:** Ensure to execute the Discovery scheduled job first.

    2.  Set the run frequency.

    3.  To run frequency by demand, select **Execute now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Click **Continue**.

    5.  Click **View all connections** to view the newly created connection.


## Result

AI connection is created for GCP Vertex AI.

