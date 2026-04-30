---
title: Connection &amp; Credential configuration templates
description: Enable users with the admin and flow\_designer roles to set up spoke integrations with third-party systems using a single, customizable form.
locale: en-US
release: xanadu
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring credentials, connections, and aliases, Connections and Credentials, Access Management]
---

# Connection &amp; Credential configuration templates

Enable users with the admin and flow\_designer roles to set up spoke integrations with third-party systems using a single, customizable form.

For example, you can set up an OAuth integration, which registers an OAuth provider, generates a token, and creates connection and credential records. An action designer or developer can use a configuration template to set up the spoke in one place and the system creates the associated records.

## Benefits

Configuration templates enable:

-   Admins or flow designers to set up a complex integrations using a single form.
-   Developers to set static values in an integration, simplifying the setup process for admins and flow designers.

## Supported credential types

You can create configuration templates for integrations with these credential types:

-   Basic auth
-   API key
-   OAuth JWT Bearer grant type
-   OAuth Authorization Code grant type
-   Custom authentication

## Configuration template components

-   **Default Data Template**

    Sets static information that applies to every integration. For example, you can set the API and token URL if the value applies to every integration.

-   **Dynamic Data Template**

    Defines the information that the user must complete to set up the integration. For example, you can add user name and password key-value pairs to gather user-defined values.

-   **Post Processing Script**

    Creates additional records required by the integration. For example, if your spoke includes custom tables, you can create records in those tables based on user input in the configuration template. This script executes after the connection and credential records are created.

-   **Pre Edit Script**

    Pre-populates the custom fields in the **Additional Information** section when you edit an existing connection. Pre-populating the custom fields enables you to view the current value associated to the custom field.


## Demo data

The Connection &amp; Credential Templates \[sys\_alias\_templates\] table includes example templates to demonstrate how to set up templates for common authentication types. Use these examples as a guide when creating your own.

-   **[Configure a template for OAuth JWT Bearer grant type](../reference/docusign-example.md)**  
This example configuration template sets up Credential and Connection records using the JWT Bearer grant type to authenticate requests to Docusign.
-   **[Create a configuration template](../task/create-template.md)**  
Create a template that defines the inputs required to set up a spoke. Set static key-value pairs to create records and set values that apply to every integration. Set dynamic key-value pairs to gather user input and set field values that may vary. Using this template, admins and flow designers can set up the spoke from a single form.

**Parent Topic:**[Exploring credentials, connections, and aliases](credentials-connections-alias.md)

