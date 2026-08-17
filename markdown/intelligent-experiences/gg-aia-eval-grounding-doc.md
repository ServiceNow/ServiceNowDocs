---
title: General guidelines for AI voice agent evaluation grounding
description: Guidelines for writing effective grounding documents to generate scenarios for automated testing of AI voice agents and assistants.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gg-aia-eval-grounding-doc.html
release: australia
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 6
breadcrumb: [Getting started, Evaluate, Evaluate agentic AI assets, AI Agent Studio, Enable AI experiences]
---

# General guidelines for AI voice agent evaluation grounding

Guidelines for writing effective grounding documents to generate scenarios for automated testing of AI voice agents and assistants.

## Overview of AI voice agent evaluation grounding documents

A grounding document gives the data-generation pipeline the context it needs to create realistic test-call scenarios. It explains what the agent should handle, what it should avoid, and what “correct” behavior looks like. The goal is to make synthetically generated conversations closely match real caller scenarios, so the resulting evaluations are meaningful and reliable.

None of the sections are strictly required, but they build on each other. The more of them your document covers, the more realistic and thorough the generated test scenarios will be.

An example of a grounding document can be downloaded from the guided setup for an AI voice agent.

## AI voice agent grounding

For best results, work through the sections in order.

1.  **Start with a short summary.**

    In three or four sentences, say who the agent is, what starts it, and its goal. Also add what it does not do.

    **Example:** “This is a voice agent that files new support tickets. It starts when a caller says they want to report a problem. It takes down the issue, asks a few questions, files the ticket, and reads back the ticket number. It does not look up old tickets, and it does not try to fix the problem.”

2.  **Set the scene: company and policy context.**

    Give the background that makes generated test calls sound real and that some of your rules depend on. Two things to include:

    -   **The environment.** Who uses the agent and where, including the kind of organization, its size, the sites or regions, and the sorts of roles that call in. This is what lets the system generate callers who will act like your real users.

    -   **The rules it must honor.** Any policy, compliance, or legal requirement the agent must follow and the consequence of breaking it. Keep this separate from ordinary “can’t” items, because they usually carry more weight and are worth testing on their own.

    **Example:** “Callers are employees across several regional offices. By policy, the agent may only file a ticket for the person who called, not on someone else’s behalf, and all calls are recorded for quality review.”

3.  **List what’s in and out of scope.**

    Make two lists: the things the agent handles, and the things it doesn’t. For every out-of-scope item, say where the request should go instead: transfer to a person, hand to another agent, and so on.

    **Example:** “If the caller asks to reset a password, the agent declines and offers to transfer them to the password reset line.”

4.  **Spell out what it can and can’t do.**

    Two short lists: what the agent is allowed to do, and what it must never do. Write each “can’t” as a specific action.

5.  **Explain any decisions the agent makes silently.**

    If your agent decides something behind the scenes, how urgent an issue is, which category it belongs in, write down the exact rule it should follow, and what to do when there’s no clear signal.

    **Example:** “If the caller says, ‘I can’t work’ or ‘everything is down,’ mark it high urgency. If there’s no clear signal either way, default to medium.”

6.  **Quote anything the agent says out loud.**

    For fixed phrases such as greetings, signoffs, or the exact wording when it declines something, write the words exactly as the agent should say them, in quotes. The evaluation checks the agent said the right thing, so it needs the right words to compare against.

7.  **Show the mistakes to watch for.**

    List the specific wrong behaviors, each with a short example of what “wrong” looks like.

8.  **Provide real examples with the expected answers.**

    Give a set of sample requests, and for each one, fill in what the correct result should be, including the category, urgency, and details the agent should capture.

9.  **Define the possible outcomes.**

    List the ways a conversation can end such as ticket filed, transferred to a person, and caller hung up. A short, fixed list of outcomes lets you count results across a whole test run \(for example, “94% filed, 6% transferred”\).

10. **Include one ideal conversation.**

    Write out one full example call from greeting to sign-off, exactly as it should go. This shows the system the shape and tone you’re after and doubles as a benchmark to compare against.


## Voice Assistant grounding

With an assistant, the main thing you’re checking is whether it sent each request to the right agent.

1.  **List every place a request can go.**

    Write out each agent the assistant can route to, its name, what makes the assistant choose it, one line on what it handles, and where it hands off if it can’t.

2.  **List the types of requests and how to tell them apart.**

    Name every kind of request the assistant recognizes \(including “none of the above”\). Then, for any two that are easy to confuse, write down the rule for telling them apart.

3.  **Map requests to the right destination.**

    A table that says, for each situation, where the request should go, and which agent handles it.

    |When the caller…|Send it to…|
    |----------------|-----------|
    |reports a new problem|the ticket-filing agent|
    |asks about an existing ticket|the ticket-lookup line|
    |asks to reset a password|the password reset line|
    |wants to report phishing|the security reporting tool|
    |asks for two things at once|each request in turn|
    |says something unclear|a clarifying question first, then route|
    |asks for something unrelated|a polite decline|

    Replace these rows with your assistant’s real capabilities. This table is an example.

4.  Any section applicable for AI voice agents can be also added to this section if the voice assistant requires that information.


## Advanced context \(optional\)

-   **Tool signatures of the agent – only applicable for Voice Agent**

    List the tools the agent can call, and for each: its name, a one-line description of what it does, its input parameters \(name, type, whether required\), and what it returns.

-   **Reference or seed data**

    Provide representative data the generated calls can draw on. Real values make scenarios specific and let the evaluation check exact matches. Use synthetic or masked data only; do not include PII.

-   **Error handling \(agent behavior on failure\)**

    Describe how the agent should behave when something goes wrong mid-call. State what the agent should say, whether it retries, and where it hands off. This lets the pipeline generate failure-path scenarios and check the agent degrades gracefully instead of only testing the happy path.

    **Example:** “If file\_ticket fails, the agent says ‘I’m having trouble filing that right now,’ apologizes, and offers to transfer to a live agent. It does not invent a ticket number.”

-   **Conversation length or max turns**

    State the expected and maximum length of a call, in turn or in scope of tasks. This bounds the shape of generated scenarios and defines when a conversation should wrap up or escalate rather than looping. Note any rule for ending a call that has run too long.

    **Example:** “A typical call is 6–10 turns. If the agent hasn’t gathered enough to file a ticket after ~12 turns, it summarizes what it has and offers to transfer.”


