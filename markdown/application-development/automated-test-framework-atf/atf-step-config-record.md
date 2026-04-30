---
title: Automated Test Framework Step Config record
description: The step config record controls how a test step of this type behaves.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Step configurations, Administration, Reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework Step Config record

The step config record controls how a test step of this type behaves.

<table><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name for this test step configuration.

</td></tr><tr><td>

Active

</td><td>

**True** if this step configuration is active. Otherwise, **false**.

</td></tr><tr><td>

Step Environment

</td><td>

The [step environment](../concept/step-environments-module.md) in which a step with this configuration can run.

</td></tr><tr><td>

Category

</td><td>

The [category](../concept/step-configuration-categories-module.md) assigned to a step with this configuration.

</td></tr><tr><td>

Application

</td><td>

The application scope in which the system runs steps with this configuration.

</td></tr><tr><td>

Batch order constraint

</td><td>

Constrains where a step with this configuration can appear in a test:-   **None**: A step based on this configuration can appear at any point in a test.
-   **Start Batch Execution**: If a test includes this a step based on this configuration, it must be the first step in the test.
-   **Run in the middle of an execution**: If a test includes a step based on this configuration, it cannot be the first or last step.
-   **Stop Execution**: If a test includes a step based on this configuration, it must be the last step in the test.

</td></tr><tr><td>

Class type

</td><td>

For custom step configurations, this field is always **Script**.

</td></tr><tr><td>

Order

</td><td>

An integer specifying where steps with this configuration appear in the step list on the Add Test Step dialog. For more information, see the [example using the Order field](atf-step-config-xmpls.md#iss_1jv_xw).

</td></tr><tr><td>

Template reminder

</td><td>

The instructions that appear when a step with this configuration is included in a test as part of a template. For more information, see the[example of using the Template reminder field.](atf-step-config-xmpls.md#qzw_phv_xw)

</td></tr><tr><td>

HTML description

</td><td>

The text that appears when the cursor highlights a step with this configuration on the Create New Step dialog. For more information, see the [example using the HTML description field.](atf-step-config-xmpls.md#qtf_33v_xw)

</td></tr><tr><td>

Description generation script

</td><td>

Generates the text that describes a step when a test includes it. For more information, see the [example using the description generation script](atf-step-config-xmpls.md#b5m_zrx_yw).

</td></tr><tr><td>

Step execution script

</td><td>

Script \(javascript\) that runs when a step with this config runs.

</td></tr><tr><td>

Input Variables related list

</td><td>

The variables that act as inputs for a step with this config.

</td></tr><tr><td>

Output variables related list

</td><td>

The variables that act as outputs for a step with this config.

</td></tr></tbody>
</table>**Parent Topic:**[Step configurations](../concept/step-configurations-module.md)

