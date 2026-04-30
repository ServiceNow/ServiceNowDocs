---
title: Install multiple applications in a batch
description: The Batch Installation feature helps you install multiple applications, plugins, or application-customizations together, instead of having to install them serially one at a time. You can access this feature either from the Continuous Integration and Continuous Delivery \(CI/CD\) APIs via three new endpoints, or via the CI/CD Spoke on Integration Hub using Workflow Studio subflows and actions.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Install multiple applications in a batch

The Batch Installation feature helps you install multiple applications, plugins, or application-customizations together, instead of having to install them serially one at a time. You can access this feature either from the Continuous Integration and Continuous Delivery \(CI/CD\) APIs via three new endpoints, or via the CI/CD Spoke on Integration Hub using Workflow Studio subflows and actions.

## Overview

When managing many types of applications, it can be a challenge to have separate pipelines for each application and to wait for them to serially deploy to the same environment. With the Batch Installation feature, you can install several applications together by bundling them into a single JSON manifest file. These applications include scoped or global applications, plugins, and application-customizations.

A batch can contain any combination of the following types:

-   A ServiceNow plugin
-   Application: Scoped applications in the ServiceNow Store that your company doesn't own, scoped or global applications in the Application Repository owned by your company, and your application-customizations for Store applications stored in the Application Repository.

## Batch installation methods

For details on installing applications in a batch via the REST API see [Continuous Integration/Continuous Delivery \(CI/CD\) API](https://www.servicenow.com/docs/access?context=cicd-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

For details on installing applications in a batch with the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) application, see [Continuous Integration and Continuous Delivery \(CICD\) spoke](https://www.servicenow.com/docs/access?context=cicd-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

**Parent Topic:**[Using Legacy Application Manager](../../../build/applications/task/using-legacy-application-manager.md)

