---
title: Serverless Discovery
description: Discovery can find applications on host machines without the need to discover the host first. This type of Discovery is referred to as serverless Discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Serverless Discovery

Discovery can find applications on host machines without the need to discover the host first. This type of Discovery is referred to as serverless Discovery.

Serverless Discovery relies on infrastructure patterns to explore CIs on a host. This kind of Discovery skips the [scanning and classification phases of Discovery](disco-process-flow-patterns.md). There are two types of serverless Discovery: standard and host-based. Both types require an infrastructure pattern.

## Standard serverless Discovery

Standard serverless Discovery finds remote application CIs that reside on an unknown host. This type of serverless Discovery uses protocols, such as REST or HTTP, to find the CIs. The IP address of the host machine is not required. You define input parameters in an infrastructure pattern to connect to a remote resource. Use this type of Discovery when you want to discover web-based applications.

## Host-based serverless Discovery

Host-based serverless Discovery finds CIs that reside on a host machine that you already discovered. The host acts as a proxy through which you find other CIs. You do not actually run Discovery on the host. Use this type of Discovery when:

-   You do not know the IP address of the CIs you want to discover, or the CIs do not actually have IP addresses.
-   The CIs reside on an already discovered host CI.

For this type of Discovery, you also need an infrastructure pattern, but you do not need to define input parameters like you do for standard serverless Discovery. The pattern can specify operations, such as a WMI Query, which executes queries on a host. After Discovery connects to the host, it uses the credentials of the host to perform the Discovery of CIs you are exploring in the pattern. You do not need to specify additional credentials. When you run debug mode on the pattern, you can see the details under **Temporary Variables** on the pattern. You can then create pattern operations that make API calls from the host to the CIs you are trying to discover.

## Serverless Discovery schedules

The infrastructure patterns that serverless Discovery uses are triggered from a Discovery schedule, rather than from a classifier. Serverless Discovery ignores classifiers. Use a serverless schedule type for both types of serverless Discovery. The serverless schedule allows you to specify:

-   Values for input parameters in the pattern if you are using standard serverless Discovery. See [Create a schedule for standard serverless Discovery](../task/create-pattern-for-serverless.md#) for instructions.
-   A host CI if you are using proxy-host based Discovery. See [Create a schedule for host-based serverless Discovery](../task/create-pattern-for-proxy-serverless.md#) for more information.

