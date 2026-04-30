---
title: Flow Designer and Integration Hub usage with IBM QRadar offense ingestion integration
description: Using the Flow Designer and Integration Hub functionality, several subflows and actions have been built as part of the IBM QRadar offense ingestion integration.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Flow Designer and Integration Hub usage with IBM QRadar offense ingestion integration

Using the Flow Designer and Integration Hub functionality, several subflows and actions have been built as part of the IBM QRadar offense ingestion integration.

The following IBM QRadar subflows are available:

-   Connection and Credential Validation: This is used in the configuration tile for validating the host and credentials in the initial setup.
-   IBM QRadar Rules Retrieval: This is used in the Rules section of the profile setup to retrieve all active rules in IBM QRadar. This subflow is triggered asynchronously.
-   Fetch Sample Offenses Data From IBM QRadar: This is used in the Mapping section of the profile setup to fetch sample data. This subflow is triggered asynchronously.
-   IBM QRadar Offense status updates: This is triggered by a scheduled job every minute and updates the offense in IBM QRadar when the security incident is created or closed.
-   Process Profiles from Scheduled Job and Queue Offenses: This is triggered by a scheduled job every minute to pull offenses per profile based on polling interval. This pulls offenses and queues them to the polling table for further processing.
-   Process Polling Queue and Poll in Batches: This is triggered by a scheduled job every 30 seconds to process the Polling table Queue.
-   Fetch Recent IBM QRadar Flows: This is triggered from the security incident form link to get latest flows of offense.
-   Fetch Recent IBM QRadar Events: This is triggered from the security incident form link to get latest events of offense.

To view these subflows, login as a user with the `sn_si.admin` role and navigate to **Flow Designer** &gt; **Designer**. Click on the Name link of any of the subflows listed above to view the subflow in detail.

