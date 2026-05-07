---
title: Triaged instance data
description: You can triage your instance to get instant information on transactions, jobs, nodes utilization, semaphores, schedulers and update sets. Minimal use of this feature is recommended as use of this consumes resources on your instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Triage a ServiceNow instance, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Triaged instance data

You can triage your instance to get instant information on transactions, jobs, nodes utilization, semaphores, schedulers and update sets. Minimal use of this feature is recommended as use of this consumes resources on your instance.

**Note:** Triage as a feature is for all markets and all tiers – Guided, Advanced, and Total.

## Transactions

The transactions widget breaks down the transactions into their current execution duration. You can click **View Details** to get a comprehensive list of transactions. You can sort by age or search for a specific transaction. You can also access a particular transaction in the syslog transaction table by clicking the linked Transaction ID.

## Jobs

The jobs widget breaks down the jobs into their current execution duration. You can click **View Details** for a comprehensive list of jobs. You can also sort by age or search for a specific job.

## Servlets

Use Servlets widget to learn more about your instance’s nodes. The servlets widget displays information about the servlets currently serving the instance, including their names, start times, and the amount of heap and meta space they are using in comparison to what is available. This widget allows you to evaluate the distribution of activity among your nodes.

## Schedulers

The schedulers widget allows you to gain insight into your schedulers by providing a detailed list that includes the number of jobs being executed, the number of worker nodes assigned to a node, the number of workers currently in use, the average age of the queue, and the total number of queues. Use this widget to identify the most heavily used nodes within your instance.

## Semaphore Sets

The semaphore sets widget lists the utilization of various semaphores available on specific nodes within your instances at the time when triage was executed. You can click on hyperlinked node name to gain more insight to a specific node and the transactions in-flight during the time of triage.

## Update Sets

The update sets widget lists all the updates that are applied in the past 24 hours and their completion state. Use this widget to gain insight of any updates that may be responsible to new features or performance changes within your instance.

**Parent Topic:**[Triage a ServiceNow instance](../task/io-triage-sn-instance.md)

