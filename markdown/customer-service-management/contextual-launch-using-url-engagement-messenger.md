---
title: Launch a feature in Engagement Messenger using URL parameters
description: Use URL parameters in your website's URL to enable the deep linking and launch a feature in Engagement Messenger integrated with your website.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Deep linking feature in Engagement Messenger, Set up Engagement Messenger, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Launch a feature in Engagement Messenger using URL parameters

Use URL parameters in your website's URL to enable the deep linking and launch a feature in Engagement Messenger integrated with your website.

## Before you begin

[Configure Engagement Messenger](create-engagement-messenger-module.md).

[Embed Engagement Messenger in your web application](embed-engagement-messenger-code-in-your-web-application.md).

Role required: ec\_admin and website administrator

## About this task

You can use URL parameters to display specific feature in Engagement Messenger. When the URL is accessed, it opens your website and automatically loads the specified feature in Engagement Messenger. For example, you can embed the URL in an email to share a knowledge article from Engagement Messenger.

**Note:**

If you are using existing Embed code, ensure that you update the script to include `v=3.1`. For example:

![Engagement Messenger with the version number highlighted in the Embed code.](../image/em-version-no-update.png)

## Procedure

1.  Navigate to **Engagement Messenger** &gt; **Modules**.

2.  In the Configure Engagement Messenger Module, open the Implement tab.

3.  Copy the code from the Embed code section.

4.  In a text editor, open the HTML file of the web page on your website where you integrate Engagement Messenger.

5.  Paste the code you copied before the closing body tag.

6.  Save the file.

7.  Modify the website URL to include the feature.

    ```
    https://website/page.html?feature=<FEATURE_NAME>&<PARAM_NAME1>=<PARAM_VALUE1>&<PARAM_NAME2>=<PARAM_VALUE2>
    ```

    -   **&lt;FEATURE\_NAME&gt;**

        The feature name. For information, see [Feature context parameters supported in Engagement Messenger](../reference/contextual-launch-supported-features.md).

    -   **&lt;param\_name1&gt;=&lt;param\_value1&gt;**

        Name and value of a parameter associated with the feature. To define multiple parameters, use the same format. For more information, see [Feature context parameters supported in Engagement Messenger](../reference/contextual-launch-supported-features.md).

8.  Verify that the URL launches the designated feature automatically.


## Result

The feature you included in the URL is set as the default launch screen in Engagement Messenger.

## Example

The following sample URL includes a system identifier \(sys\_id\) for a knowledge article that will automatically display when the website is launched.

```
https://mywebsite/page.html?feature=VIEW_ARTICLE &sys_kb_id=ec7617461b01f01080df6247b04bcbaf
```

