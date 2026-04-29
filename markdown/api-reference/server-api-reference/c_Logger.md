---
title: logger - Global
description: The logger API provides inbound email actions that append messages to the email log.Appends the specified message to the email log.Appends the specified error message to the email log file.Appends the specified warning message to the email log file.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# logger- Global

The logger API provides inbound email actions that append messages to the email log.

It provides methods that add information, warning, and error messages. The added message has its source set to `email.<Sys ID of incoming email>`.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## logger - log\(String msg\)

Appends the specified message to the email log.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Text to append to the email log. These should be information type messages.|

|Type|Description|
|----|-----------|
|void| |

This code example queries email from the sys\_user table and then calls the appropriate logger method based on the sender information.

```
var grUser = new GlideRecord("sys_user");
grUser.addQuery("email", email.from);
grUser.query();
  if (grUser.next()) {
    if (grUser.user_name) {
      logger.log("Sender found: " + email.from); //Append information message to the email log
      createInc(grUser.sys_id);
    } else {
        logger.logWarning("Sender: " + email.from + " " + "found but no userID found, please take necessary actions"); //Append warning message to the email log.
        createInc(grUser.sys_id);
    }
  } else {
      logger.logError("Sender is not present in the system hence action aborted"); //Append error message to the email log.
      current.setAbortAction(true);
  }
```

## logger - logError\(String msg\)

Appends the specified error message to the email log file.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Error message to append to the email log|

|Type|Description|
|----|-----------|
|void| |

This code example queries email from the sys\_user table and then calls the appropriate logger method based on the sender information.

```
var grUser = new GlideRecord("sys_user");
grUser.addQuery("email", email.from);
grUser.query();
  if (grUser.next()) {
    if (grUser.user_name) {
      logger.log("Sender found: " + email.from); //Append information message to the email log
      createInc(grUser.sys_id);
    } else {
        logger.logWarning("Sender: " + email.from + " " + "found but no userID found, please take necessary actions"); //Append warning message to the email log.
        createInc(grUser.sys_id);
    }
  } else {
      logger.logError("Sender is not present in the system hence action aborted"); //Append error message to the email log.
      current.setAbortAction(true);
  }
```

## logger - logWarning\(String msg\)

Appends the specified warning message to the email log file.

|Name|Type|Description|
|----|----|-----------|
|msg|String|Warning message to append to the email log|

|Type|Description|
|----|-----------|
|void| |

This code example queries email from the sys\_user table and then calls the appropriate logger method based on the sender information.

```
var grUser = new GlideRecord("sys_user");
grUser.addQuery("email", email.from);
grUser.query();
  if (grUser.next()) {
    if (grUser.user_name) {
      logger.log("Sender found: " + email.from); //Append information message to the email log
      createInc(grUser.sys_id);
    } else {
        logger.logWarning("Sender: " + email.from + " " + "found but no userID found, please take necessary actions"); //Append warning message to the email log.
        createInc(grUser.sys_id);
    }
  } else {
      logger.logError("Sender is not present in the system hence action aborted"); //Append error message to the email log.
      current.setAbortAction(true);
  }
```

