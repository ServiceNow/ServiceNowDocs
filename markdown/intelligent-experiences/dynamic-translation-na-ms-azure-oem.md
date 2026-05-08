---
title: Microsoft Azure OEM for Dynamic Translation in Now Assist
description: Support multi-language input in Now Assist applications with the Microsoft Azure OEM translator service included in Generative AI Controller.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 2
keywords: [Microsoft Azure OEM, Dynamic Translation, Now Assist, multi-language input, generative AI controller, translator configurations]
breadcrumb: [Configure multilingual service for Now Assist applications, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Microsoft Azure OEM for Dynamic Translation in Now Assist

Support multi-language input in Now Assist applications with the Microsoft Azure OEM translator service included in Generative AI Controller.

## Multi-language support for Now Assist applications

![In the Translator Configurations table, the Microsoft Azure OEM record](../image/dynamic-translation-na-ms-azure-oem-X1.png)

When dynamic translation in the Generative AI Controller is enabled, your users' input text is handled by Microsoft Azure OEM \(com.snc.microsoft\_oem\_translation\_spoke\) as follows:

1.  The language of the text is detected.
2.  The text is dynamically translated to English, then provided to Now Assist.
3.  Now Assist returns a response in English.
4.  The English response is translated to the user's preferred language and displayed in the UI.

For more information about enabling dynamic translation in this context, see [Configure multilingual service for Now Assist applications](../task/enable-dynamic-translation-for-now-assist-applications.md) and [Enable Dynamic Translation for capabilities in Generative AI Controller](../../generative-ai-controller/task/enable-dynamic-translation-for-generative-ai-capabilities.md).

From the Zurich release, this spoke has available support for specific regulated markets, subject to conditions. For information see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) on the Now Support portal.

## Activation

The Microsoft Azure OEM translator service is included with Generative AI Controller. Microsoft Azure OEM requires Dynamic Translation tables, so Generative AI Controller activates Dynamic Translation if it isn't already active.

Microsoft Azure OEM appears as a row in the Translator Configurations \(sn\_dt\_translator\_configuration\) table. This record is not editable. The connection credentials of this translator service are already configured. For more information about this integration, see [https://www.servicenow.com/company/media/press-room/gen-ai-now-platform.html](https://www.servicenow.com/company/media/press-room/gen-ai-now-platform.html).

If you try to update this record in the Translator Configurations table, the following error is displayed: "The Microsoft Azure OEM translator configuration is used in Generative AI flows. It cannot be edited".

With the Xanadu Patch 3 release, the Microsoft Azure OEM translator includes support for Exclusion Framework in Dynamic Translation. Also the API used by flows and subflows is automatically updated to v4.

The application scope for Microsoft Azure OEM is sn\_ms\_oem.

For more information, see Dynamic Translation.

**Parent Topic:**[Configure multilingual service for Now Assist applications](../task/enable-dynamic-translation-for-now-assist-applications.md)

**Related topics**  


[bundle-platadm.dynamic-translation-overview]

[Generative AI Controller](../../generative-ai-controller/concept/generative-ai-controller.md)

