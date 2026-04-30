---
title: Idea Portal navigation
description: Configure the Idea Portal URL to enable access to the Idea Portal from the application navigator.
locale: en-US
release: xanadu
product: Innovation Management
classification: innovation-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Idea Portal administration, Manage Idea Portal, Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Idea Portal navigation

Configure the Idea Portal URL to enable access to the Idea Portal from the application navigator.

## Before you begin

Role required: idea\_admin

## About this task

Enable access to the Idea Portal module using the Application Menus module.

## Procedure

1.  Open the **Ideas** application menu record and add the Idea Portal to the navigation menu.

    For information about how to add Idea Portal to the navigation menu, see [Create a module](https://www.servicenow.com/docs/access?context=test-steps-app-navigator-category&version=xanadu&pubname=xanadu-application-development&section=t_CreateAModule&ft:locale=en-US).

2.  In the Module form, set the value of the **Link type** field as **URL \(from arguments\)**.

    Use the Module Id as a parameter in the URL to specify the Idea module that you want to associate with the Idea Portal.

    For example, if you created an Idea module for your HR department and used **hr** as the **Module Id**, the URL to access the Idea Portal would be as follows: `/idea/?id=ideas_list&sysparm_module_id=hr`.


**Parent Topic:**[Idea Portal administration](../concept/idea-portal-administration.md)

**Previous topic:**[Idea Portal administration](../concept/idea-portal-administration.md)

**Next topic:**[Create an Idea module](create-idea-module.md)

