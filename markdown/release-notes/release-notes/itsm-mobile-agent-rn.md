---
title: ITSM Mobile Agent release notes
description: The ServiceNow ITSM Mobile Agent app delivers base system, mobile-first experiences designed for IT agents to triage, act on, and resolve incidents on the go. ITSM Mobile Agent was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# ITSM Mobile Agent release notes

The ServiceNow® ITSM Mobile Agent app delivers base system, mobile-first experiences designed for IT agents to triage, act on, and resolve incidents on the go. ITSM Mobile Agent was enhanced and updated in the Yokohama release.

## ITSM Mobile Agent highlights for the Yokohama release

Starting in the 9.1 release, you can do the following:

-   Summarize the incident record and activity information when adding work notes to an incident record or while reassigning an incident.
-   Set different alert tones for incidents with different priority levels.
-   Set the incident impact and urgency levels to set the incident priority level automatically.
-   Redirect from the mobile web browser to the ITSM Mobile Agent app seamlessly when opening and viewing different task records.

See [ITSM Mobile Agent](https://www.servicenow.com/docs/access?context=itsm-mobile-agent&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

**Important:** ITSM Mobile Agent is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Summarize the incident record and activity information](https://www.servicenow.com/docs/access?context=gen-inc-rec-task-summariz&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    When adding work notes to an incident record, use the GenAI task summarization capabilities to summarize an incident record and activity information, such as the issue details or actions taken.

    You can also summarize the incident information when adding work notes when reassigning the incident record. After an information summary is generated, you can edit and add the information as work notes. This feature helps reduce the effort required to draft work notes. The feature is available in the following applets:

    -   My team applet
    -   Major incidents
    -   My work
    To enable this feature in ITSM Mobile Agent, you must configure the Incident summarization skill in Now Assist for ITSM.

-   **[Set alert tones for incident with different priority levels](https://www.servicenow.com/docs/access?context=set-alert-tones-incident-priority&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Set alert tones for incident with different priority levels. The alert tone can notify you of important actions so you can respond to them quickly.

-   **[Email notification redirection behavior](https://www.servicenow.com/docs/access?context=my-work-application&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Redirect from the mobile web browser to the ITSM Mobile Agent app seamlessly when opening and viewing different task records. This feature is applicable on the following type of records:

    -   Incident
    -   Incident task
    -   Catalog task
    -   Change request
    -   Change task
    When you select the record link from an email notification on a mobile device, the link opens in the mobile web browser. A pop-up banner then prompts you to view the record in the ITSM Mobile Agent app, which provides a fast and intuitive way to access the records. This feature is applicable only if the following conditions are met:

    -   The ITSM Mobile Agent application is installed on the mobile device.
    -   The **Enable universal links** \(**glide.sg.universal\_links.enabled**\) system property is set to `true`.
-   **[Set the incident impact, urgency, and priority levels](https://www.servicenow.com/docs/access?context=create-incident-mobile&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Automatically set the incident priority level by defining the impact and urgency levels. This feature determines an incident priority level by maintaining uniform synchronization and consistency between the priority, impact, and urgency levels. When you edit the **Impact** and **Urgency** fields, you must add to the **Work notes** field.


## Activation information

Install ITSM Mobile Agent by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

