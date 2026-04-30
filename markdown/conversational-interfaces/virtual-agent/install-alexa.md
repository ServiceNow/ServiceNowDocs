---
title: Install Conversational Integration with Alexa
description: You can install the Conversational Integration with Alexa application \(sn.va.alexa\) if you have the admin role. The application installs the related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Conversational Integration with Alexa, Integrating Virtual Agent with Alexa, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Install Conversational Integration with Alexa

You can install the Conversational Integration with Alexa application \(sn.va.alexa\) if you have the admin role. The application installs the related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Role required: external\_app\_install\_admin, va\_admin, or admin

## About this task

The following applications are installed with Conversational Integration with Alexa:

-   **Conversational Custom Chat Integration \(com.glide.cs.custom.adapter\)**

    Provides the custom chat integration framework of scriptable APIs to enable the Virtual Agent application on any conversational interface.

    For more information, see [Creating conversational custom chat integrations in Virtual Agent](../concept/va-custom-adapter-framework.md).

-   **ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)**

    Enables the execution of ServiceNow® Integration Hub actions and flows.


## Procedure

1.  **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**

2.  Find the Conversational Integration with Alexa application \(sn\_va\_alexa\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    All the dependent plugins and applications are listed if they will be installed, or currently installed, or must be installed. If any plugins or applications must be installed, you must install them before you can install Conversational Integration with Alexa.

4.  Click **Install**.


## What to do next

**JSON for configuring Alexa**

```
{
    "interactionModel": {
        "languageModel": {
            "invocationName": "my agent",
            "intents": [
                {
                    "name": "AMAZON.CancelIntent",
                    "samples": []
                },
                {
                    "name": "AMAZON.HelpIntent",
                    "samples": []
                },
                {
                    "name": "AMAZON.StopIntent",
                    "samples": []
                },
                {
                    "name": "EverythingIntent",
                    "slots": [
                        {
                            "name": "EverythingSlot",
                            "type": "Bag_of_words"
                        }
                    ],
                    "samples": [
                        "{EverythingSlot}"
                    ]
                },
                {
                    "name": "AMAZON.NavigateHomeIntent",
                    "samples": []
                },
                {
                    "name": "VAKeywordIntent",
                    "slots": [
                        {
                            "name": "skip_keyword_slot",
                            "type": "Skip_slot_type"
                        },
                        {
                            "name": "repeat_keyword_slot",
                            "type": "Repeat_keyword_slot_type"
                        },
                        {
                            "name": "more_keyword_slot",
                            "type": "More_keyword_slot_type"
                        }
                    ],
                    "samples": [
                        "{more_keyword_slot}",
                        "{repeat_keyword_slot}",
                        "{skip_keyword_slot}"
                    ]
                }
            ],
            "types": [
                {
                    "name": "Bag_of_words",
                    "values": [
                        {
                            "name": {
                                "value": "name: bag_of_words"
                            }
                        }
                    ]
                },
                {
                    "name": "Skip_slot_type",
                    "values": [
                        {
                            "name": {
                                "value": "skip"
                            }
                        }
                    ]
                },
                {
                    "name": "More_keyword_slot_type",
                    "values": [
                        {
                            "name": {
                                "value": "more"
                            }
                        }
                    ]
                },
                {
                    "name": "Repeat_keyword_slot_type",
                    "values": [
                        {
                            "name": {
                                "value": "repeat"
                            }
                        }
                    ]
                }
            ]
        }
    }
}
```

