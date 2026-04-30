---
title: Link Alexa events using the macOS Terminal
description: Link Alexa events using your macOS Terminal to complete the Alexa account linking process with your ServiceNow instance.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Account linking with Alexa, Configure Conversational Integration with Alexa, Conversational Integration with Alexa, Conversational IVR with Amazon Connect, Virtual Agent integration with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Link Alexa events using the macOS Terminal

Link Alexa events using your macOS Terminal to complete the Alexa account linking process with your ServiceNow instance.

## Before you begin

**Note:** Copy the Skill ID of your skill from the Alexa developer console. The Skill ID is the same inbound ID used in the sys\_cs\_provider\_application record.

Role required: admin

## Procedure

1.  On your macOS, open the Terminal.

2.  Execute the `npm install -g ask-cli` command.

    Executing this command installs the Alexa command-line interface on your machine if it was not previously installed.

3.  Execute the `ask configure` command.

4.  Log in with your Amazon developer account credentials when prompted.

    **Note:** Choose **No** if you are asked the question **Do you want to link your AWS account in order to host your Alexa skills?**

5.  To download the manifest file, execute the `ask smapi get-skill-manifest -s {<provide skillId>} > skill.json` command.

6.  To edit the `skill.json` file, add the following JSON script inside the manifest object.

    ```
    "events": { 
          "endpoint": { 
            "uri": <provide lambda ID>.  
          }, 
          "subscriptions": [ 
            { 
              "eventName": "SKILL_ENABLED" 
            }, 
            { 
              "eventName": "SKILL_DISABLED" 
            }, 
            { 
              "eventName": "SKILL_PERMISSION_ACCEPTED" 
            }, 
            { 
              "eventName": "SKILL_PERMISSION_CHANGED" 
            }, 
            { 
              "eventName": "SKILL_ACCOUNT_LINKED" 
            } 
          ] 
        },
    ```

    **Note:** Be sure to edit the URL endpoint with the Lambda ID. You can copy one of the endpoints from the `skill.json` file and replace it with the Lambda ID. You can also fetch it from the Alexa console from **Build** &gt; **Endpoints**.

7.  To upload the updated manifest file, execute the `ask smapi update-skill-manifest -s {<provide skillId>} --manifest "$(cat skill.json)` command.


## Result

Your Alexa account is linked with your ServiceNow instance.

Your Alexa account is linked with your ServiceNow instance.

