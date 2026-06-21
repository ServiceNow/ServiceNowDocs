---
title: Add or edit a digital integration in the EA Workspace
description: Add a digital integration or edit an existing digital integration in the EA Workspace. The digital integration is a design object used by the Enterprise Architects. It describes a connection between two business applications or between a business application and an external service \(for example: AWS, Yahoo, a TimeZone Conversion service\) that provides an interface \(API\) to interact with.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/enterprise-architecture/eaw-create-digital-integ.html
release: yokohama
product: Enterprise Architecture
classification: enterprise-architecture
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Digital integrations in Enterprise Architecture Workspace, Working with an application portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add or edit a digital integration in the EA Workspace

Add a digital integration or edit an existing digital integration in the EA Workspace. The digital integration is a design object used by the Enterprise Architects. It describes a connection between two business applications or between a business application and an external service \(for example: AWS, Yahoo, a TimeZone Conversion service\) that provides an interface \(API\) to interact with.

## About this task

The digital integration form helps you define why a connection is required between two data entities. You can define the interface where they should communicate. You can provide a link to relevant designs and architectural material in the description. A Digital Integration underpins a business capability and provides business value.

## Before you begin

Role required: sn\_apm.apm\_analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon \(\[Omitted image "portfolio-icon.png"\] Alt text: portfolio icon.\).

3.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: expand row icon.\) next to **Application Portfolio**.

4.  Select **Digital Integrations**.

5.  Add or edit a digital integration.

    -   To add a digital integration, select **New** or **New \(Easy form\)**.
    -   To update an existing digital integration, select the digital integration, select **Edit**.
6.  On the **Digital Integration** form, fill in the fields.

    For a description of the field values, see [Digital integration form \(easy form\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/enterprise-architecture/eaw-digital-integ-form.md) or [Digital integration form in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/enterprise-architecture/eaw-update-digital-integration-form.md).

7.  Select **Add** or **Update**.


## Result

After submission of the form, within the CMDB platform, a CI relationship \(Interfaces::Interfaced By\) gets created between provider and subscriber business applications. In the case where the digital interface has no relation to a business application \(using Open or Public API\), the digital integration is created between the subscriber business application and a standalone digital interface.

**Parent Topic:**[Digital integrations in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/enterprise-architecture/eaw-digital-integration.md)

