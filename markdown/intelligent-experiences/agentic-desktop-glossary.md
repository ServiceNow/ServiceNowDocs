---
title: Agentic Desktop glossary
description: Learn about the terms and concepts that are unique to Agentic Desktop.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, Agentic Desktop, AI Desktop Agents, AI Desktop Actions, glossary terms, Agentic Desktop, AI Desktop Agents, AI Desktop Actions]
breadcrumb: [Reference, Agentic Desktop, Enable AI experiences]
---

# Agentic Desktop glossary

Learn about the terms and concepts that are unique to Agentic Desktop.

**Parent Topic:**[Agentic Desktop reference](agentic-desktop-reference.md)

## A

Glossary terms are grouped alphabetically.

### Action recorder

Recording feature in the Design workspace that auto-captures user interactions with desktop applications to create automated workflows. The recorder captures clicks, keystrokes, data entry, and visual and contextual information as screens and steps.

### AI agent

Set of large language model \(LLM\) instructions and tools in AI Agent Studio that can process natural language inputs, generate execution plans, and run desktop actions autonomously or semi-autonomously.

### AI Agent Studio

ServiceNow platform interface for creating, managing, testing, and activating AI agents. Desktop actions are published to AI Agent Studio as tools that AI agents can use during execution.

### Anchor

Reference point on a captured screen that helps the automation identify and interact with nearby UI elements. During execution, the system uses computer vision to locate the anchor and then identifies UI elements at a relative distance from it. Anchors improve the stability and accuracy of steps when the target element location may shift or when the UI layout varies across sessions.

### Auto-capture

Method of creating desktop actions by recording user interactions with desktop applications using the Action recorder. The recorder captures clicks, keystrokes, and data entry along with visual and contextual information.

## C

Glossary terms are grouped alphabetically.

### Confidence threshold

Accuracy level required for matching a captured image before the system performs a step. A value of 1 defines a 100% match while 0.5 defines a 50% match. The default value is 0.95 \(95% match\).

## D

Glossary terms are grouped alphabetically.

### Design workspace

Interactive no-code environment within Agentic Desktop for creating, configuring, managing, and testing desktop actions. The workspace provides a visual canvas where you can design multi-screen automation workflows that capture business processes across different applications. Accessible to users with the AI Agent Admin \(sn\_aia.admin\) role.

### Desktop action application

Record that stores the association between a desktop action and the desktop application it interacts with. Stored in the Desktop action application \[sn\_desktop\_core\_action\_application\] table.

### Desktop action

Reusable automation that defines how AI agents interact with desktop applications. Desktop actions consist of screens, anchors, and steps. There are two types: UI block and non-UI block.

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

### Non-UI block

Type of desktop action that uses pre-built connectors to interact with applications and system components in the background without UI interaction. Supported applications include Microsoft Excel, Microsoft Outlook, Microsoft Word, PDF, PowerShell, SQL, SSH, and System Actions. Non-UI block actions can't be created by users.

### Now Assist panel

ServiceNow interface from which users trigger AI agent automations. When you provide instructions through the Now Assist panel, the AI agent selects and runs the appropriate desktop actions in the Execution workspace. Accessible to users with the Now Assist panel user \(now\_assist\_panel\_user\) role.

## P

Glossary terms are grouped alphabetically.

## S

Glossary terms are grouped alphabetically.

### Screen

Captured image of an application window within a desktop action. Screens represent the application states that the automation moves through during execution. Each screen contains one or more anchors and associated steps.

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

## U

Glossary terms are grouped alphabetically.

### UI block

Type of desktop action that simulates human interactions with UI elements on thick client applications, legacy systems, or SaaS applications without APIs. Interactions include clicking buttons, entering text, and selecting from menus. UI block actions are created and managed in the Design workspace.

