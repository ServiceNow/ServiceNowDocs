---
title: Customer Data Foundation
description: Models who a customer is, how they relate to the organization that serves them, and what each person can access across Customer Service Management \(CSM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-data-foundation.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Data models, Set up your environment, Configure, Customer Service Management]
---

# Customer Data Foundation

Models who a customer is, how they relate to the organization that serves them, and what each person can access across Customer Service Management \(CSM\).

## Overview of Customer Data Foundation

Customer Data Foundation is the framework that CSM uses to model the customer. It defines who a customer is, how they relate to the organization that serves them, and what each person can see and do. The framework has four layers:

-   the company that provides products and services
-   the customer organizations it serves
-   the individual people who consume those products and services
-   the access controls that govern access

The same foundation supports the following business models: business-to-business \(B2B\), business-to-consumer \(B2C\), and business-to-business-to-consumer \(B2B2C\). Because the foundation is shared across the customer service portfolio, a record created in one product is immediately available in another, without duplication.

## Provider and customer model

\[Omitted image "refarch-data-models-customers.png"\] Alt text: Flowchart showing relationships between provider company, employees, fulfillers, and three customer types: B2B accounts, B2C consumers, and B2B2C accounts with consumers.

The company builds the products and services and serves customers through its employees. Some employees are fulfillers who handle customer interactions directly. This relationship is the Customer-Employee relationship shown at the top of the model.

## Customer Data Foundation layers

Customer Data Foundation is organized into four layers. Each layer has a distinct purpose, and the entities in each layer connect to the layers preceding and succeeding.

<table id="table_tst_ymx_zjc"><thead><tr><th>

Layer

</th><th>

What it covers

</th><th>

Key entities

</th></tr></thead><tbody><tr><td>

Company

</td><td>

The organization that builds products and services for the end customers, and the employees who serve them.

</td><td>

-   Company
-   Employee
-   Fulfiller

</td></tr><tr><td>

Customer organizations

</td><td>

External end-customers who pay for or are entitled to the goods and services.

</td><td>

-   Account
-   Partner account
-   Consumer
-   Household

</td></tr><tr><td>

Customer people

</td><td>

People who directly or indirectly consume the product, or who represent the business consuming the service.

</td><td>

-   Contact
-   Partner contact
-   Account consumer
-   Consumer profile
-   Member

</td></tr><tr><td>

Access requirements

</td><td>

The access that end users hold, expressed as the roles they act in.

</td><td>

-   Requester
-   Contact admin
-   Authorized representative
-   Head of household

</td></tr></tbody>
</table>## Business models supported

Customer Data Foundation supports the following business models: B2B, B2C, and B2B2C. Each model uses the same underlying entities in a different combination. It also supports, business-to-business-to-employee model \(B2B2E\) variant that extends the B2B model.

<table id="table_fyk_t5w_zjc"><thead><tr><th>

Business model

</th><th>

Entities

</th><th>

Typical scenario

</th></tr></thead><tbody><tr><td>

B2B

</td><td>

-   Account
-   Contact

</td><td>

A software company sells to another business, and the buyer's employees are its contacts.

</td></tr><tr><td>

B2C

</td><td>

-   Consumer
-   Household member

</td><td>

A telecommunications provider serves individual subscribers or households.

</td></tr><tr><td>

B2B2C

</td><td>

-   Account
-   Consumer \(via account consumer\)

</td><td>

An insurance carrier covers policyholders through a broker, or a healthcare payer covers patients through providers.

</td></tr><tr><td>

B2B2E

</td><td>

Reuses the B2B model \(account and contact\)

</td><td>

An HR service company delivers services to the employees of an enterprise customer.

</td></tr></tbody>
</table>**Related topics**  


[Data management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-data-management.md)

[User management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/user-management.md)

[Service Model Foundation overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-industry-data-model.md)

