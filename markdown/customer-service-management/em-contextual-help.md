---
title: Use Engagement Messenger embed Code to integrate proactive recommendations on a web page
description: Modify the embed code of Engagement Messenger to enable recommendations and pass the search query for recommendations based on AI Search.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up Engagement Messenger, Enable communication channels, Configure, Customer Service Management]
---

# Use Engagement Messenger embed Code to integrate proactive recommendations on a web page

Modify the embed code of Engagement Messenger to enable recommendations and pass the search query for recommendations based on AI Search.

## Before you begin

-   [Embed Engagement Messenger in your web application](embed-engagement-messenger-code-in-your-web-application.md).
-   [Activate an Engagement Messenger module](activate-engagement-messenger-module.md).
-   Role required: sn\_csm\_ec.ec\_admin

## Procedure

1.  Navigate to **All** &gt; **Engagement Messenger** &gt; **Modules**.

2.  Select the Engagement Messenger module you want to install on your website.

3.  In the Edit module column, click **Edit**.

4.  In the Configure Engagement Messenger module, select the **Implement** tab.

5.  In a text editor, open the HTML file of the web page on your website where you integrate Engagement Messenger.

6.  In the **Implement** tab, copy the code from the Embed code section.

7.  Paste the code you copied into the text file before the closing body tag.

8.  Enable recommendations for a specific page in messenger by adding the parameter `enableRecommendations: true` in the embed code.

    In the website where you integrate Engagement Messenger, when the user enters a search term in messenger, by default the website URL slug \(last part of the URL\) will be considered the search query. The URL slug conditions for the search query entered in the messenger search bar are as follows:

    -   If a single forward slash is at the end of the URL, then no search term is picked. For example, `https://example.service-now.com/`.
    -   If a term is surrounded by forward slashes at the end of the URL, the enclosed text is considered to be a search term. For example, in the URL `https://example.service-now.com/product-xyz/`, product xyz is considered a search term.
    -   If a single forward slash is followed by text, that text is considered to be a search term. For example, in the URL `https://example.service-now.com/search_string` search string is considered as a search term.
    The URL slug is used to deduce the search query as follows:

    -   All the special characters are replaced by a space. For example, in the URL `https://example.service-now.com/product-xyz`, the search term is "product xyz".
    -   Any file extension is ignored. For example, in the URL `https://example.service-now/product.html`, the search term is "product".
9.  Enable recommendations at the module level.

    1.  Navigate to **All** &gt; **Engagement Messenger** &gt; **Modules**.

    2.  Select your Engagement Messenger module.

    3.  Click **Edit**.

    4.  In the Configure Engagement Messenger module, select the **Behavior** tab.

    5.  Enable the **Enable recommendations** toggle switch.

10. Add custom logic for passing a search query parameter to the AI Search by passing a function callback as the value for a parameter `getAISRecommendationsContext`.

    The following example shows the modified code to generate proactive recommendations with the custom logic for passing a search context query.

    ```
    ‹script src="https://example.service-now.com/scripts/sn_csm_ec.js"></script>
      ‹script>
      SN_CSM_EC.init({
                  moduleID:"https://instancename.service-now.com/<sys_id>",
                   loadFeature: SN CSM EC. loadEMFeature(),
                   enableRecommendations: true, 
                   getAISRecommendationsContext: function getSearchQuery(){
                   //Insert your code here to fetch the search query string return product xyz
    }
    
      };
      </script>
    ```

11. Save and publish the HTML file.


## Result

Engagement Messenger shows recommendations based on the context provided by the third-party website.

## Example

The following example shows the modified code to generate default proactive recommendations for the default context.

```
‹script src="https://example.service-now.com/scripts/sn_csm_ec.js"></script>
  ‹script>
  SN_CSM_EC.init({
              moduleID:"https://instancename.service-now.com/<sys_id>",
               loadFeature: SN CSM EC. loadEMFeature(),
               enableRecommendations: true 
              }

  };
  </script>
```

