---
title: Generate a test using Test generation
description: Simplify and automate your testing process with Test generation. Describe your desired test, and Now Assist empowered Test generation application automatically generates the necessary tests.
locale: en-US
release: australia
product: Test Generation
classification: test-generation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Test generation, Test generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Generate a test using Test generation

Simplify and automate your testing process with Test generation. Describe your desired test, and Now Assist empowered Test generation application automatically generates the necessary tests.

## Before you begin

Starting with the Australia release, Test generation is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: admin or now.assist.creator

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

    A list of tests shows up.

2.  Click **Create with Now Assist** to create a test using Now Assist.

    You can also create a regular ATF test by choosing your steps with the standard ATF interface. To create a regular ATF test, select the **Create on your own** button next to the **Create with Now Assist** button.

    The new Test form shows up.

3.  Select the **Application** scope from the globe icon.

4.  Enter your text prompt in the **Now Assist directions** field.

    **Note:** It is recommended to describe the expected test comprehensively for a desired output.

5.  Click **Generate test preview** to generate the preview test.

    The Test preview page appears.

    **Note:** The Test preview page is a read-only content which can't be directly edited. If you want to modify the generated preview test, you can edit your prompt in the **Now Assist directions** field on the Test preview page. See Test generation for more information.

6.  Click **Regenerate test preview** if you have modified your prompt.

    **Note:** This step is applicable only if you have modified the prompt on the Test preview page. The **Regenerate test preview** button is enabled only if you have updated the prompt.

7.  Click **Save and open test** once the test generation completes.

    **Note:** You can also click **Discard test** if you don't want to save the generated test.

    The created test shows up.

    **Note:** A generated test is designated as an active test only when you accept the test. If you don’t make a choice of either accepting or rejecting, the test is still saved but the active flag is set to false.

    If you want to edit a test after saving, you can modify it using any actions in the Test steps related list. See [Edit a generated test using Test generation](../concept/tg-edit-test.md) for more information.


**Parent Topic:**[Using Test generation](../concept/tg-use.md)

**Related topics**  


[Edit a generated test using Test generation](../concept/tg-edit-test.md)

