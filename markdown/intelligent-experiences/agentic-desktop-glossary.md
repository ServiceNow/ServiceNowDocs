---
title: AI Desktop Actions glossary
description: Learn about the terms and concepts that are unique to AI Desktop Actions.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
keywords: [glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions]
breadcrumb: [Reference, AI Desktop Actions, Enable AI experiences]
---

# AI Desktop Actions glossary

Learn about the terms and concepts that are unique to AI Desktop Actions.

**Parent Topic:**[AI Desktop Actions reference](agentic-desktop-reference.md)

## A

Glossary terms are grouped alphabetically.

### Action recorder

Recording feature in the Design workspace that auto-captures user interactions with desktop applications to create automated workflows. The recorder captures clicks, keystrokes, data entry, and visual and contextual information as screens and steps.

### Adaptive path desktop action

A type of desktop action in which the AI agent dynamically determines the steps required to complete a task based on a high-level goal you provide in the tool configuration. Unlike defined path desktop actions, adaptive path desktop actions do not follow a fixed sequence of steps. Instead, the AI agent checks the current state of the web page and adjusts its approach at runtime. Because steps are determined dynamically, results may vary between runs of the same task.

Example: Reviewing an open incident and routing it based on its current priority level, where the next steps depend on the value the AI agent finds on the page.

### AI agent

Set of large language model \(LLM\) instructions and tools in AI Agent Studio that can process natural language inputs, generate execution plans, and run desktop actions autonomously or semi-autonomously.

### AI Agent Studio

ServiceNow platform interface for creating, managing, testing, and activating AI agents. Desktop actions are published to AI Agent Studio as tools that AI agents can use during execution.

### Anchor

Reference point on a captured screen that helps the automation identify and interact with nearby UI elements. During execution, the system uses computer vision to locate the anchor and then identifies UI elements at a relative distance from it. Anchors improve the stability and accuracy of steps when the target element location may shift or when the UI layout varies across sessions.

### Auto-capture

Method of creating desktop actions by recording user interactions with desktop applications using the Action recorder. The recorder captures clicks, keystrokes, and data entry along with visual and contextual information.

## B

Glossary terms are grouped alphabetically.

### Background task

Type of desktop action that uses prebuilt connectors to interact with applications and system components in the background without UI interaction. Supported applications include Microsoft Excel, Microsoft Outlook, Microsoft Word, PDF, PowerShell, SQL, SSH, and System Actions. Background task desktop actions can't be created by users.

## C

Glossary terms are grouped alphabetically.

### Confidence threshold

Accuracy level required for matching a captured image before the system performs a step. A value of 1 defines a 100% match while 0.5 defines a 50% match. The default value is 0.95 \(95% match\).

## D

Glossary terms are grouped alphabetically.

### Defined path desktop action

Reusable automation that defines how AI agents interact with desktop and web applications. Desktop actions consist of screens, anchors, and steps. There are two types: On-screen task and Background task. For this desktop action, you design a fixed sequence of steps in the AI Desktop Actions Windows application. The AI agent executes these steps in the order you specified, without deviation. Defined path desktop actions support both desktop applications and web-based applications, and do not require Google Chrome or a browser extension.

Use defined path desktop actions for tasks that follow the same sequence every time and involve predictable UI interactions. Contrast with adaptive path desktop actions.

Example: Automatically entering shipping data into a shipping management application using a fixed form structure that does not change between executions.

### Design workspace

Interactive no-code environment within Agentic Desktop for creating, configuring, managing, and testing desktop actions. The workspace provides a visual canvas where you can design multi-screen automation workflows that capture business processes across different applications. Accessible to users with the AI Agent Admin \(sn\_aia.admin\) role.

### Desktop action application

Record that stores the association between a desktop action and the desktop application it interacts with. Stored in the Desktop action application \[sn\_desktop\_core\_action\_application\] table.

### Desktop-in-Desktop \(DiD\) mode

Virtual environment within the Execution workspace where automations run in isolation from the main desktop session. You can monitor the execution of desktop actions and how they interact with desktop applications while continuing to work on other tasks.

### Desktop session

Isolated Windows session within the Execution workspace where desktop actions run. The desktop session launches automatically when you test a desktop action or trigger an automation from the Now Assist panel.

## E

Glossary terms are grouped alphabetically.

### Execution status

Current state of an automation in the Execution workspace. Statuses include Ready, Initiated, Running, Success, Failed, and Canceled.

### Execution workspace

Isolated desktop session where desktop actions run during testing or AI agent execution. This workspace launches automatically when you test a desktop action from the Design workspace or trigger an automation from the Now Assist panel. You do not open the Execution workspace directly.

## M

Glossary terms are grouped alphabetically.

### Manual capture

Method of creating desktop actions by taking screen captures, inserting anchors, and defining steps individually rather than recording interactions automatically.

## N

Glossary terms are grouped alphabetically.

### Now Assist panel

ServiceNow interface from which users trigger AI agent automations. When you provide instructions through the Now Assist panel, the AI agent selects and runs the appropriate desktop actions in the Execution workspace. Accessible to users with the Now Assist panel user \(now\_assist\_panel\_user\) role.

## O

Glossary terms are grouped alphabetically.

### On-screen task

Type of desktop action that simulates human interactions with UI elements on thick client applications, legacy systems, or SaaS applications without APIs. Interactions include clicking buttons, entering text, and selecting from menus. On-screen desktop actions are created and managed in the Design workspace.

## P

Glossary terms are grouped alphabetically.

### Parameter record

Record created by an AI Agent Admin that stores a reference name for credentials such as usernames or passwords. AI agents access these records during desktop action execution to retrieve sensitive values securely. Currently supported only for SSH connector, background task desktop actions.

### Parameter Value record

Child record under a Parameter record that stores the actual credential value, such as a username or password, for a specific user. Only one Parameter Value record can be created per user for each Parameter record.

## S

Glossary terms are grouped alphabetically.

### Screen

Captured image of an application window within a desktop action. Screens represent the application states that the automation moves through during execution. Each screen contains one or more anchors and associated steps.

### Smart sizing

Display feature in the Execution workspace that automatically adapts the desktop session to the display. Includes two options:

-   **Fit to window**: Scales the session to fit within the Execution workspace.
-   **Original resolution**: Displays the session at its native resolution with scroll bars if necessary.

### Step

Individual interaction within a desktop action, such as clicking a button, entering text, or extracting data. Steps are positioned relative to an anchor.

-   Input step types include Set Text, Click, Mouse Click, and Send Keys.
-   Output step types include Get Text, Get Table, and OCR Read Text.

### Step in / Step out

Manual control options in the Execution workspace. Step in transfers control to the user for manual input such as entering an OTP or CAPTCHA. Step out returns control to the AI agent to continue the automation.

## T

Glossary terms are grouped alphabetically.

### Tool

Desktop action that has been activated and added to an AI agent in AI Agent Studio. Tools provide AI agents with the capabilities to complete specific tasks during execution. An AI agent selects a tool based on its name and description.

