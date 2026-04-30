---
title: Requested restricted caller access \(RCA\)
description: You can use a requested RCA to grant store apps access to protected resources in the ServiceNow AI Platform without the need to wait for the next family release. If you have the system admin or application admin role, you can review requested RCAs and approve and deny them.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Requested restricted caller access \(RCA\)

You can use a requested RCA to grant store apps access to protected resources in the ServiceNow AI Platform without the need to wait for the next family release. If you have the system admin or application admin role, you can review requested RCAs and approve and deny them.

RCAs are classified into two categories:

-   Real RCA: sys\_scope==target\_scope
-   Requested RCA: sys\_scope!=target\_scope

For example: A real RCA record is where the application scope and target scope match. A requested RCA is a record that is still awaiting approval for access to the target scope.

When you install an application, your scheduled jobs generate RCA records with the status of Requested in the target application for each requested RCA record that is packaged in the source application.

**Note:** The jobs are generated once Upgrade Summary has run.

## Example of how a store app accesses a table

Let's say that a store app called HR Integrations Framework wants to access an HR Core Case table. The table is in the business rule called Find Case in the Integration Service table.

To request access, the HR Integrations Framework app requires that an RCA privilege is packaged in its own scope as follows:

-   sys\_scope = HR Integrations Framework
-   target = HR Core Case
-   status = Allowed
-   target\_scope = Human Resource: Core
-   source = Find Case

## App development example for developers

When you are developing an application, real RCAs are generated with the status of Requested when the target has a caller restriction. If the target has caller tracking, the status becomes Allowed. The developer can review and finalize all the real RCA records that are required for the application to work. For example, those RCAs with a status of Allowed.

A developer can click the **Generate RCA Privileges in Current App** in the related links to generate requested RCAs that are packaged in the current application. Requested RCAs are synchronized with real RCAs, which means that if a real RCA is updated or deleted, a requested RCA is updated or deleted too.

Now, the HR Integration Framework application can be packaged and installed on a customer instance.

## App installation example for administrators

When you are installing an app on a customer's instance, real RCAs are generated in the target application. A real RCA would have the Human Resource: Core with a status of Requested. This process is done asynchronously in a scheduled job, where some lag time can occur.

To notify the target app admin about an RCA's pending review, messages have been added to application pages. An example is as follows:

![RCA pending review message on application page.](../image/rca-pending-review.png "RCA pending review message")

## Store App backward compatibility

If a store app is compatible and can be installed on an instance that is pre-Rome, then you must package the RCA records in their own scope with the status of Allowed.

**Note:** This process ensures that the store app works on all versions.

When upgrading to Rome, you can configure a one-time fix script to move RCAs in the source scope to the target scope. In Rome, if the target app already has the necessary RCA records, no RCA records are generated for the RCAs that are packaged by the source app.

