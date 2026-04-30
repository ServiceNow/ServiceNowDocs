---
title: Add secrets to Docker for Headless Browser setup in Microsoft Windows
description: Create a Docker secret that stores the password of the ServiceNow user who will log into the instance to execute the tests. Docker Secrets is a feature of ServiceNow for securely storing the passwords that will be used in containers.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Headless Browser setup for Microsoft Windows, Headless Browser for Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Add secrets to Docker for Headless Browser setup in Microsoft Windows

Create a Docker secret that stores the password of the ServiceNow user who will log into the instance to execute the tests. Docker Secrets is a feature of ServiceNow® for securely storing the passwords that will be used in containers.

## Before you begin

Complete Step 4: [Create the Docker image and containers for Headless Browser setup in Microsoft Windows](headless-browser-create-docker-image-containers-windows.md)

Role required: Go to your ServiceNow instance and create a new user to be used by the Docker container to log in. Give this user the roles of **admin** or **atf\_test\_admin**. Save the password to be used in Step 2 of the following procedure.

## About this task

Inside the Docker container is an automation script that opens a web browser, logs into the instance, and opens the Client Test Runner page. In order to log into the ServiceNow instance, you will need a user password. In this step you use a Docker feature called Docker Secrets so you can securely store passwords. Then when you run containers, the password is automatically available to log in to your instance.

## Procedure

1.  In the admin command line, enter `docker swarm init`

2.  In the admin command line, enter `echo <your user's password> | docker secret create sn_password -`

    **Note:** Replace `<your user's password>` with the user's ServiceNow password.

    Your results should look like this:

    ![Results of entering echo "my password" code](../image/echo-password.png)


## Result

The result is your secret ID, which you must save for later use. The secret ID will be added to the ServiceNow instance in the sys\_property `sn_atf.headless.secret_id`.

**Parent Topic:**[Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md)

**Previous topic:**[Create the Docker image and containers for Headless Browser setup in Microsoft Windows](headless-browser-create-docker-image-containers-windows.md)

**Next topic:**[Set up instance for Headless Browser in Microsoft Windows](headless-browser-instance-setup-windows.md)

