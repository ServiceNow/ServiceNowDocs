---
title: AI Suites versions
description: The Application Manager uses AI Suites versions to verify compatibility between multiple generative AI applications in one instance.Some AI applications are part of multiple AI Suites because they're compatible with multiple other AI application versions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-suites-app-mgr.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Install AI plugins in AI Admin Hub, Configuring plugins and skills in AI Admin Hub, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# AI Suites versions

The Application Manager uses AI Suites versions to verify compatibility between multiple generative AI applications in one instance.

## AI Suites overview

AI applications often function interdependently, which can result in runtime errors when one AI application is dependent on a specific version of another one. AI Suites help reduce runtime errors by bundling compatible versions of AI applications together. AI Suites versions are independent from the application versions that they contain.

The Application Manager uses AI Suites versions to verify compatibility between every new AI application version you install and all AI application versions already present on your instance. This verification happens when installing new applications for the first time and when updating application versions. The installation details for AI applications enable you to select an AI Suites version and review which applications, if any, need to be updated or procured for suite compatibility.

An AI application version might be included in multiple AI Suites versions based on its compatibility with other applications. When you install or update an AI application, you can choose any AI Suites version that the application is compatible with. Based on the AI Suites version you choose, multiple applications might be updated.

## Example: Install an AI Suites version

Some AI applications are part of multiple AI Suites because they're compatible with multiple other AI application versions.

**Note:** The following examples are for illustrative purposes only. They might not reflect actual AI Suites versions. For details about available AI Suites versions and their compatibility with ServiceNow AI Platform versions, see [Now Assist Suite release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-now-assist-suite-release-notes.html).

Assume that you want to install ServiceNow Otto for ITSM for the first time. You have the following AI applications installed on your instance already:

-   ServiceNow Otto for ITOM \(version 1.5.0\)
-   ServiceNow Otto for Creator \(version 27.1.1\)

When you start to install ServiceNow Otto for ITSM, you can select different AI Suites versions based on the versions of ServiceNow Otto for ITSM that are compatible with your instance. You can choose from AI Suites 4.0.0, 3.0.0, or 2.0.0.

### AI Suites 4.0.0

The latest available AI Suites version is selected by default. The following information is displayed when AI Suites version 4.0.0 is selected:

|AI application|Version|Status|
|--------------|-------|------|
|ServiceNow Otto for ITSM|9.0.1|Will be installed|
|ServiceNow Otto for ITOM|2.0.3|Will be updated|
|ServiceNow Otto for Creator|27.2.2|Will be updated|

AI Suites version 4.0.0 includes the latest versions of ServiceNow Otto for ITSM, ServiceNow Otto for ITOM, and ServiceNow Otto for Creator.

If you want to update to the latest version of ServiceNow Otto for ITSM and ServiceNow Otto for ITOM now, AI Suites version 4.0.0 could be a good option.

**Note:** Test application updates in a non-production environment to verify expected functionality before making updates in production instances.

### AI Suites 3.0.0

The following information is displayed when you select AI Suites version 3.0.0:

|AI application|Version|Status|
|--------------|-------|------|
|ServiceNow Otto for ITSM|9.0.1|Will be installed|
|ServiceNow Otto for ITOM|2.0.2|Will be updated|
|ServiceNow Otto for Creator|27.2.2|Will be updated|

AI Suites 3.0.0 includes the latest version of ServiceNow Otto for ITSM \(9.0.1\). It also includes a newer \(but not the latest\) version of ServiceNow Otto for ITOM and the latest version of ServiceNow Otto for Creator.

ServiceNow Otto for ITSM version 9.0.1 and ServiceNow Otto for Creator version 27.2.2 are both in AI Suites 3.0.0 and 4.0.0. The difference between AI Suites versions 3.0.0 and 4.0.0 are the versions of ServiceNow Otto for ITOM that are available. Which version of ServiceNow Otto for ITOM you want can help you decide between updating to AI Suites 3.0.0 or 4.0.0.

### AI Suites 2.0.0

The following information is displayed when you select AI Suites version 2.0.0:

|AI application|Version|Status|
|--------------|-------|------|
|ServiceNow Otto for ITSM|8.0.0|Will be installed|
|ServiceNow Otto for ITOM|1.5.0|Up to date|
|ServiceNow Otto for Creator|27.1.1|Up to date|

AI Suites 2.0.0 includes versions of ServiceNow Otto for ITOM and ServiceNow Otto for Creator that are already installed on your instance. The latest version of ServiceNow Otto for ITSM isn't part of AI Suites 2.0.0, but a previous version \(8.0.0\) is.

In this case, you can choose to install the older version of ServiceNow Otto for ITSM, and not update your other AI applications yet.

**Note:** Not updating the AI Suites version might not be an option. Depending on compatibility of a new AI application, you might have to update your AI Suites version to complete installation.

