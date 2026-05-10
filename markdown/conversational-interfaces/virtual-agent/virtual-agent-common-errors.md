---
title: Common errors in Virtual Agent API
description: This section describes some common errors in Virtual Agent API and how they can be resolved.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-02-02"
reading_time_minutes: 3
breadcrumb: [Virtual Agent API reference, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Common errors in Virtual Agent API

This section describes some common errors in Virtual Agent API and how they can be resolved.

## Virtual Agent API structure validation

**Request structure:**

Virtual Agent API expects the following JSON structure:

```
{
  "requestId": "any-unique-request-id",
  "clientSessionId": "any-unique-session-id",
  "userId": "any-unique-user-id",
  "emailId": "user@example.com",
  "action": "",
  "message": {
    "text": "User message text",
    "typed": true
  },
  "contextVariables": {},
  "history": [
    {
      "isBotMessage": true,
      "value": "How can I help you?",
      "displayName": "Bot",
      "type": "text"
    }
  ],
  "clientVariables": {
    "id": "va-bot-12345",
    "timestamp": "1687527831786"
  }
}
```

|Field|Required|Description|
|-----|--------|-----------|
|`requestId`|No|Pass-through variable returned in responses|
|`clientSessionId`|No|Pass-through session identifier|
|`userId`|Yes|Unique user identifier \(mandatory\)|
|`emailId`|No\*|User email for linking \(\*required for user linking\)|
|`action`|No|Optional action parameter|
|`message.text`|Yes|User message content \(mandatory\)|
|`message.typed`|No|`true` for search text, `false` for value selection|
|`contextVariables`|No|Optional context data|
|`history`|No|Bot conversation history \(first request only\)|
|`clientVariables`|No|Pass-through client variables|

**Note:** Only **userId** and **message.text** are mandatory fields in the request.

## File upload issues

Virtual Agent API supports two file upload modes, such as Synchronous and Asynchronous.

**File upload request structure:**

```
{
    "userId": "{{user_id}}",
    "message": {
        "attachment": {
                "clientAttachmentId": "{{request_id}}",
                "contentType": "video/mp4",
                "fileName": "sample.mp4",
                "url": "https://sample-videos.com/video123/mp4/720/big_buck_bunny_720p_1mb.mp4",
                "headers": {
                    "header 1": "value 1"
                }
            },
        "text": "along with text",
        "typed": true
    }
}
```

|Field|Required|Description|
|-----|--------|-----------|
|`contentType`|Yes|MIME type \(e.g., `video/mp4`, `image/png`\)|
|`fileName`|Yes|Name of the file with extension|
|`url`|Yes|Accessible URL to download the file|
|`clientAttachmentId`|No|Unique identifier for tracking|
|`headers`|No|Authentication headers for file download|

**File upload in synchronous mode:**

To upload a file in synchronous mode, follow the below steps:

1.  Upload the file by using Media API. For more information, see [CCCIF Media Resource API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/cccif-api.md).

    Media API returns a url. An example of the response is:

    ```
    {
      "result": {
        "mediaUrl": "<instance>/api/now/v1/cs/media/JOBBfkqSq6kDiFzxyinvHhke73O4TZ0j",
        "name": "image.png",
        "state": "available",
        "attachmentId": "e8671b9193209210a755b8e86cba104b"
      }
    }
    ```

2.  Use the media url in Virtual Agent API request. A JSON example is:

    ```
    {
      "userId": "user123",
      "message": {
        "attachment": {
          "contentType": "image/png",
          "fileName": "image.png",
          "url": "<instance>/api/now/v1/cs/media/JOBBfkqSq6kDiFzxyinvHhke73O4TZ0j"
        },
        "text": "Here is the image",
        "typed": true
      }
    }
    ```


**File upload in asynchronous mode:**

You can upload a file in asynchronous mode in two ways:

1.  Use the file url in the Virtual Agent API request.
    -   Direct file url:

        ```
        {
          "userId": "user123",
          "message": {
            "attachment": {
              "contentType": "application/pdf",
              "fileName": "report.pdf",
              "url": "https://publicserver.com/files/report.pdf"
            },
            "text": "Document attached",
            "typed": true
          }
        }
        ```

    -   Protected file url:

        ```
        {
          "userId": "user123",
          "message": {
            "attachment": {
              "contentType": "application/pdf",
              "fileName": "confidential.pdf",
              "url": "https://secureserver.com/files/confidential.pdf",
              "headers": {
                "Authorization": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
                "X-Custom-Header": "custom-value"
              }
            },
            "text": "Secure document attached",
            "typed": true
          }
        }
        ```

2.  Using the Media API \(as followed in synchronous mode\).

## User linking issues

Virtual Agent API supports automatic user linking only out-of-the-box. Manual linking is not enabled by default in Virtual Agent API.

**Prerequisites for user linking:**

1.  Message Auth is mandatory.
    -   Without message auth in `sys_cs_provider_application`, user linking doesn't work.
    -   You must configure Message auth properly. \(See the authentication section.\)
2.  Required request fields.
    -   `userId` must be present and unique.
    -   `emailId` must be present and valid.

**User record requirements:**

The `emailId` must match a `sys_user` record that meets all of the below conditions:

-   Record exists in the `sys_user` table.
-   Email field matches exactly.
-   User is active. \(`active=true`\)
-   User is not locked out. \(`locked_out=false`\)
-   Only one user record matches these conditions.

**Note:** If multiple users have the same email, linking fails.

**Auto linking configuration:**

1.  Verify the provider configuration.
    -   Navigate to the `sys_cs_provider` table and open the **"VA Bot to Bot Provider"** record.
    -   |Field|Expected Value|
|-----|--------------|
|`automatic_link_enabled`|`true`|
|`automatic_link_action`|`sn_va_as_service.virtual_agent__bot_to_bot_auto_link_account`|
|`link_account_enabled`|`true`|

2.  Check the provider user map.
    -   Navigate to the `provider_user_map` table.
    -   Filter by: `active=false` AND `channel_user_id={userId from request}`.
    -   Issue: If record exists with `active=false`, the user cannot be linked automatically.
    -   Solution: Admin must manually delete the inactive record and retry the linking request.
3.  Check for customizations.
    -   Review customizations by running the `sn_va_as_service.virtual_agent__bot_to_bot_auto_link_account` script.
    -   Check for the common customization issues:
        -   Logic preventing automatic linking
        -   Additional validation checks
        -   Modified field mappings

**User linking troubleshooting checklist:**

-   Configuration:
    -   Message auth exists and is active.
    -   `userId` is present in request.
    -   `emailId` is present in request.
    -   `automatic_link_enabled = true`
    -   `automatic_link_action` points to correct script.
    -   `link_account_enabled = true`
-   User record:
    -   User exists in `sys_user`.
    -   Email matches exactly \(case-sensitive\).
    -   User is active.
    -   User is not locked out.
    -   Only one user matches the email.
-   Provider user map:
    -   No inactive records for this `userId`.
    -   Check for duplicate mappings.
-   Customizations:
    -   Review auto-link script for modifications.
    -   Test with OOB script if customized.

**Parent Topic:**[Virtual Agent API reference](virtual-agent-api-reference.md)

