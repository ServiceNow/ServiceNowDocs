---
title: Understand why an SLA did not trigger as expected
description: Describes the conditions when an SLA might not trigger as expected.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SLA timeline, Service Level Management reference, Service Level Management, IT Service Management]
---

# Understand why an SLA did not trigger as expected

Describes the conditions when an SLA might not trigger as expected.

Using Task SLA -1 \(highlighted in the screenshot\) as an example, an SLA Manager may have expected this SLA to trigger earlier.

![SLA Timeline](../image/why-sla-did-not-trigger-1.png)

To troubleshoot this inconcistency, the SLA Manager can enable **Show all task updates** from the settings menu in the upper right of the SLA Timeline. The SLA timeline displays task updates that do not cause an SLA stage change as a white triangle.

![Show all task updates toggle button](../image/why-sla-did-not-trigger-2.png)

If you click the first or second task updates that did not cause a stage change, the details section displays the SLA start conditions and the task values that are key to trigger the start condition. In this case, the Configuration Item field is not populated and the SLA Definition conditions are defined to trigger when the Configuration Item is defined as the CI SAN 001.

![SLA Definition Conditions](../image/why-sla-did-not-trigger-3.png)

On inspecting the details for the task update that triggered the SLA start condition, you can find that the configuration item is set to Storage Area Network 001 and this matches the SLA Definition start condition.

**Show all task updates** is a powerful tool to help SLA Managers understand why an SLA may not have behaved as expected.

![SLA conditions that caused stage change](../image/why-sla-did-not-trigger-4.png)

**Parent Topic:**[SLA timeline](c_SLATimeline.md)

