---
title: Real-time proactive resolution
description: Use metric rules, alerts, and auto-correction scripts to detect and remediate device and application issues within minutes, before users are affected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/digital-end-user-experience-dex/proactive-resolution-real-time.html
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 3
breadcrumb: [Resolve, Digital End-User Experience, IT Service Management]
---

# Real-time proactive resolution

Use metric rules, alerts, and auto-correction scripts to detect and remediate device and application issues within minutes, before users are affected.

DEX collects metric data at configurable intervals \(every 5, 10, or 15 minutes depending on the metric configuration\) and evaluates conditions that indicate a device or application issue. When a threshold is breached, DEX generates events and alerts that trigger remediation actions.

DEX supports two real-time detection and remediation approaches:

-   **Metric-based**: Uses metric rules to evaluate time-series data and generate alerts. Suitable for conditions that can be expressed as a threshold on collected metrics, such as disk usage or crash frequency.
-   **Auto-correction scripts**: Uses check definitions wrapped in policies to detect and correct conditions at a defined frequency. Suitable for common detect-correct scenarios that don't require additional analysis or correlation, and that must work even when the device is offline.

## Alert generation

When a metric rule detects that a device or application metric has breached a threshold, DEX generates events and alerts in the following sequence:

\[Omitted image "dex-alert-generation-flow.svg"\] Alt text: DEX alert generation flow

1.  DEX evaluates metric rules against incoming metric data for each device.
2.  For each device that breaches a threshold, DEX creates one event in the `em_event` table.
3.  DEX generates one alert per device in the `em_alert` table \(device alerts\) or one alert per application and metric rule combination \(application alerts\).
4.  DEX groups device alerts using the alert correlation rule available with the base system, which consolidates all device alerts for the same metric rule combination within a configurable time window. The default window is one hour and is controlled by the system property `sn_dex.alert.correlation_rule.device_period`.
5.  For application alerts, subsequent evaluations for the same application and metric rule update the same `dex_alert_metadata` record with the new event ID and impacted devices. All new events for the same application and metric rule map to the same alert number until the alert is closed.
6.  Impacted users and devices are recorded in the `dex_alert_impacted_users` table. Additional details are recorded in `dex_alert_metadata`.

## Alert remediation

When a resolution is defined in the metric rule, DEX generates an experience issue per impacted user in the `sn_pren_experience_issue` table. Remediation can be silent \(executed automatically without user interaction\) or can engage the end user through a notification.

\[Omitted image "dex-alert-remediation-flow.svg"\] Alt text: DEX alert remediation flow

-   **Remediation action types**
    -   **Remedial action**: Executes a CI action \(command or script on the endpoint\), catalog item, flow, or Virtual Agent \(VA\) topic.
    -   **Create incident**: Opens an incident record in ServiceNow.
    -   **Self-help instructions**: Delivers instructions to the end user.
    -   **URL**: Directs the end user to a resource URL.
-   **Silent execution**

    The remediation action runs automatically on the device without notifying the end user.

-   **Notify and engage**

    DEX sends the end user a notification through a VA push notification, email, or desktop push notification, then requests consent before executing the action. After execution, the user confirms resolution or escalates.

-   **Notify only**

    DEX notifies the end user without prompting for consent or executing an action.

-   **Fallback configuration**

    If the user does not respond or confirms that the issue is not resolved, a fallback action runs. Fallback options include doing nothing, creating an incident, or connecting the user to a live agent.


When all devices are removed from the impacted device list, DEX closes the alert automatically. For device alerts, the experience issue is also closed. For application alerts, the alert closes when no devices remain in the impacted list.

## Auto-correction scripts

Auto-correction scripts use check definitions wrapped in policies to detect and correct issues at a configured frequency. This approach is suitable for common detect-correct scenarios, such as reconnecting a VPN, connecting to Wi-Fi, or restarting a service, that don't require correlation with metric data or other data collected with DEX.

Auto-correction scripts run on the endpoint and work even when the device is not connected to the internet or to the ServiceNow instance.

**Tip:** For guidance on authoring policies and check definitions, see the policy and check definition authoring documentation.

