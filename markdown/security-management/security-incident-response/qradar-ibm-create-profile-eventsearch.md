---
title: Select IBM QRadar rules
description: Based on the IBM QRadar Source, select one or more IBM QRadar rules for the profile.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup IBM QRadar profile, Set up instance, IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Select IBM QRadar rules

Based on the IBM QRadar Source, select one or more IBM QRadar rules for the profile.

## Before you begin

Role required: sn\_si.admin

## About this task

View the available IBM QRadar rules in your ServiceNow AI Platform instance so you know the active IBM QRadar rules for which you want to ingest and create security incidents.

In IBM QRadar, you can identify rules by their origin as System, Override, and User rules. By default, the origin of a rule is linked to a System rule. When you modify a System rule in IBM QRadar, its origin is set as Override.

Click the list in the IBM QRadar Rules List field. A list of active IBM QRadar rules that are present in the IBM QRadar Console is displayed. Select one or more rules from the list and move them to the **Selected** column. Offenses triggered by one or more of the IBM QRadar rules selected are ingested in this profile.

**Rules with the same name**: In the ServiceNow AI Platform instance, a list of active or enabled rules are displayed. If you modify an active or enabled System rule in IBM QRadar, a new Override rule is created. This results in two rules being displayed with the same name in the ServiceNow AI Platform. When this scenario occurs, select both the rules to ingest and create security incidents.

The following figure is an example of a completed form:![IBM QRadar: Create Profile: Select Rules](../image/ibm-qradar-rules-selection.png)

Click **Continue** to proceed to the next step in the wizard.

