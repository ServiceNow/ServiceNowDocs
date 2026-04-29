---
title: Add secrets to Docker for Headless Browser setup in Linux
description: Create a Docker secret, which stores the password of the ServiceNow user who will log into the instance to execute the tests. Docker Secrets is a feature of ServiceNow for securely storing the passwords that will be used in containers.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Headless Browser setup for Linux, Headless Browser for Automated Test Framework, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Add secrets to Docker for Headless Browser setup in Linux

Create a Docker secret, which stores the password of the ServiceNow user who will log into the instance to execute the tests. Docker Secrets is a feature of ServiceNow® for securely storing the passwords that will be used in containers.

## Before you begin

Complete Step 3: [Create the Docker image and containers for Headless Browser setup in Linux](headless-browser-create-docker-image-containers.md)

Role required: none.

## About this task

Inside of the Docker container is an automation script that opens a web browser, logs into the instance, and opens the client test runner page. In order to log into the ServiceNow instance, you will need a user password. In this procedure you use a Docker feature called **Docker Secrets** so you can securely store passwords. When you run containers, the password is automatically available to log in to your instance.

Role required: admin on your ServiceNow instance and local administrator on the host machine.

## Procedure

1.  At the command line, enter `docker swarm init`

2.  Enter `echo "<your user's password>" | docker secret create sn_password -`

    **Note:** Replace `<your user's password>` with the user's ServiceNow password.

    Your results should look like this:

    ![Results of entering echo "my password" code](../image/echo-password.png)


## Result

The result is your secret ID, which you must save for later use. The secret ID will be added to the ServiceNow instance in the **sys\_property** `sn_atf.headless.secret_id`.

**Parent Topic:**[Headless Browser setup for Linux](../concept/headless-browser-procedure-linux.md)

**Previous topic:**[Create the Docker image and containers for Headless Browser setup in Linux](headless-browser-create-docker-image-containers.md)

**Next topic:**[Set up instance for Headless Browser in Linux](headless-browser-instance-setup.md)

