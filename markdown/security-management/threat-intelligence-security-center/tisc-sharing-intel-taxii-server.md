---
title: Sharing intelligence using TAXII Server
description: You can retrieve threat intelligence from a source TISC instance into a target TISC instance using TAXII collections. This process requires configuration in both the source and target instances.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-02-24"
reading_time_minutes: 2
breadcrumb: [Share Threat Intelligence data between TISC instances, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Sharing intelligence using TAXII Server

You can retrieve threat intelligence from a source TISC instance into a target TISC instance using TAXII collections. This process requires configuration in both the source and target instances.

## TAXII-Based Sharing

TAXII-based sharing enables structured and standardized exchange of threat intelligence between TISC instances. In this model, the source instance exposes intelligence through TAXII collections, and the target instance retrieves that data using a configured TAXII feed.

## Configuring the source TISC instance

Complete the following steps in the source TISC instance before configuring the target instance.

1.  **Configure global sharing rules**:

    Ensure the following are configured and published based on your requirements:

    -   [Outbound Intel Data Exclusion Rules](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-outbound-data-exclusion.html)
    -   [Outbound Intel Sharing Controls](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-outbound-sharing.html)
2.  **Create TAXII collections**: Set up the required TAXII collections in the source TISC instance. For instructions, see [Create a TAXII collection](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-create-taxii-collection.html).

3.  **Create outbound intelligence sharing templates**: Create and publish an outbound intelligence sharing template with the required configuration for TAXII sharing. For instructions, see [Outbound intelligence sharing templates](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-intel-sharing-templates.html).
4.  **Add records to the TAXII collection**: You can add records using either of the following methods:
    -   Ad-hoc addition via the graphical user interface \(GUI\). For more information, see [Add records to a TAXII collection](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-obs-add-taxii-collects.html).
    -   Automated addition using flows. For more information, see [Automate sharing to TAXII collections](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-automated-share-taxii.html).
5.  **Create a TAXII API user for the target TISC instance**: Create a dedicated API user in the source TISC instance for authentication when the target instance connects to fetch intelligence data.

    Assign the role `sn_sec_tisc.taxii_server_api_user`.


## Configuring the target TISC instance

After completing the source configuration, configure the target instance to pull intelligence from the source.

1.  **Create a new TAXII feed**: In the target TISC instance, create a new TAXII feed. For more information, see [Configure a new TAXII feed](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-configure-a-new-taxii-feed.html).
2.  **Configure the discovery service**: Set **Configuration Type** to **Discovery Service URL** and enter the following URL:

    ```
    https://{instance_name}/api/sn_sec_tisc/taxii_server/taxii2
    ```

3.  **Configure Authentication**:
    -   Select **Basic** as the authentication method.
    -   Provide the username and password of the TAXII API user created in the source instance.
4.  **Save** the configuration:

    Validate the connection then click the **Get TAXII Collections** button to retrieve the enabled TAXII collections from the source instance.

5.  **Enable and configure ingestion**:

    1.  Navigate to the collection you want to ingest.
    2.  Enable the collection.
    3.  Specify the **Fetch From Time** and the desired ingestion frequency.
    All records added to the collection in the source instance after the specified time are pulled into the target instance according to the configured schedule.


