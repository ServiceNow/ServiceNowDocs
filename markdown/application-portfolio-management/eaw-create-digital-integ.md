---
title: Add or edit a digital integration in the EA Workspace
description: Add a digital integration or edit an existing digital integration in the EA Workspace. The digital integration is a design object used by the Enterprise Architects. It describes a connection between two business applications or between a business application and an external service \(for example: AWS, Yahoo, a TimeZone Conversion service\) that provides an interface \(API\) to interact with.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with digital integrations, Working with digital integration management in Enterprise Architecture Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add or edit a digital integration in the EA Workspace

Add a digital integration or edit an existing digital integration in the EA Workspace. The digital integration is a design object used by the Enterprise Architects. It describes a connection between two business applications or between a business application and an external service \(for example: AWS, Yahoo, a TimeZone Conversion service\) that provides an interface \(API\) to interact with.

## About this task

The digital integration form helps you define why a connection is required between two data entities. You can define the interface where they should communicate. You can provide a link to relevant designs and architectural material in the description. A Digital Integration underpins a business capability and provides business value.

## Before you begin

Role required: sn\_apm.apm\_analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon \(![portfolio icon.](../../image/portfolio-icon.png)\).

3.  Select the expand row icon \(![expand row icon.](../../image/ExpandIcon.png)\) next to **Application Portfolio**.

4.  Select **Digital Integrations**.

5.  Add or edit a digital integration.

    -   To add a digital integration, select **New** or **New \(Easy form\)**.
    -   To update an existing digital integration, select the digital integration, select **Edit**.
6.  On the **Digital Integration** form, fill in the fields.

    For a description of the field values, see [Digital integration form \(easy form\) in EA Workspace](../../reference/eaw-reference/eaw-digital-integ-form.md) or [Digital integration form in EA Workspace](../../reference/eaw-reference/eaw-update-digital-integration-form.md).

7.  Select **Add** or **Update**.


## Result

After submission of the form, within the CMDB platform, a CI relationship \(Interfaces::Interfaced By\) gets created between provider and subscriber business applications. In the case where the digital interface has no relation to a business application \(using Open or Public API\), the digital integration is created between the subscriber business application and a standalone digital interface.

**Parent Topic:**[Working with digital integrations](../../concept/eaw-concept/eaw-work-with-digital-integrations.md)

**Related topics**  


[Manage architectural artifacts of a digital integration in EA Workspace](eaw-assoicate-artifact-dig-intgn.md)

[Associate an information object to a digital integration](eaw-dig-integ-add-info-object.md)

[View all digital integrations](eaw-view-all-dig-integ.md)

