---
title: Configure access through the responsibility access configuration
description: Streamline how you create and update your responsibility definitions and access configurations by using the declarative responsibility framework in the Customer Service Management \(CSM\) application. This framework enables you to select the level of access for each responsibility by leveraging low-code or no-code capabilities, which reduces the time required for scripting.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring customer access management, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure access through the responsibility access configuration

Streamline how you create and update your responsibility definitions and access configurations by using the declarative responsibility framework in the Customer Service Management \(CSM\) application. This framework enables you to select the level of access for each responsibility by leveraging low-code or no-code capabilities, which reduces the time required for scripting.

## Before you begin

Role required: admin

## About this task

The Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table is used to store the metadata of the responsibility access configuration. This configuration specifies the level of access and the entities that can be accessed by a particular responsibility. For more information about creating a responsibility definition, see [Create a responsibility definition](t_CreateAResponsibilityDefinition.md). The need for domain separation in configuring access records is determined by the domain of the referenced responsibility.

**Note:** Starting with the Yokohama release, creating and updating responsibility definitions and access configurations using the declarative responsibility framework is deactivated.

