---
title: HR Integrations
description: Integrate HR Service Delivery with HR management systems to synchronize employee profiles, to-dos, and other data; background check systems to request background checks; e-signature systems to request electronic signatures; and more.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# HR Integrations

Integrate HR Service Delivery with HR management systems to synchronize employee profiles, to-dos, and other data; background check systems to request background checks; e-signature systems to request electronic signatures; and more.

For select systems, preconfigured integrations are available to use. You can also configure your own custom integration with third-party systems that use SOAP or REST services.

**Important:** Workday integration and SuccessFactors integration that were available with the HR Integrations \[com.sn\_hr\_integrations\] plugin have been deprecated. For Workday integration, you can use the [HR Service Delivery Integration with Workday](w-integration.md) application, and for SuccessFactors integration, you can use the [HR Service Delivery Integration with SuccessFactors](hr-service-delivery-integration-success-factors.md) application.

## Preconfigured integrations

HR Service Delivery provides preconfigured integrations for the following third-party systems.

<table id="table_axf_rkq_ldb"><thead><tr><th>

Third-party system

</th><th>

Preconfigured integration

</th></tr></thead><tbody><tr><td>

Background check system

</td><td>

-   [Integrate with First Advantage service](hr-integrations-with-first-advantage.md)
-   [Integrating with the Accurate Background service](integrate-with-accurate-service.md)
-   [Integrating with the Sterling Talent Solutions service](integrate-with-sterling-service.md)

</td></tr><tr><td>

E-signature system

</td><td>

-   [Integrating with the DocuSign service](docusign-integration-for-hr.md)
-   [Integrating with the Adobe Sign service](integrating-with-adobe-sign-service.md)

</td></tr><tr><td>

Tax form management system

</td><td>

[Integrating with the CIC Plus service](integrating-with-cic-plus-service.md)

</td></tr></tbody>
</table>## Support and troubleshooting information

For information on HR Integrations support and troubleshooting, see the [HR Integrations FAQs \[KB0678031\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0678031) article in the HI Knowledge Base.

**Note:** There are scenarios that are not supported in the initial integration, specifically when an employee is rehired or when an employee moves from contingent to full time.

## Activation information

HR Integrations is automatically activated when you activate Case and Knowledge Management. If it is not activated, you can manually activate HR Integrations. For information on what components are installed with the application, see [Components installed with HR Integrations](../reference/components-installed-with-hr-integrations.md).

-   **[Activate HR Integrations](../task/activate-hr-integrations.md)**  
You can activate Human Resources Scoped App: Integrations \[com.sn\_hr\_integrations\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
-   **[Integrate with First Advantage service](hr-integrations-with-first-advantage.md)**  
The preconfigured First Advantage integration uses SOAP services to request background checks through the First Advantage service. You can use the preconfigured integration as-is or customize it to meet your needs.
-   **[Integrating with the Accurate Background service](integrate-with-accurate-service.md)**  
The preconfigured Accurate Background integration uses REST services to request background checks through the Accurate Background service. You can use the preconfigured integration as-is or customize it to meet your needs.
-   **[Integrating with the Sterling Talent Solutions service](integrate-with-sterling-service.md)**  
The preconfigured Sterling Talent Solutions integration uses REST services to request background checks through the Sterling service. You can use the preconfigured integration as-is or customize it to meet your needs.
-   **[Integrating with the DocuSign service](docusign-integration-for-hr.md)**  
Request electronic signatures through the DocuSign service with the DocuSign integration.
-   **[Integrating with the Adobe Sign service](integrating-with-adobe-sign-service.md)**  
Request electronic signatures through the Adobe Sign service with the Adobe Sign integration. This integration depends on the Adobe Sign spoke in IntegrationHub, and is enabled for the signing of adhoc documents \(HR PDF document templates\) and Adobe Sign templates.
-   **[Integrating with the CIC Plus service](integrating-with-cic-plus-service.md)**  
Integrate with the CIC Plus service so that you can enable US-based new hires to provide relevant tax information as part of the onboarding process.

**Parent Topic:**[Integration of HR Service Delivery with third-party systems](integrate-third-party-systems.md)

