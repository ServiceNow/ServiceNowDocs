---
title: Design considerations for prompting
description: Generate your desired test by following the guided principles of effective prompting.
locale: en-US
release: yokohama
product: Test Generation
classification: test-generation
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Test generation references, Test generation, Testing and debugging applications, Building applications]
---

# Design considerations for prompting

Generate your desired test by following the guided principles of effective prompting.

-   Clear and concise ATF prompts that describes test steps
-   Consider the scope and capability of Test generation
    -   Test generation is a Now Assist backed skill to create ATF tests
    -   The tests are created in the application scope that you are currently on
    -   Other types of functional or integration tests are out of Test generation scope
    -   Test generation can't update or delete existing ATF tests
-   Test generation supports the following
    -   Forms: open/submit form, field validation/visibility, UI/Declarative Action and Modal button. Each form API supports workspace as formUI type, including service\_operations\_workspace and asset\_workspace and cmdb\_workspace.
    -   Server operations: impersonation/create user, log message, record CRUD, replay request, search catalog item and check out shopping cart​.
    -   Email: generate, reply, send and validate inbound / outbound email​
    -   Application Navigator: navigate to module, menu/module visibility​
    -   Reporting: report visibility, dash board visibility and sharing​
    -   Service Catalog: open/order catalog item, add item to shopping cart, set/validate item quantity, submit order, validate quantity, price, and variable status​

<table id="table_o43_zss_12c"><thead><tr><th>

Good and effective prompts

</th><th>

Bad and irrelevant prompts

</th><th>

Comparison description

</th></tr></thead><tbody><tr><td>

Write a test to create a new user with name Bill McDermott and assign the "itil" role. Create a new incident record, update the short description to "my new test record" and then validate the record description. Update caller to Bill McDermott, impact and urgency categories to "2- Medium" and submit the record. Delete the record and create a log for the deletion.

</td><td>

I need a new user Bill McDermott to open a new record. Make sure its called my new test record. Update caller to user, impact and urgency categories to Med. Delete the record and create a log for the deletion.

</td><td>

The bad prompt is irrelevant and incomplete for the following reasons:-   No user role defined
-   Insufficient definition around the new user. Its unclear if the new user is to be created or impersonated
-   Insufficient definition around record handling with the name
-   No specific info about the caller field update
-   Not specific about category value to be used

</td></tr><tr><td>

Write an ATF test, named 'incident record test', impersonate admin, create a new incident record, then update the record short description to 'test update field from example', delete the record, then log a message 'record deleted'

</td><td>

Create an ATF test for an admin to create an incident record. Make description test update field from example. Then delete the record

</td><td>

The bad prompt lacks the following:-   Does not specify "create a new user" or "impersonate" for the model to understand
-   Unclear expectation around setting description name
-   Unclear where exactly the name for the description begins

</td></tr><tr><td>

Write a test to open Apple iPhone 13 catalog item, set color to 'pink', monthly data allowance to 500MB, validate price to be $800.00 and log the price

</td><td>

Write a test to open iPhone, color should be pink and data should be 500. The price should be 800. Log the price

</td><td>

The bad prompt is incomplete for the following reasons:-   Catalog Item entity hasn’t been called out
-   Missing keywords such as set or update for field value settings
-   Incomplete field id specified for monthly data allowance
-   Unclear expectation for price validation
-   Missing $ sign in price

</td></tr></tbody>
</table>**Parent Topic:**[Test generation references](tg-reference.md)

**Related topics**  


[Test generation design considerations](tg-summary.md)

