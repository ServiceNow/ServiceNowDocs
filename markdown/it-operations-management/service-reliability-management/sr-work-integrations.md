---
title: Working with integrations in SRM
description: Connect your services to monitoring tools using the Integrations Launchpad . Integrations send information to Service Reliability Management \(SRM\), helping you track alerts, manage incidents, and maintain service health.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-reliability-management/sr-work-integrations.html
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with SRM services, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Working with integrations in SRM

Connect your services to monitoring tools using the Integrations Launchpad . Integrations send information to Service Reliability Management \(SRM\), helping you track alerts, manage incidents, and maintain service health.

## Access the Integrations Launchpad

As an SRM admin, manager, or responder, you can access the Integrations Launchpad in the following ways:

-   From the primary navigation, select the ITOM Admin Experience icon, and then select either **Add integration** or **Manage installed integrations**.
-   From the Services page \(\[Omitted image "icon-sr-services.png"\] Alt text: Services page icon\), select a service, select the **Integrations** tab, and then select **Add an integration**.
-   From the Services page \(\[Omitted image "icon-sr-services.png"\] Alt text: Services page icon\), select a service, expand **Complete setup**, and then select **Add integrations**.

## Integration details specific to SRM

Be aware of the following when using the Integrations Launchpad for SRM:

-   **Connector type support**

    SRM supports custom, pull, and push connectors. Pull connectors retrieve data from external sources, and push connectors send data from external sources to your instance.

    **Note:** For information about setting up connectors, see [Integrations Launchpad in Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/integrations-launchpad.md).

-   **Configuration item field**

    When you set up an integration for SRM, the Provide details step has an additional field called Default configuration item.

    Set this field to the service your integration monitors. If an incoming alert doesn't include service details, SRM uses this field to connect the alert to the relevant service. This field helps make sure that your teams receive alerts for the services they support.

    \[Omitted image "srm-ci-integration.png"\] Alt text: Box highlights the Default configuration item field in the Provide details step.


## Learn more

Visit the following links to set up and manage integrations with the Integrations Launchpad. The pages are in a different section because the Integrations Launchpad is part of the broader Service Operations Workspace.

-   [Activate integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/activate-integration.md)
-   [Configure an event custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/custom-connector.md)
-   [Configure an event pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/pull-connector.md)
-   [Configure an event push connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/push-connector.md)
-   [Deactivate integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/deactivate-integration.md)
-   [Delete integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/delete-integration.md)

**Parent Topic:**[Working with SRM services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-reliability-management/sr-work-services.md)

