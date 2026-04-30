---
title: Create an Alexa skill
description: Create an Alexa-hosted skill using the Alexa developer console. Creating an Alexa skill helps you prepare to use the Alexa app.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up Conversational Integration with Alexa, Configure Conversational Integration with Alexa, Integrating Virtual Agent with Alexa, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Create an Alexa skill

Create an Alexa-hosted skill using the Alexa developer console. Creating an Alexa skill helps you prepare to use the Alexa app.

## Before you begin

Role required: admin

## Procedure

1.  Log in to the Alexa developer console with your Amazon developer account.

2.  Click **Create Skill**.

3.  In the **Skill name** field, enter a skill name.

4.  From the Default language list, select a default language to add your skill.

5.  Under Choose a model to add your skill, select **Custom**.

6.  Under Choose a method to host your skill's backend resources, select **Alexa-Hosted \(Node.js\)**.

7.  Click **Create skill**.

8.  To add your skill, select the **Start from Scratch** template.

9.  Click **Continue with Template**.

    **Note:** Creating an Alexa-hosted skill takes a few minutes.

10. In the skill, navigate to **Interaction Model** &gt; **Intents** &gt; **JSON Editor**.

11. Replace the **JSON Editor** with the following JSON script.

    ```
    {
        "interactionModel": {
            "languageModel": {
                "invocationName": "now agent",
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
                        "name": "AMAZON.NavigateHomeIntent",
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
                    }
                ],
                "types": [
                    {
                        "name": "Bag_of_words",
                        "values": [
                            {
                                "name": {
                                    "value": "value: Hello world"
                                }
                            },
                            {
                                "name": {
                                    "value": "name: bag_of_words"
                                }
                            }
                        ]
                    }
                ]
            }
        }
    }
    ```

12. Click **Save Model**.

13. Navigate to **Invocations** &gt; **Skill Invocation Name**.

14. In the **Skill Invocation Name** field, provide the skill Invocation name.

    **Note:** The skill name is the name which you use in your Alexa device to invoke the skill.

    For example: `<ask <skill name>`.

15. Navigate to **Interfaces** and enable **Alexa Presentation Language**.

    **Note:** This option enables all the screen devices which you want to use in Alexa.

16. Click **Save Interfaces**.


