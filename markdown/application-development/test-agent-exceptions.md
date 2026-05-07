---
title: Test Agent guidelines
description: Leverage the full potential of Test Agent by following these guidelines.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-22"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [References, Test Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Test Agent guidelines

Leverage the full potential of Test Agent by following these guidelines.

## Supported metadata

Test Agent supports the following metadata:

-   sys\_ui\_action
-   sys\_ui\_policy
-   sys\_ui\_policy\_action
-   sys\_ui\_policy\_rl\_action
-   sys\_script\_client
-   sys\_ui\_script
-   sys\_data\_policy2
-   sys\_ui\_action\_role
-   sys\_ui\_action\_view
-   sys\_ui\_base\_theme
-   sys\_ui\_form
-   sys\_ui\_formatter
-   sys\_ui\_macro
-   sys\_ui\_message
-   sys\_ui\_related\_list
-   sys\_ui\_section
-   sys\_ui\_view
-   sys\_ui\_title
-   sys\_ui\_style
-   sys\_ui\_theme
-   sys\_ui\_page
-   sys\_ui\_context\_menu
-   sys\_ui\_list
-   sys\_ui\_list\_control
-   sys\_ui\_list\_control\_embedded
-   sys\_ui\_list\_script\_client
-   sys\_ui\_list\_script\_server
-   sys\_ui\_related\_list
-   sys\_user\_role
-   sys\_app\_application
-   sp\_widget
-   sp\_instance
-   sys\_security\_acl\_role
-   sys\_script
-   sys\_app\_module
-   sysevent\_email\_action
-   sys\_report
-   sys\_security\_acl
-   catalog\_ui\_policy
-   catalog\_ui\_policy\_action
-   sp\_theme
-   sp\_widget
-   sys\_sg\_universal\_link\_path\_segment
-   sys\_sg\_sections\_screen\_m2m\_section
-   sys\_sg\_location\_tracking\_details
-   sys\_highlighted\_value\_condition
-   sys\_sg\_card\_size
-   sys\_sg\_custom\_map\_config
-   sys\_sg\_empty\_state
-   sys\_aw\_form\_header\_secondary\_values
-   sys\_aw\_registered\_scripting\_modal
-   sys\_template
-   sys\_sg\_alert
-   sys\_aw\_form\_header
-   sys\_script\_include
-   sys\_scriplet\_function
-   sys\_ui\_extension\_instance
-   sys\_playbook\_experience\_action\_assignment\_map
-   sys\_df\_data\_filtration
-   sys\_email\_address\_filt\_domain
-   sys\_atf\_step
-   sys\_atf\_test
-   sys\_atf\_step\_config
-   atf\_input\_variable

## Exceptions

Test Agent doesn't support the following metadata:

-   Flows
-   Configurable workspace steps
-   Custom UI test steps
-   Custom test steps

## Scope and availability

Test Agent is available in the following environments and scopes:

|Dimension|Supported values|
|---------|----------------|
|Authoring environment|ServiceNow IDE or ServiceNow Studio|
|Application scope|Global, custom, store|
|Test types|ATF unit tests, ATF functional tests|
|Execution target|Cloud runner lanes|

## Example prompts

-   Write an ATF test in the global scope to validate that an employee can order a laptop from the Service Catalog.
-   Write an ATF test to validate that internal IT knowledge articles are not visible to self‑service users.
-   Write an ATF test to validate that all mandatory fields on the Incident form are completed before submission.

**Note:** The examples above are prompts for authoring ATF tests in the global scope. To run a test, prompt to execute the ATF test by specifying its name or sys\_id. To troubleshoot a failure, prompt to triage the failed ATF test by providing the test name or the sys\_id of the test result.

