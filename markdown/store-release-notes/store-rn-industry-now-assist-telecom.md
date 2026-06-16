---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) release notes
description: Version history for the ServiceNow Now Assist for Telecommunications, Media and Technology \(TMT\) application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-industry-now-assist-telecom.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Telecommunications Service Management release notes, ServiceNow Store release notes]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) release notes

Version history for the ServiceNow® Now Assist for Telecommunications, Media and Technology \(TMT\) application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.1 - June 2026**
    -   New support of 3p models and security fixes
    -   Small models: Claude Haiku 4.5GPT‑5 miniLarge Models:Claude Sonnet 4.6GPT‑5.4
-   **Version 1.1.5 - April 2026**

    Repackaging for product tiers

-   **Version 1.0.5 - March 2026**
    -   Generative AI and AI agent collections for Telecommunications. This will include:
        -   Skills:
            -   Customer Service Problem Management for Case Summarization, Test Summarization, KB Generation and Resolution Notes Generation
            -   Skills on C360 for telecommunications for AI summary
            -   Remote hands Skill
        -   AI Agents
            -   Service Test and Repair telecom service issues AI agent
                -   Service Problem ManagerAI agent which will suggest relevant knowledge articles and check for the customer inventory to be active.
                -   Customer Payment Status AI agent which will check outstanding payments.
                -   Preliminary Troubleshooter AI agent to ask questions from the documents and recommend similar cases.
                -   On-demand Service Tester AI agent to show the tests based on the inventory specification if the recommended tests are shown
                -   Service Repairer AI agent to create repair tasks based on the test outcom
    -   Analyze network incidents
        -   This includes the following AI agents:
            -   Network ticket resolution AI Agent
                -   This will help in checking knowledge articles as well as the manager agent that will be helpful for orchestration to other agents
            -   Ticket readiness AI agent
                -   This will help in checking any fields that would be required for incident progression including SLA's, category, sub-category, asisgnment group by looking into historic incidents using group action framework
            -   Network correlation monitor AI Agent
                -   AI Agent capable to identify impacted services and customer accounts, and create Service Problem Major Case.
            -   Network ticket actionable steps generation AI agent
                -   AI Agent to determine next action based on similar incidents and historic data
            -   Network Remediation Generation AI Agent
                -   AI Agent capable to map resolution steps to corresponding task type, and create such tasks
    -   Help remediate bill issues
        -   Billing account information collector AI agent
            -   This AI agent is designed to handle billing inquiries by following a structured approach. It retrieves billing inquiry case details, obtains the billing account details using the account number. The agent is intended for use by ServiceNow agents for getting the billing account number.
        -   Recommended plans AI agent
            -   This AI agent is designed to facilitate the generation and confirmation of service plan recommendations through a structured approach. It first generates a recommended plan, update the work notes, presents it to the user for confirmation, verifies whether an email is associated with the customer account and triggers the email notification agent to send the recommended plan details to the user.
        -   Billing invoice data collector AI agent
            -   Agent responsible for collecting the billing invoice data
    -   Customer Voice Quality Issue Resolution \(A2A\)
        -   Customer interaction context gatherer:
            -   Collects the customer problem and identify the subscriber details
        -   RADCOM ticket handling AI Agent
            -   Based on the subscriber details provide the Voice and data related KPI's
        -   Ticket creation AI agent
            -   Creates service problem cases based on customer voice and data quality issue.

**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

