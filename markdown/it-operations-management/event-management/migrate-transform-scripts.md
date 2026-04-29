---
title: Use legacy listener transform scripts
description: Use legacy listener transform scripts when upgrading a ServiceNow AI Platform instance from Paris or earlier. These scripts can be run as part of existing integrated systems, or in unison with Event Management push connectors.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Use legacy listener transform scripts

Use legacy listener transform scripts when upgrading a ServiceNow AI Platform instance from Paris or earlier. These scripts can be run as part of existing integrated systems, or in unison with Event Management push connectors.

You can use listener transform scripts to ensure that previous integrations are supported. For example, if you are using the `https:/<instance-name>.service-now.com/api/global/em/inbound_event` endpoint in various existing integrations, you can continue to use this endpoint in a Quebec or later ServiceNow AI Platform instance.

If you want to use the Event Management push connectors, download the plugin from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website. You can then access the push connectors in the ServiceNow AI Platform instance, and the `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event` endpoint is also created.

## Use the legacy endpoint with push connectors

You can continue to use the `https:/<instance-name>.service-now.com/api/global/em/inbound_event` endpoint with the push connectors, by deactivating the relevant transform scripts. To deactivate a script, navigate to **Event Management** &gt; **Integrations** &gt; **Listener Transform Scripts**. Then click the relevant script in the displayed list, and clear the **Active** check box in the form.

## Use the legacy endpoint and deactivate all listener transform scripts

You can also continue to use the `https:/<instance-name>.service-now.com/api/global/em/inbound_event` endpoint but deactivate all listener transform scripts to use the push connectors instead. To deactivate all scripts, navigate to **System Properties** &gt; **All Properties**, locate the **sn\_em\_connector\_listener\_table\_for\_InboundEvent** property, and set its value to **True**.

## Migrate custom listener transform scripts to the push connectors module

If you have created custom listener transform scripts, they must be migrated to the push connectors module if you want to use the new `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event` endpoint. To migrate the custom script, navigate to **Event Management** &gt; **Integrations** &gt; **Listener Transform Scripts**, click the relevant listener transform script, and select the displayed script. Then navigate to **Integrations** &gt; **Push Connectors**, click **New**, and paste in the script you copied from the listener transform script.

**Parent Topic:**[Integrate with push connectors](../task/configure-listener-transform-script.md)

