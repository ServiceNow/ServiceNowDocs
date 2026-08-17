---
title: Configure ServiceNow Otto for Virtual Agent for Conversational AI Health and Safety incident report
description: An admin can configure the default ServiceNow Otto for Virtual Agent assistants and the default ServiceNow Otto panel assistants \(Platform\). Configuring the assistants enables the ServiceNow Otto panel on the Employee Center and the Health and Safety workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-health-and-safety/now-assist-configure-virtual-agent-conversational-incident.html
release: australia
product: Now Assist for Health and Safety
classification: now-assist-for-health-and-safety
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure conversational AI, Configure, ServiceNow Otto for Health and Safety, Health and Safety, Employee Service Management]
---

# Configure ServiceNow Otto for Virtual Agent for Conversational AI Health and Safety incident report

An admin can configure the default ServiceNow Otto for Virtual Agent assistants and the default ServiceNow Otto panel assistants \(Platform\). Configuring the assistants enables the ServiceNow Otto panel on the **Employee Center** and the Health and Safety workspace.

## Before you begin

Role required: admin

## About this task

1.  Enable AI Search to provide consumer-grade search experiences for your users.

    For more information, see [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configuring-ais.md).

2.  Install the ServiceNow Otto for platform \[sn\_genai\_platform\] to enable ServiceNow Otto for the workspace.
3.  Install the Health and Safety Incident Management \[sn\_hs\_im\_incident\] plugin.

    For more information, see [Install Health and Safety Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-incident-management/install-hs-incident-mgmt.md)

4.  For detailed information about configuring ServiceNow Otto for Virtual Agent, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

## Procedure

1.  To turn on the ServiceNow Otto panel, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

    The **CI Admin console** opens the **Assistants** page that shows the two assistants.

    -   Now Assist in Virtual Agent \(default\)
    -   ServiceNow Otto panel assistants \(Platform\)
2.  Select the **More options** icon \(\[Omitted image "wsd-more-options-icon-loc-directory.png"\] Alt text: more options\) for **ServiceNow Otto for Virtual Agent \(default\)**

3.  Select **Turn on/off**, to turn on the assistant.

    Select **Setup** in the pop-up dialogue.

4.  Select **Save and continue** on the **Overview** tab.

5.  On the **AI skills** tab, select the check box for **Custom skills** under the **Skill name** column.

6.  Select **Save and continue**

7.  For **Display experience** select, **Add portal** drop-down in the **Portal tab** and then select **Employee Center**.

8.  Select **Save and continue**

9.  Select **Save and continue** for the **Information sources** and **Branding** tab.

10. On the **Chat experiences** tab, select the check box for **Document uploads** and then select **Save and continue**.

11. Review the assistant and select **Done**.

    The Now Assist in Virtual Agent assistant shows the status as on.


## Result

The ServiceNow Otto panel is enabled for the Employee center.

**Parent Topic:**[Configure conversational AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-health-and-safety/hs-configure-conversational-ai.md)

