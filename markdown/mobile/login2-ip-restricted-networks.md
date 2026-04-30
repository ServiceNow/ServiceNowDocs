---
title: Log in to instances on IP-restricted networks with your mobile device
description: Learn how to log in with your mobile device to a ServiceNow instance that uses adaptive authentication to restrict access based on IP addresses.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with instances, Using the mobile apps, Mobile Platform]
---

# Log in to instances on IP-restricted networks with your mobile device

Learn how to log in with your mobile device to a ServiceNow® instance that uses adaptive authentication to restrict access based on IP addresses.

## Before you begin

Role required: user

Make sure you have access to a company-provided computer to begin the registration process.

## About this task

To register your mobile device, you must begin by logging in to the ServiceNow instance using a company-provided computer. This computer should use an IP address that has access to the instance.

Registering your mobile device and your ServiceNow instance credentials with the instance, sets up a trust relationship between your profile and the instance. If more than one user must use a single mobile device, your ServiceNow instance administrator can configure that by using system properties.

## Procedure

1.  Log in to the desired ServiceNow instance using a company-provided computer and your login credentials.

2.  Select your name in the upper right and then select **Profile**.

3.  On your profile page, in the Related Links section, select **Register trusted mobile app**.

    You're presented with a validation QR code on the company-provided computer.

4.  Open the ServiceNow mobile app on your device and enter the ServiceNow instance address.

    Because the instance restricts access based on IP addresses, a Registration screen displays on your mobile device. You must establish trust with the ServiceNow instance by entering a validation secret in the form of a QR code.

5.  On your mobile device, tap **Scan the QR code** and then scan the QR code on the company-provided computer with your mobile device.

6.  Press **Submit** on your mobile device to send the validation secret to the ServiceNow instance server.

    After submitting the QR code to the instance, an instance login screen displays on the mobile device.

7.  Enter your user name and password to log in to the ServiceNow instance as usual.


