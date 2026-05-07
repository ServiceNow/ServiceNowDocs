---
title: Launch a feature in Engagement Messenger using custom code
description: Use the custom code to enable the deep linking and launch a feature in Engagement Messenger integrated with your website.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Deep linking feature, Engagement Messenger, Set up self-service, Configure, Customer Service Management]
---

# Launch a feature in Engagement Messenger using custom code

Use the custom code to enable the deep linking and launch a feature in Engagement Messenger integrated with your website.

## Before you begin

[Configure Engagement Messenger](create-engagement-messenger-module.md).

[Embed Engagement Messenger in your web application](embed-engagement-messenger-code-in-your-web-application.md).

Role required: ec\_admin and website administrator

## About this task

**Note:**

If you’re using existing code, verify that you update the script to show `v=3.1`. For example:

```
<script src="https://example.service-now.com/scripts/sn_csm_ec.js?v=3.1"></script>
<script>
SN_CSM_EC.init({
      moduleID: "https://example.service-now.com/#aeff0547dd393010f87734cef087e2ba",
      loadFeature: SN_CSM_EC.loadEMFeature()
});
</script>
```

## Procedure

1.  Navigate to **Engagement Messenger** &gt; **Modules**.

2.  In the Configure Engagement Messenger Module, open the Implement tab.

3.  Copy the code from the Embed code section.

4.  In a text editor, open the HTML file of the web page on your website where you integrate Engagement Messenger.

5.  Paste the code that you copied before the closing body tag.

6.  Define the feature context and specify the variables for the feature.

    Use the following format to define a feature context:

    ```
    { 
    	feature: "*&lt;feature\_name&gt;*", 
    	openOnLoad: *&lt;true/false&gt;*, 
    	params: { 
    		"*&lt;param\_name&gt;*": "*&lt;param\_value&gt;*",
    		"*&lt;param\_name&gt;*": "*&lt;param\_value&gt;* 
    	} 
    }
    ```

    In the format, specify the feature variables.

    -   **feature**

        The feature name. For more information, see [Feature context parameters supported in Engagement Messenger](../reference/contextual-launch-supported-features.md) .

    -   **openOnLoad**

        Include this option and set it to true only if you want Engagement Messenger to open automatically. The default setting for this option is for Engagement Messenger not to open automatically.

    -   **&lt;param\_name&gt;": "&lt;param\_value&gt;**

        Name and value of a parameter associated with the feature. For more information, see [Feature context parameters supported in Engagement Messenger](../reference/contextual-launch-supported-features.md).

7.  Create a custom wrapper function to pass the feature context to the `SN_CSM_EC.init` function of the embed code.

    For example, the following code uses the `chatFeatureContext()` custom wrapper function for the chat feature context.

    ```
    
    function chatFeatureContext(){ 
    	return { 
    			feature: "CHAT",
    			openOnLoad: false,
    			params: { 
    				"topic_id": "8708db281bd5b81080df6247b04bcb79",
    				"language": "fr"		
    				} 
    		  } 
    }
    ```

8.  Replace the `SN_CSM_EC.loadEMFeature()` function with a custom wrapper function that you created in [step 7](contextual-launch-using-script-engagement-messenger.md).

    For example, in the following code, the `chatFeatureContext()` wrapper function is passed as the value of the `loadFeature` attribute.

    ```
    SN_CSM_EC.init({ 
    		moduleID: "https://example.service-now.com/#<module_id>", 
    		loadFeature: *chatFeatureContext*()
    }); 
    
    ```

9.  Save the file.

10. Verify that the designated feature launches.

    1.  Open the website in which you embedded Engagement Messenger.

    2.  Select the launcher icon.

    3.  Verify that Engagement Messenger launches feature you configured in the embed code.


## Result

The feature you specified in the embed code is launched by default when Engagement Messenger is opened in the website in which it’s embedded.

## Example

The following code initiates the chat feature by default. It also shows how to trigger a Virtual Agent topic by default when chat is loaded by passing the system identifier \(sys\_id\) of the topic. You can also specify a language to initiate chat in that language.

```
<script src="https://example.servicenow.com/scripts/sn_csm_ec.js?v=3.1"></script>
<script>
function chatFeatureContext(){ 
	return { 
			feature: "CHAT",
			openOnLoad: false,
			params: { 
				"topic_id": "8708db281bd5b81080df6247b04bcb79",
				"language": "fr"		
				} 
		  } 
}

SN_CSM_EC.init({
	moduleID: "https://example.service-now.com/#d27c94d6db403810a2a6a0ced39619da",
	loadFeature: chatFeatureContext()
});
</script>
```

-   **function**

    *chatFeatureContext\(\)*: The wrapper function for chat context.

-   **feature**

    *CHAT*: The chat feature for initiating Virtual Agent or Live Agent chat.

-   **openOnLoad**

    *false*: Disable the automatic launch of Engagement Messenger.

-   **topic\_id**

    *8708db281bd5b81080df6247b04bcb79*: The module system identifier \(sys\_id\).

-   **language**

    *fr*: Sets the default chat language to French.


