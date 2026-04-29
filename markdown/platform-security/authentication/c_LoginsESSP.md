---
title: Logins and the employee self-service portal
description: The system keeps track of the first starting page that a user is trying to access even if the user wants to log in to the Employee Self-Service Portal.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Define login scenarios, Local authentication, Authentication, Access Management]
---

# Logins and the employee self-service portal

The system keeps track of the first starting page that a user is trying to access even if the user wants to log in to the Employee Self-Service Portal.

Consider the following scenarios.

Example 1:

1.  A user is not logged in, and then tries to access a record using a specific SYS ID in the URL.
2.  The system redirects the user to the login page.
3.  Rather than logging in, the user tries to access another site, such as the Employee Self-Service \(/ess\) Portal.
4.  The system redirects the user to the login page again.
5.  The user logs in and is redirected to the record that the user was first trying to access rather than the Employee Self-Service Portal.

Example 2:

1.  A user is not logged in, and then tries to access a record using a specific SYS ID in the URL through the Employee Self-Service \(/ess\) Portal.
2.  The system redirects the user to the login page.
3.  Rather than logging in, the user tries to access another record through the Employee Self-Service Portal.
4.  The system redirects the user to the login page again.
5.  The user logs in and is redirected to the first record rather than the second.

