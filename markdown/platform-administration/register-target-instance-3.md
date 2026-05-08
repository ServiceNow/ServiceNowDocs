---
title: IP authentication error
description: Troubleshoot a IP authentication error that occurs while registering a target instance
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Troubleshooting for registering target instance, Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# IP authentication error

Troubleshoot a IP authentication error that occurs while registering a target instance

## Condition

A failure to authenticate an IP address prevents the target instance from being registered.

## Cause

The IP address for the target instance is outside of the IP range.

## Remedy

If the target instance uses IP range based authentication, it must enable the IP range `10.0.0.0/10.255.255.255` to communicate on a local network. See IP range based authentication.

**Parent Topic:**[Troubleshooting for registering target instance](register-target-instance-troubleshooting.md)

