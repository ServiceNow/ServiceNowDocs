---
title: Exploring Financial Services Operations Integration with Guidewire
description: With the Financial Services Operations Integration with Guidewire application, insurers can embed the Guidewire Cloud based APIs in the FSO workflows to handle the day to day business operations for policy services, claims services, and billing services.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Guidewire, Integrate, Financial Services Operations \(FSO\)]
---

# Exploring Financial Services Operations Integration with Guidewire

With the Financial Services Operations Integration with Guidewire application, insurers can embed the Guidewire Cloud based APIs in the FSO workflows to handle the day to day business operations for policy services, claims services, and billing services.

## Layers in the Guidewire integration

The following table describes the different layers in the Guidewire integration.

<table id="id_kvf_s4q_jzb"><thead><tr><th>

Layer

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Industry Workflow/FSO Layer

</td><td>

Layer that includes the Financial Services Operations application.

</td></tr><tr><td>

Integration Layer

</td><td>

Layer that helps to integrate with the Financial Services Operations application and stores information to the data model. This layer provides the following components:-   End-to-end integration of the FSO layer and spoke layer.
-   Subflows that consume the actions in the Guidewire spoke. Each action has both individual subflows and combined subflows to call all the actions together. The combined subflows are as follows:
    -   Get Personal Auto Claim
    -   Get Commercial Auto Claim

</td></tr><tr><td>

Spoke Layer

</td><td>

Layer that includes the Guidewire spoke plugin. This layer provides the actions that use REST Web Services to interact with the Guidewire APIs. To view Guidewire spoke actions, see [Guidewire Spoke](https://www.servicenow.com/docs/access?context=guidewire-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) actions.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations Integration with Guidewire](fso-integration-with-guidewire-landing-page.md)

