---
title: Writing effective stories in Agile Development 2.0
description: Well-written stories are easy to understand by all developers and members of team members, such as Testing or Documentation.
locale: en-US
release: zurich
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Agile Development 2.0, Strategic Portfolio Management]
---

# Writing effective stories in Agile Development 2.0

Well-written stories are easy to understand by all developers and members of team members, such as Testing or Documentation.

Stories enable the assignment group to accurately estimate the effort required to implement the work according to the definition of done. Definition of done is the exit criteria agreed to by the group, that determines when a story is complete.

A story has the following basic conditions:

-   Description: The story description relates to a user persona, such as administrator, and either describes a business value or addresses a technical debt.
-   Acceptance criteria: The story acceptance criteria are measurable and testable.

## Story descriptions

A good user story description identifies the following for meeting the stated requirement:

-   the role of the user persona in the system
-   the need expressed by the user persona
-   the benefit to all stakeholders such as developers, users, and others

Typically, a story description is expressed as: "As a &lt;role&gt;, I want &lt;goal or need&gt;, so that &lt;benefit&gt;".

-   **Examples of good story description**
    -   Description: As a developer, I want to publish the current state of my application to an update set, so that I can deploy it to a production system.
    -   Description: As a customer, I want to receive notifications when comments are entered for an incident so that I am updated on the status.
    -   Description: As a change manager, I want to enable the assessment of risk for any given change by establishing a list of questions with multiple choice answers.
-   **Example of bad story description**

    Description: Notifications are sent when incidents are created.

    This description is poor because:

    -   The description does not state who or what is sending the notifications, not in what form the notification takes, such as email.
    -   The description does not include any benefit information, so the business value is not clear.
    It could be better written as:

    Description: As an incident creator, I want email notifications to be sent to a predefined set of interested parties when I create an incident, so that they can be informed when an incident affecting them is created.


## Story acceptance criteria

Acceptance criteria define the boundaries of a user story, and are used to confirm when the software is working as intended, which means the story is completed. Acceptance criteria are an essential part of the 'Definition of Done' for a story.

-   **Good acceptance criteria**

    Good acceptance criteria should include the following, where relevant:

    -   Usability: Be sure to include measures of usability in the acceptance criteria. Indicate how to answer the question: Is it easy to use? The key is to identify the right measurements and make sure each is quantifiable.
    -   Functionality: Identify specific user tasks, business processes, or functions that must be in place at the end of the project. A functional requirement might be: The user can choose from multiple sizes.
    -   Error handling: Enumerate error cases and how each should be handled. For example, if a user performs the steps in the wrong order, how will the software handle it?
    -   Performance: Test system performance from the perspective of an individual user. For example: Is the UI responsive?
    -   Stress tests: Describe how the system responds when it is under stress because there are many users, transactions, or queries. Acceptance criteria should define acceptable thresholds for stress testing. For example: Does the system respond within a 250-millisecond threshold when 100 users submit queries simultaneously?
-   **Example of Good Acceptance Criteria**

    Description: As a customer, I want to order and pay for the book via a secure web-based form, so that my credit card information is safe.

    Acceptance Criteria:

    -   All mandatory fields must be completed before a customer can submit a form.
    -   Information from the form is stored in the customer orders database.
    -   Payment can be made via Amex, Master Card, or Visa credit card.
    -   The system shall accurately calculate and apply sales tax.
    -   The system shall accurately calculate and apply shipping charges.
    -   The customer shall be able to verify the accuracy of the order.
    -   An acknowledgment email is sent to the customer submitting the form.
    -   Protection against spam is working.
-   **Example of Bad Acceptance Criteria**

    Description: As a customer, I want to receive notifications when an incident is commented, so that I am updated on the status.

    Acceptance Criteria: The appropriate people are notified when incidents are commented.

    The acceptance criteria are poor because they do not give enough detail to test, for example, it is not clear who the appropriate people are.

    The acceptance criteria could be better written as:

    1.  As an ESS user, create an incident.
    2.  Select **Notify interested parties**.
    3.  Save the incident.
    4.  Log in as an interested party.
    5.  Check that you have received an email for the logged incident.

**Parent Topic:**[Agile Development 2.0 reference](../reference/agile-development-2-reference.md)

