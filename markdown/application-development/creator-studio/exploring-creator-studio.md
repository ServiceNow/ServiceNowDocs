---
title: Exploring Creator Studio
description: Creator Studio makes creating apps easier by dividing their creation into simple steps. In this section, we'll explain each one.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Exploring Creator Studio

Creator Studio makes creating apps easier by dividing their creation into simple steps. In this section, we'll explain each one.

All the steps involve requests. So, we'll start by explaining how Creator Studio stores requests.

**Summary:** After reading this section, you'll understand:

-   How requests are stored
-   How people enter requests
-   How your app automatically does things

## Let's talk about storing requests

When people make a request, we have to store it somewhere so someone can review it later.

**Tables hold requests**

Creator Studio stores requests in a table. Each row in that table is a request. Here's a simplified version of a table with three requests.

**Use cases:**

-   My monitor stopped working. I need a new one.
-   I'm requesting a new mouse so I can have one at home and in the office.
-   My laptop is over four years old. I want to request a replacement.

**People enter requests using forms**

How do people enter requests that eventually get stored in the app's table? They use your app to fill out a form. The questions on the form contain the information your fulfiller needs.

In our app's table, questions are stored as part of the [record](creator-studio-glossary.md#), which is composed of all the information on the form.

|Request|Name|Email|Request date|
|-------|----|-----|------------|
|I need a new monitor.|Sushma Singh|SushmaSingh@example.com|04-05-2024|
|I need a new laptop.|Peter Smith|PeterSmith@example.com|05-01-2024|

In this example, the form has four fields:

-   Request
-   Requester's name
-   Requester's email address
-   Request date

These fields contain all the info the reviewer needs to accept or reject the request. You'll have to figure out all the information your reviewer needs to make a decision. Later, we'll show you how to create a form \(using Now Assist or on your own\) in the section [Working with forms in Creator Studio](creator-studio-work-with-forms.md).

**Key terms:**

-   **Requester**

    Someone requesting something, like a piece of equipment or permission to do something.

-   **Fulfiller**

    Someone who works on requests. Fulfillers may also approve or deny requests, depending on any approval automation for the app.


Okay, now you understand that requesters fill out forms to create requests and Creator Studio stores those requests in the app's table.

## Try Creator Studio on a PDI

Want to play with Creator Studio on your Personal Development Instance \(PDI\)? It comes automatically installed from the Application Manager on your PDI. For more information, see [Personal developer instance guide](../../applications/concept/personal_developer_instance_guide.md).

