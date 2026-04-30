---
title: Predictive Intelligence for defining work order solutions
description: Use your instance records to build solutions to Field Service Management issues.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Predictive Intelligence for Field Service Management, Setting up FSM reports and analytics, Configuring Field Service Management, Field Service Management]
---

# Predictive Intelligence for defining work order solutions

Use your instance records to build solutions to Field Service Management issues.

## Solution definitions

Solution definitions are available as templates on instances where both Predictive Intelligence and Field Service Management are active. For more information about solution definitions and their types, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). You can also create your own solution definition records.

|Solution Definition|Solution Type|Description|
|-------------------|-------------|-----------|
|Similar Work Orders|Similarity|Recommends similar work orders based on the text in the **Short description** field.|
|Similar Knowledge Articles|Similarity|Recommends similar knowledge articles by comparing the text in the **Text**, **Short Description**, and **Description** fields of knowledge articles to the **Short Description** field of the work orders or work order tasks.|
|Similar Part Requirements|Similarity|Recommends similar part requirements for work order tasks based on the text in the short description and other insights gathered from the similar work order tasks.|
|Grouping of Work Orders into Topics|Clustering|Clusters similar work orders into topics based on the text in the**Short description** field.|

