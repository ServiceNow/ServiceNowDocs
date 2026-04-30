---
title: Components installed with Customer Service Problem Management
description: Several types of components are installed with activation of the Customer Service Problem Management application, including tables, user roles, and business rules.
locale: en-US
release: yokohama
product: Customer Service Problem Management
classification: customer-service-problem-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Customer Service Problem Management reference, Customer Service Problem Management]
---

# Components installed with Customer Service Problem Management

Several types of components are installed with activation of the Customer Service Problem Management application, including tables, user roles, and business rules.

## Roles

Customer Service Problem Management adds the following roles:

<table id="table_gj4_5qk_sbc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test Definition Manager\[sn\_st\_mgmt.test\_def\_manager\]

</td><td>

Enables you to set up, create, and update service test definitions and all their related child entities. Additionally, this role includes the ability to view the product catalog.

</td></tr><tr><td>

Test Definition Viewer\[sn\_st\_mgmt.test\_def\_viewer\]

</td><td>

Enables you to read the service test definition and all its related child entities.

</td></tr><tr><td>

Test Definition Writer\[sn\_st\_mgmt.test\_def\_writer\]

</td><td>

Enables you to write the service test definition and all its related child entities. Additionally, this role includes the test definition viewer role.

</td></tr><tr><td>

Test Definition Creator\[sn\_st\_mgmt.test\_def\_creator\]

</td><td>

Enables you to create the service test definition and all its related child entities. Additionally, this role includes the test definition viewer role.

</td></tr><tr><td>

Test Definition Delete\[sn\_st\_mgmt.test\_def\_delete\]

</td><td>

Enables you to delete the service test definition and all its related child entities.

</td></tr><tr><td>

Test Run Manager\[sn\_st\_mgmt.test\_manager\]

</td><td>

Enables you to trigger or update Service test results and all its related child entities. Additionally, this role includes the product inventory viewer role.

</td></tr><tr><td>

Test Run Viewer\[sn\_st\_mgmt.test\_viewer\]

</td><td>

Enables you to read the service test and all its related child entities.

</td></tr><tr><td>

Test Run Writer\[sn\_st\_mgmt.test\_writer\]

</td><td>

Enables you to write the service test and all its related child entities. Additionally, this role includes the test viewer role.

</td></tr><tr><td>

Test Run Creator\[sn\_st\_mgmt.test\_creator\]

</td><td>

Enables you to create the service test and all its related child entities. Additionally, this role includes the test viewer role.

</td></tr><tr><td>

Test Run Delete\[sn\_st\_mgmt.test\_delete\]

</td><td>

Enables you to delete the service test and all its related child entities.

</td></tr><tr><td>

Test Integrator\[sn\_sprb\_mgmt.test\_integrator\]

</td><td>

Enables you to create and update the service test definitions, service tests, and all their related child entities.

</td></tr><tr><td>

Service Problem Case Navigator\[sn\_sprb\_mgmt.navigation\_menu\]

</td><td>

Enables you to navigate through the service problem cases.

</td></tr><tr><td>

Service Problem Case Agent\[sn\_sprb\_mgmt.agent\]

</td><td>

Enables you to create, read, and write the service problem cases. Additionally, this role includes the ability to run the test runs and view the diagnostic test results.

</td></tr><tr><td>

Service Problem Case Customer\[sn\_sprb\_mgmt.customer\]

</td><td>

Enables you to create, read, and write the service problem cases in the customer service portal. Additionally, this role includes the ability to view the inventory.

</td></tr><tr><td>

Service Problem Case Admin\[sn\_sprb\_mgmt.admin\]

</td><td>

Enables you to create, read, and write the service problem case, the test runs, and the test definitions. Additionally, this role includes the ability to view the diagnostic test results and resolution task.

</td></tr></tbody>
</table>## Tables

Customer Service Problem Management adds the following tables.

<table id="table_jzy_5k2_jbc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Test Definition

</td><td>

Description of the service test in terms of parameters to be configured and measures to be taken.Test definitions are configurations that are required to run a particular test against the service being impacted.

</td></tr><tr><td>

Test Definition Characteristics

</td><td>

Properties or attributes that are needed to be configured or placed before running the test.

</td></tr><tr><td>

Test Measure Definition

</td><td>

Definition a measure of a specific aspect of a product, service, or resource test, such as lost packets or connectivity status.

</td></tr><tr><td>

Threshold Rule

</td><td>

Rule that defines the condition \(raise or clear\) to achieve to apply consequences when a threshold is crossed or ceased to be crossed.

</td></tr><tr><td>

Measure Consequences

</td><td>

Action to take when a Threshold Rule is crossed. The action can be a prescribed action or notification.

</td></tr><tr><td>

Test Definition Relationship

</td><td>

Test definitions hierarchy. The relationship can be a substitution, dependency, or exclusivity relationship between test specifications.

</td></tr><tr><td>

Specification to Test Definition Relationship.

</td><td>

Test Definition relationship with Specification \(Product / Service / Resource\) or product Model.

</td></tr><tr><td>

Test Run

</td><td>

Test run with actual test measure values and rule violations.

</td></tr><tr><td>

Test Characteristic

</td><td>

Description of a characteristic of Service Test through a name-value pair.

</td></tr><tr><td>

Test Measure

</td><td>

Measure of a specific aspect of a product, service, or resource test, such as lost packets or connectivity status.

</td></tr><tr><td>

Threshold Rule Violation

</td><td>

Violation of a rule that defines the Threshold Rule Definition.

</td></tr><tr><td>

Applied Consequence

</td><td>

The action to take when a Threshold Rule Violation occurs. The action can be a prescribed action or notification.

</td></tr><tr><td>

Diagnostic Task

</td><td>

Task extension. Task for an agent to trigger tests on services.

</td></tr><tr><td>

Resolution Task

</td><td>

Task extension. Task for an agent for repair and resolution based on test failures.

</td></tr><tr><td>

Service Problem Case

</td><td>

Case extension and a new case type.

</td></tr></tbody>
</table>**Parent Topic:**[Customer Service Problem Management reference](cspm-reference.md)

