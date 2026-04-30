---
title: Associating locations to consumer profiles
description: By enabling relationships between consumer profiles and locations across industries such as Financial Services Operations, Healthcare and Life Sciences, and Public Sector Digital Services Core, multiple consumer profiles can be associated with their corresponding addresses in the Customer Service Management \(CSM\) application.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Creating multiple consumer profiles for a user, Configure consumers, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Associating locations to consumer profiles

By enabling relationships between consumer profiles and locations across industries such as Financial Services Operations, Healthcare and Life Sciences, and Public Sector Digital Services Core, multiple consumer profiles can be associated with their corresponding addresses in the Customer Service Management \(CSM\) application.

## Overview

Individual consumer profiles can be associated with multiple locations, or multiple consumer profiles can be linked to the same location by using consumer profile locations. That means that different industries can associate consumer profiles with multiple locations and location types. The Customer Service Management \(CSM\) application supports the consumer profile \(sn\_csm\_consumer\_profile\) table with a reference to the consumer \(csm\_consumer\) table that helps to define and support consumer profiles.

## Use case

For example, in the Healthcare and Life Sciences industry, clinicians must be able to store multiple addresses for patients, like mailing addresses for sending reports and home addresses for sample collections. Similarly, in the Financial Services Operations industry, financial institutions must store multiple addresses, such as mailing addresses for important documents and work addresses for billing purposes, for their customers.

In some scenarios, business-to-consumer \(B2C\) customers may have multiple addresses that can be used across their profiles for various purposes, serving as distinct addresses. For example, a customer's address could function as a shipping address for a Financial Services Operations profile, while simultaneously serving as a billing address for a Healthcare and Life Sciences profile.

**Related topics**  


[Associate an existing consumer location with a consumer profile](../task/assoc-existing-consumer-loc.md)

[Create and associate a location to a consumer profile](../task/creating-loc-and-assoc-to-consumer-profile.md)

