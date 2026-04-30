---
title: Use filters to limit the number of results
description: One way to make your web service calls fit within the 250 record limit is to think about the design of your integrating application.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Strategies, Record retrieval limitations, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Use filters to limit the number of results

One way to make your web service calls fit within the 250 record limit is to think about the design of your integrating application.

For example, let's assume that we are making an incident form in C\# to show a user the incidents that are assigned to him.

## Problematic query approach

The C\# application makes a soap call to retrieve all of the incidents within ServiceNow. The application would then store the results locally in memory. When the user decides to view the incidents that are assigned to him, the application loops the internal array and displays the incidents that are assigned to the user.

## A better query approach

The C\# application makes a soap call to retrieve all of the incidents within ServiceNow that are assigned to the logged-in user. The results are stored locally in memory. When the user decides to view the incidents that are assigned to him, the application shows all the results to the user.

## A performance-optimized query approach

The C\# application makes no SOAP call initially. When a logged-in user decides to view the incidents that are assigned to him, the application presents him with the choice of viewing active, closed, etc. It gives him the ability to filter the results that he wants to see before the SOAP call is even made. Then, the user is only presented with the results that he wished to view.

**Parent Topic:**[SOAP strategies](../concept/c_SOAPStrategies.md)

