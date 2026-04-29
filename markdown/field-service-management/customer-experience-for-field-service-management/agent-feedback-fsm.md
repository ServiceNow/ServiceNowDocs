---
title: Collecting agent feedback
description: Use Field Technician Feedback to collect feedback of field service agents from the customers by sending a survey link through email and SMS.
locale: en-US
release: australia
product: Customer Experience for Field Service Management
classification: customer-experience-for-field-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer or Consumer Service Portal, Customer self service, Use, Field Service Management]
---

# Collecting agent feedback

Use Field Technician Feedback to collect feedback of field service agents from the customers by sending a survey link through email and SMS.

When agent marks the work order task as complete, the customer receives a survey link through email and SMS to provide feedback. Customers can provide feedback on a field service agent by rating the agent and posting their comments if any.

The system calculates the average rating of an agent and store it in the wm\_agent\_rating table. The Geolocation tracking map displays the calculated rating of an agent to the customers who are tracking the agent.

The Process agent rating, Daily Data Collection job runs every night to refresh the data so that an updated agent rating is calculated and displayed on the Geolocation tracking map for customers.

**Related topics**  


[Configuring Field Service Management Customer Experience](Configuring-cust-exp.md#)

