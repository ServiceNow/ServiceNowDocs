---
title: Automated Test Framework Test API - ServiceNow Fluent
description: The Automated Test Framework Test API defines automated tests \[sys\_atf\_test\] that you can run to confirm that your instance works after making a change.Create an automated test \[sys\_atf\_test\] containing a series of steps to execute.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Automated Test Framework Test API - ServiceNow Fluent

The Automated Test Framework Test API defines automated tests \[sys\_atf\_test\] that you can run to confirm that your instance works after making a change.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about Automated Test Framework tests, see [Automated Test Framework \(ATF\)](../../../administer/auto-test-framework/concept/atf-landing-page.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Test object

Create an automated test \[sys\_atf\_test\] containing a series of steps to execute.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

A unique name for the test.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of what the test does.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the test is active.Valid values:

-   true: The test is active.
-   false: The test isn't active.

Default: true

</td></tr><tr><td>

failOnServerError

</td><td>

Boolean

</td><td>

Flag that indicates whether to fail when a server error occurs during the test.Valid values:

-   true: The test fails when a server error occurs.
-   false: The test doesn't fail when a server error occurs.

Default: true

</td></tr><tr><td>

configurationFunction

</td><td>

Function

</td><td>

The steps of the test. Test steps are passed as statements within the atf function. For example:```javascript
(atf) => {
    atf.form.openNewForm({
        table: 'sn_example_table',
        formUI: 'standard_ui',
        view: '',
    })
}
```

For more information about test steps, see [Supported test steps](atf-test-now-ts.md#section_q5c_qmp_ccc).

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>The output values of test steps with output variables can be saved as variables and used as inputs to other steps using the syntax `output.<output-variable>`. The output variables can be used both directly as inputs on appropriate fields or inside of a template string, such as with `atf.server.log` in the following example.

```javascript
import { Test } from '@servicenow/sdk/core'

Test({
        active: true,
        failOnServerError: true,
        name: 'Simple example',
        description: 'An illustrative test written in fluent',
        $id: Now.ID[1],
    },
    (atf) => {
        atf.form.openNewForm({
            table: 'sn_table_app_reptile_table',
            formUI: 'standard_ui',
            view: '',
        })
        atf.form.setFieldValue({
            table: 'sn_table_app_reptile_table',
            formUI: 'standard_ui',
            fieldValues: {
                reptiles: 'lizard' as any,
            },
        })
        const output = atf.form.submitForm({ assertType: 'form_submitted_to_server', formUI: 'standard_ui' })
        atf.server.recordValidation({
            recordId: output.record_id,
            table: 'sn_table_app_reptile_table',
            assertType: 'record_validated',
            enforceSecurity: true,
            fieldValues: 'reptiles=lizard',
        })
        atf.server.log({
            log: `Submitted record with sys_id: ${output.record_id} to table ${output.table}`
        })
    }
)
```

### Supported test steps

The following test steps are supported. For information about step properties, see the [Automated Test Framework \(ATF\) test step categories](../../../administer/auto-test-framework/reference/test-step-categories.md) documentation.

**Note:** Some fields available for test steps on forms aren't available as properties in ServiceNow Fluent.

<table id="table_uqw_2mp_ccc"><thead><tr><th>

Category

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

[Application Navigator category](../../../administer/auto-test-framework/reference/test-steps-app-navigator-category.md#)

</td><td>

-   atf.applicationNavigator.applicationMenuVisibility
-   atf.applicationNavigator.moduleVisibility
-   atf.applicationNavigator.navigateToModule

</td></tr><tr><td>

[Email category](../../../administer/auto-test-framework/reference/test-steps-email-category.md#)

</td><td>

-   atf.email.generateInboundEmail
-   atf.email.generateInboundReplyEmail
-   atf.email.generateRandomString
-   atf.email.validateOutboundEmail
-   atf.email.validateOutboundEmailGeneratedByFlow
-   atf.email.validateOutboundEmailGeneratedByNotification

</td></tr><tr><td>

[Form category](../../../administer/auto-test-framework/reference/test-steps-form-category.md#)

</td><td>

-   atf.form.addAttachmentsToForm
-   atf.form.clickDeclarativeAction
-   atf.form.clickModalButton
-   atf.form.clickUIAction
-   atf.form.declarativeActionVisibility
-   atf.form.fieldStateValidation
-   atf.form.fieldValueValidation
-   atf.form.openExistingRecord
-   atf.form.openNewForm
-   atf.form.setFieldValue
-   atf.form.submitForm
-   atf.form.uiActionVisibility

</td></tr><tr><td>

[Forms in Service Portal category](../../../administer/auto-test-framework/reference/test-steps-forms-portal-category.md#)

</td><td>

-   atf.form\_SP.addAttachmentsToForm
-   atf.form\_SP.clickUIAction\_SP
-   atf.form\_SP.fieldStateValidation\_SP
-   atf.form\_SP.fieldValueValidation\_SP
-   atf.form\_SP.openForm\_SP
-   atf.form\_SP.openServicePortalPage
-   atf.form\_SP.setFieldValue\_SP
-   atf.form\_SP.submitForm\_SP
-   atf.form\_SP.uiActionVisibilityValidation\_SP

</td></tr><tr><td>

Quick start tests for Dashboards

</td><td>

-   atf.reporting.responsiveDashboard
-   atf.reporting.responsiveDashboardSharing

</td></tr><tr><td>

[REST category](../../../administer/auto-test-framework/reference/test-steps-rest-category.md#)

</td><td>

-   atf.rest.assertJsonResponsePayloadElement
-   atf.rest.assertResponseHeader
-   atf.rest.assertResponseJSONPayloadIsValid
-   atf.rest.assertResponsePayload
-   atf.rest.assertResponseTime
-   atf.rest.assertResponseXMLPayloadIsWellFormed
-   atf.rest.assertStatusCode
-   atf.rest.assertStatusCodeName
-   atf.rest.assertXMLResponsePayloadElement
-   atf.rest.sendRestRequest

</td></tr><tr><td>

[Server category](../../../administer/auto-test-framework/reference/test-steps-server-category.md#)

</td><td>

-   atf.server.addAttachmentsToExistingRecord
-   atf.server.checkoutShoppingCart
-   atf.server.createUser
-   atf.server.impersonate
-   atf.server.log
-   atf.server.recordDelete
-   atf.server.recordInsert
-   atf.server.recordQuery
-   atf.server.recordUpdate
-   atf.server.recordValidation
-   atf.server.replayRequestItem
-   atf.server.runServerSideScript
-   atf.server.searchForCatalogItem
-   atf.server.setOutputVariables

</td></tr><tr><td>

[Service Catalog category](../../../administer/auto-test-framework/reference/test-steps-service-catalog-category.md#)

</td><td>

-   atf.catalog.addItemToShoppingCart
-   atf.catalog.openCatalogItem
-   atf.catalog.openRecordProducer
-   atf.catalog.orderCatalogItem
-   atf.catalog.setCatalogItemQuantity
-   atf.catalog.setVariableValue
-   atf.catalog.submitRecordProducer
-   atf.catalog.validatePriceAndRecurringPrice
-   atf.catalog.variableStateValidation
-   atf.catalog.validateVariableValue

</td></tr><tr><td>

[Service Catalog in Service Portal category](../../../administer/auto-test-framework/reference/test-steps-catalog-portal-category.md#)

</td><td>

-   atf.catalog\_SP.addItemtoShoppingCart\_SP
-   atf.catalog\_SP.addOrderGuidetoShoppingCart\_SP
-   atf.catalog\_SP.addRowToMultiRowVariableSet\_SP
-   atf.catalog\_SP.navigatewithinOrderGuide\_SP
-   atf.catalog\_SP.openCatalogItem\_SP
-   atf.catalog\_SP.openOrderGuide\_SP
-   atf.catalog\_SP.openRecordProducer\_SP
-   atf.catalog\_SP.orderCatalogItem\_SP
-   atf.catalog\_SP.reviewIteminOrderGuide\_SP
-   atf.catalog\_SP.reviewOrderGuideSummary\_SP
-   atf.catalog\_SP.saveCurrentRowOfMultiRowVariableSet\_SP
-   atf.catalog\_SP.setCatalogItemQuantity\_SP
-   atf.catalog\_SP.setVariableValue\_SP
-   atf.catalog\_SP.submitOrderGuide\_SP
-   atf.catalog\_SP.submitRecordProducer\_SP
-   atf.catalog\_SP.validateOrderGuideItem\_SP
-   atf.catalog\_SP.validatePriceAndRecurringPrice\_SP
-   atf.catalog\_SP.variableStateValidation\_SP
-   atf.catalog\_SP.validateVariableValue\_SP

</td></tr></tbody>
</table>