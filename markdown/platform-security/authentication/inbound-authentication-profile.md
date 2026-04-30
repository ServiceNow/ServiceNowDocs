---
title: REST API access policies
description: REST API access policies allow you to restrict access to inbound REST APIs based on the authentication type and the specified filter criteria of the access policy.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [API access policy, Authentication, Access Management]
---

# REST API access policies

REST API access policies allow you to restrict access to inbound REST APIs based on the authentication type and the specified filter criteria of the access policy.

A REST API, also known as RESTful API is a type of application programming interface \(API\) that adheres to the guidelines of REST architectural style. REST APIs provide a high degree of flexibility making it prevalent across the web.

Filter criteria contains filter conditions or queries that are used as policy inputs for an authentication policy.

You can configure the default Global Blocking Policy or create a custom API access policy according to your security requirements. For example, you can create a custom API access policy that allows only OAuth 2.0 authentication type from a specified range of IP addresses. Authentication requests of other authentication types and access requests from IP addresses other than the specified IP addresses are denied.

