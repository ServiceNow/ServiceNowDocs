---
title: Explore Source-to-Pay integration with SAP
description: Learn more about the Source-to-Pay integration with SAP.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Explore Source-to-Pay integration with SAP

Learn more about the Source-to-Pay integration with SAP.

## Establishing communication between the SAP and ServiceNow instances

The Source-to-Pay integration with SAP supports the following APIs:

-   REST APIs: REST relies on a client/server approach that separates front and back ends of the API and provides considerable flexibility in development and implementation. REST is stateless, which means the API stores no data or status between requests.
-   SOAP APIs: The simple object access protocol \(SOAP\) is a messaging standard defined by the World Wide Web Consortium and broadly used to create web APIs, usually with XML. SOAP supports a wide range of communication protocols found across the internet, such as HTTP, SMTP and TCP/IP.

You can establish a connection with an SAP system from the ServiceNow instance using the following methods:

-   **SAP Java Connector** \(SAP JCo\): It is a middleware that allows Java applications to communicate with SAP systems using RFC/BAPI protocols. It supports both inbound and outbound Remote Function Calls. For more information, see SAP Documentation.
-   **OData** \(Open Data Protocol\): It is used in web technologies by SAP to make data accessible across different platforms, enabling the development of web applications, websites, and mobile apps.

SAP supports the following protocols for transferring data:

-   RFC/BAPI \(sync typically\)
-   REST/OData \(sync\)
-   SOAP \(async typically\)

## SAP Implementations

-   On-premises implementation:

    Everything is managed and maintained by the customer in their physical locations. Both SAP ECC and SAP S4 HANA can be implemented in this model.

-   On-premises implementation on Azure or AWS:

    The SAP instance could be on a cloud instance like Azure or AWS, but it’s still a type on-premises implementation as it is within a firewall, with the only difference being that the instance is hosted on a cloud server. Both SAP ECC and SAP S4 HANA can be implemented in this model.

-   Cloud implementation:

    The SAP instance is on a true cloud system. Only SAP S4 HANA can be implemented in this model, and SAP ECC can’t be implemented in this category.


The current default SAP integration workflows offered by ServiceNow cater to the implementation of the first two types. However, it doesn’t exclude customers from implementing on cloud, which can easily be achieved by converting the wrapper function modules into web service WSDLs. However, this requires customizations at SAP and ServiceNow.

