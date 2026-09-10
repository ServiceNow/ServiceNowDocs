---
title: Considerations for file upload and download
description: Lists the details of the supported file types and validation rules.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-08-21"
reading_time_minutes: 1
keywords: [file upload, file download, web agent, reference]
---

# Considerations for file upload and download

Lists the details of the supported file types and validation rules.

## Upload validation rules

The agent checks the following conditions before and after providing a file for upload.

|Condition|Result|Error message|
|---------|------|-------------|
|The file path is empty, missing, or not text|A human-in-the-Loop step is triggered that prompts the user to provide the required file path to unblock the process.|"File path is empty or invalid"|
|The file path contains a parent-directory reference \(`..`\)|Blocked|"Path traversal \(..\) is not allowed"|
|The file extension matches a blocked type \(see the following table\)|Blocked|"Blocked file type: "|
|The file does not attach after being supplied — the path does not exist, is unreadable, or does not match the input's accepted file types|Blocked|"File was not attached. The path likely does not exist, is unreadable, or does not match the input's accepted file types."|

## Blocked file types

The agent does not upload files with the following extensions, regardless of the file input's accept attribute.

|Category|Blocked extensions|
|--------|------------------|
|Executables|`.exe`, `.msi`, `.dll`, `.com`, `.scr`, `.pif`|
|Windows scripts|`.bat`, `.cmd`, `.ps1`, `.vbs`, `.vbe`, `.wsf`, `.wsh`|
|Unix scripts|`.sh`, `.csh`, `.ksh`, `.bash`|
|Other script or code files|`.js`, `.jsx`, `.ts`, `.tsx`, `.py`, `.pyc`, `.pyo`, `.rb`, `.pl`, `.php`, `.jar`, `.class`|
|Shortcut and link files|`.lnk`, `.url`, `.desktop`|
|Macro-enabled Office files|`.docm`, `.xlsm`, `.pptm`|

## Download status values

The agent reports every tracked download using one of the following statuses.

|Status|Meaning|
|------|-------|
|`pending`|The download has started but has not yet finished.|
|`completed`|The download finished, and the browser reported a final saved-file path.|
|`interrupted`|The download stopped before finishing. The agent does not retry it automatically.|

