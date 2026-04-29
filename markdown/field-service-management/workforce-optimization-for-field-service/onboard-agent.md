---
title: Onboard an external agent
description: Onboard an agent for contractor company to assign the work order tasks.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contractor Management, Contractor capabilities, Set up workforce, Configure, Field Service Management]
---

# Onboard an external agent

Onboard an agent for contractor company to assign the work order tasks.

## Before you begin

Role required: wm\_admin, wm\_contractor\_manager\_int

## About this task

Internal manager of the company can onboard field service agents for the third-party contractor companies. These onboarded agents are known as external agents and responsible for performing the assigned work order tasks at the customer location.

You can also do the initial configuration of onboarding an external manager through **Field Service** &gt; **Administration** &gt; **Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **Outsourced Field Service** &gt; **Outsourced Service Providers**.

2.  Click a contractor company from the list for which you want to on board a field service agent.

3.  Click **Onboard Agent**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |First name|Agent’s first name.|
    |Last name|Agent’s last name|
    |Active|Option for making this agent the selected external agent.|
    |Email|Agent's official email address.|
    |Time zone|Time zone for this agent’s location.|
    |Business phone|Agent's business phone number.|
    |Mobile phone|Agent's mobile phone number.|
    |Photo|Photograph of the agent.|
    |Date format|String format as specified in the field.|
    |Geolocation tracked|Option to enable tracking the real-time location of agent.|

5.  Click **Submit**.


## Result

The system sends an email to the newly onboarded agent that includes a URL to reset the password while logging to Field Service Contractor Portal for the first time.

