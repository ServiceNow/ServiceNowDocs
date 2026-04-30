---
title: Connect to Jenkins using API token authentication
description: Connect to Jenkins using API token authentication instead of user name and password.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Connect to Jenkins using API token authentication

Connect to Jenkins using API token authentication instead of user name and password.

## Before you begin

Role required:

-   Jenkins: admin or any user with overall Read and Job Read roles

## About this task

You can have multiple active API tokens at the same time and track the usage of your tokens. You can also revoke API tokens as needed. You can also use the Jenkins API token for authentication when you're using the Jenkins CLI.

## Procedure

1.  In the Jenkins banner frame, select your user name to open the user menu.

2.  Select **Security**. ![Security page for a Jenkins user](../image/jenkins-add-api-token.png)

3.  In the Security page, select **Add new Token**.

4.  Select **Generate**.

5.  Copy the API token that is generated

    **Note:**

    -   Regenerate the tokens every 6 months \(depending on your context\). Jenkins displays an indicator concerning the age of the token
    -   Use a different token for each application so that if an application is compromised you can revoke its token individually.
    -   If your token expires, regenerate the token and update it in the ServiceNow AI Platform instance
    -   ServiceNow DevOps DevOps does not support using Legacy API Tokens because Jenkins does not recommend the use of Legacy API Token. For more information, see the [Jenkins blog post](https://www.jenkins.io/blog/2018/07/02/new-api-token-system/).

