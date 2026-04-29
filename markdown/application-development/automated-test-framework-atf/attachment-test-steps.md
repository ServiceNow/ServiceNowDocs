---
title: Attachment test steps
description: Test an attachment-dependent business rule by uploading an attachment either from a form or from a server-side API call. For example, you can have a business rule that doesn't let you close an incident without an attachment such as a screenshot.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Attachment test steps

Test an attachment-dependent business rule by uploading an attachment either from a form or from a server-side API call. For example, you can have a business rule that doesn't let you close an incident without an attachment such as a screenshot.

-   **Upload from form**

    As a UI test step, the upload attachment step requires navigation to a form, which you can open using either **Open a New Form** or **Open an Existing Record**. Use **Upload Attachments** to select from the attachments that the test step adds to the form. When you select attachments to add to a form, the system waits to load the attachments before proceeding to the next test step. For more information on UI test dependency and wait mechanism, see [UI test steps](ui-test-steps.md).

-   **Upload from Server API**

    As a Server test step, the upload attachment step has no UI dependencies. Use **Upload Attachments** to select from the attachments that the test step adds to the record. When you select attachments to add to a form, the system waits for the attachments to be loaded before proceeding to the next test step. For more information, see [Server test steps](server-test-steps.md).


## Design considerations

Follow these design considerations for attachment test steps:

-   All attachment steps require adding one or more attachments.
-   The system rolls back any attachments by the step after the test completes.
-   The system cannot roll back any existing attachments after the test completes.
-   Avoid testing records with existing attachments to eliminate data dependency.
-   If UI testing is involved, add the attachment to a form.
-   When no UI is involved, add the attachment to the Server API.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)

