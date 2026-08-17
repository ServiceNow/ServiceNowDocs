---
title: Create an AI connection for Amazon \(v2.1.2\)
description: Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 2.1.2\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-amazon-v2-1-2.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-08-02"
reading_time_minutes: 1
breadcrumb: [AWS, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for Amazon \(v2.1.2\)

Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 2.1.2\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AWS** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays.

    **Note:** Select the AWS setup instructions link to follow and verify all the prerequisite steps.

4.  Select **I have read the instructions, verified the permissions, and executed the scripts accordingly** check box.

5.  Select **Continue**.

    The setup page appears.

6.  Under Configure Amazon Connection, select **AWS Services\(s\)**

    -   Amazon Bedrock
    -   Amazon Sagemaker
    -   Amazon Bedrock AgentCore
    **Note:** Select the services for which you want to create import schedules. Services that aren't selected will not have import schedules created.

7.  Enter the connection details:

    1.  Enter the **Connection name**.

    2.  Enter the **Access key ID**.

    3.  Enter the **Secret access key**.

8.  Under Configuration properties:

    1.  Enter the AWS region \(Optional\).

    2.  Enter the Target account ID \(Optional\).

    3.  Enter the STS assume role \(Optional\).

    4.  Enter the Management account ID.

    **Note:** AWS region, Target account ID, STS assume role, and Management account ID fields are optional.

    The **Amazon CloudWatch log group name** field appears only when the Amazon Bedrock service is selected.

    If the Amazon CloudWatch log group name field is empty, no schedule import is created.

9.  Select **Create and test connection**.

    A banner displaying Connection verified appears.

10. Select **Continue**.

11. Configure Amazon connection import.

    1.  Open a parent schedule import.

        **Note:** The page displays the scheduled imports for the selected services.

    2.  Select the Active check box.

    3.  Select **Run** according to your preference.

    4.  To run frequency by demand, select **Execute now**.

        **Note:** This is an optional step as schedule imports run according to the schedule.

        Select **Continue**.

12. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

