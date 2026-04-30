---
title: Ingesting the sample IBM QRadar offenses
description: You can ingest sample offenses for one or more selected IBM QRadar rules.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Map offense fields, Setup IBM QRadar profile, Set up instance, IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Ingesting the sample IBM QRadar offenses

You can ingest sample offenses for one or more selected IBM QRadar rules.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If the mapping form is not displayed, click **Mapping** on the progress bar.

2.  You can either pull the three most recent sample offenses or provide the unique offense IDs for the specific offenses that you want to use for your mapping experience.

    From the **Ingestion Preference** choice list, select one of the following:

    -   Retrieve most recent offenses: The three most recent offenses for the selected rules are retrieved.
    -   Select offenses based on offenses ID: Specify the offense ID for the offenses to be retrieved. You can specify a maximum of 3 offense ids separated by commas.
    ![IBM QRadar: Create Profile: Mapping: Default](../image/ibm-qradar-profile-mapping-default.png)

3.  Click **Fetch Sample Data** to pull the latest sample offense data from the IBM QRadar console for the selected offense rules.

    The offense fields and values results are displayed as individual tabs. An offense can be triggered by three types of rules:

    -   Event: In this rule, event logs are checked and if the specified criteria is met, an offense is created.
    -   Flow: Network data and traffic is checked and if certain conditions are met, an offense is created.
    -   Common: In this case, you can specify conditions for events or flows and either or both conditions are met, an offense is created.
    The pull for sample offenses may take a few moments. A message indicating that the transaction is working is displayed at the top of the screen. Depending on the rule or rules that triggered the offense, along with the offense fields, the event or flow fields are populated as shown in the figure below:

    ![IBM QRadar Mapping Sample offense and Events](../image/ibm-qradar-profile-mapping-mixed.png)

    **Note:** The event or flow fields displayed belong to the first event or flow field that triggered the offense based on the corresponding event or flow rule.

4.  The following are custom offense fields created for this integration.

    Standard offenses fields in addition to these custom fields are available for mapping.

    -   rules\_contributing\_to\_offense: IBM QRadar rules that contributed to the offense based on the Rule ID.
    -   users: User names for the offense
    -   remote\_destination\_ip: The remote destination IPs for the offense.

        Based on the local destination IDs for the offense, the following custom local destination address fields are available:

        -   local\_destination\_address \(domain\_id\)
        -   local\_destination\_address \(event\_flow\_count\)
        -   local\_destination\_address \(first\_event\_flow\_seen\)
        -   local\_destination\_address \(id\)
        -   local\_destination\_address \(last\_event\_flow\_seen\)
        -   local\_destination\_address \(local\_destination\_address\_ids\)
        -   local\_destination\_address \(magnitude\)
        -   local\_destination\_address \(network\)
        -   local\_destination\_address \(offense\_ids\)
        -   local\_destination\_address \(local\_destination\_ip\)
    -   The following source addresses are available based on the source IDs of the offense:

        -   source\_addresses \(domain\_id\)
        -   source\_addresses \(event\_flow\_count\)
        -   source\_addresses \(first\_event\_flow\_seen\)
        -   source\_addresses \(id\)
        -   source\_addresses \(last\_event\_flow\_seen\)
        -   source\_addresses \(source\_address\_ids\)
        -   source\_addresses \(magnitude\)
        -   source\_addresses \(network\)
        -   source\_addresses \(offense\_ids\)
        -   source\_addresses \(source\_ip\)
    Select the **Fetch additional event and flow fields \(Optional\)** check box. You can fetch sample event and flow data from any active, valid custom event and flow fields. Specify the custom fields separated by commas as shown below:

    ![IBM QRadar: Create Profile: Mapping: Custom](../image/ibm-qradar-profile-mapping-custom1.png)

    Click **Fetch Sample Data**. The specified event or flow fields along with their values \(if available\) are appended to the Event or Flow section as shown below:

    ![IBM QRadar: Create Profile: Mapping: Custom: Result](../image/ibm-qradar-profile-mapping-custom2.png)

    After you fetch the sample data, the corresponding values for these fields are populated on the left side of the form.

    ![IBM QRadar: Create Profile: Populated Offenses](../image/ibm-qradar-profile-ingest.png)


## What to do next

After you have fetched the sample data, the next step is map the offense fields to the security incident.

