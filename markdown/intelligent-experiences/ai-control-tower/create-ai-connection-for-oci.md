---
title: Create an AI connection for AI Service Graph Connector for OCI
description: Create an AI connection for OCI in AI Control Tower using the  AI Service Graph Connector for OCI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-ai-connection-for-oci.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-07-06"
reading_time_minutes: 2
breadcrumb: [OCI, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for AI Service Graph Connector for OCI

Create an AI connection for OCI in AI Control Tower using the  AI Service Graph Connector for OCI.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **SGC Central** &gt; **Create Connection**.

2.  Select **OCI GenAI** from the list of connectors, and then select **Create connection**.

3.  On the Grant attachment update permissions page, enable edit permissions for the Attachment \[sys\_attachment\] table, and then select **Continue**.

4.  On the  Review setup instructions  page, select **I have read the setup instructions**, and then select **Continue**.

5.  Create an X.509 certificate.

    1.  Select **New**.

    2.  Enter the **Name** for the certificate.

    3.  Enter the **Key store password**.

    4.  Select **Add file** to attach the Java KeyStore \(JKS\) file.

    5.  Select **Upload** to upload the JKS file.

    6.  Select **Save**, and then select **Continue**.

6.  Select the source system.

    1.  Select the services that you want to discover.

        -   ** Generative AI**: Discovers base models, custom \(fine-tuned\) models, and imported models.
        -   **Generative AI Agents**: Discovers AI agents, agent-referenced models, AI tools, AI prompts, and agent usage metrics.
        **Note:** You can select both services, if required.

    2.  Select **Continue**.

7.  Configure and test the connection.

    1.  Enter the following details for the connection.

        |Field|Description|
        |-----|-----------|
        |Connection name|Name to identify the OCI connection.|
        |Tenancy ID|The OCID of your OCI tenancy. For example, `ocid1.tenancy.oc1..aaaaaa...`.|
        |User ID|The OCID of the OCI user whose API key is configured.|
        |Key Fingerprint|The fingerprint generated when uploading the public key. See [OCI prerequisites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-sgc-oci.md) and the [Service Graph Connector for OCI - Setup Instructions \[KB2898105\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2898105) article in the Now Support Knowledge Base.|
        |Region|The OCI region identifier. For example, `us-chicago-1`.|
        |Certificate|The JKS certificate. See [OCI prerequisites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-sgc-oci.md) and the [Service Graph Connector for OCI - Setup Instructions \[KB2898105\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2898105) article in the Now Support Knowledge Base.|
        |Certificate Alias|The alias used during JKS certificate creation. See [OCI prerequisites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-sgc-oci.md) and the [Service Graph Connector for OCI - Setup Instructions \[KB2898105\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2898105) article in the Now Support Knowledge Base.|
        |Certificate Alias Password|The alias password used during JKS certificate creation. See [OCI prerequisites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-sgc-oci.md) and the [Service Graph Connector for OCI - Setup Instructions \[KB2898105\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2898105) article in the Now Support Knowledge Base.|
        |Compartment ID \(optional\)|The OCID of a specific compartment to scope discovery to that compartment and its sub-tree. If no value is specified, the entire tenancy is discovered.|

    2.  Select a MID Server.

    3.  Select **Create and test connection**, and then select **Continue**.

8.  Configure the import schedule.

    1.  Verify that the parent scheduled jobs are active.

        These jobs are shipped as inactive and must be activated manually.

        -   **SG-OCIGenAI-Discovery** for Model Track .
        -   **SG-OCIGenAIAgents-Discovery ** for Agent Track.
        -   **SG-OCIGenAIAgents-Usage ** for Usage metrics.
    2.  Set the run frequency for the scheduled import jobs.

        Alternatively, select **Execute now** to execute the import schedule immediately.

    3.  Select **Continue**.

9.  Select the **Confirm connection setup** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

**Note:** The Discovery scheduled job must be executed before viewing discovered data in the CMDB.

