---
title: Workspace tutorial for agents starting with a record
description: Perform the steps in this tutorial to get an idea how you can use Workspace when you begin with a task already stored in the database.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Learn how to use your Workspace, Starting in your Workspace, Using Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Workspace tutorial for agents starting with a record

Perform the steps in this tutorial to get an idea how you can use Workspace when you begin with a task already stored in the database.

## Before you begin

Role required: agent

## About this task

Use Workspace to:

1.  Find a task to work on.
2.  Do research to resolve the task.
3.  Communicate the solution to the requester or enter notes for yourself and other agents that document your progress in finding a solution.

The following graphic provides a quick overview of finding and solving an issue.

![Agent overview.](../video/aw-agent-overview.gif)

## Procedure

1.  Open your workspace by selecting your Workspace from the Workspace menu.

    ![Open workspace.](../image/open-workspace.png)

    **Note:** In the previous image, you can see **Agent Workspace Home** in the application modules. You can click that to open Workspace. The following steps are for you if you're using a different workspace.

2.  Click the name of your workspace and then under Related Links, click **Open workspace**.

    Your workspace opens.

3.  Log in to your workspace.

    ![Open workspace.](../image/landing-page.png)

    The first thing to do is find out what to work on. You can do that by looking at what's on the landing page, as shown in this image. Or, you can go directly to the list of open issues to solve. Let's see how to do both.

4.  View P1 incidents that haven't been solved by clicking **Open P1 Incidents** on the landing page.

    ![Open P1 incidents.](../image/open-incidents-22.png)

    A list of P1 incidents open.

    ![Open P1 incidents.](../image/open-p1-incident-list.png)

    This display is called the List view. It's a list of records, in this case, incident records. Normally, you'd click one of the records to open it. Before you do, let's see how else you can start from a list to find a task to work on.

5.  Click the list icon \(![List icon.](../image/icon-list-view.png)\) in the left, edge menu.

    In the Lists tab, you see the groups of records you can open as lists. For example, you could open **All problems** or **All change requests**.

6.  In the Lists tab, under **Incidents**, click **Open**.

    A list of open incidents appears. Let's find out what the problem is and solve it.

7.  Click an incident.

    The record opens in what is called Record view.

    ![Record view.](../image/record-view-simple.png)

    From top to bottom, here's what to notice:

    -   This record is on a tab labeled INC000905. You can open other incidents without closing this one. How? Click the list icon \(![List icon](../image/icon-list-view.png)\) and click another incident. You can always jump from record to record by clicking the tabs.
    -   The form header shows the record's short description, "Email server is down." The form header is like the title of the incident record.
    -   Underneath that title in the form header is high-level information, including the importance of the task \(**Priority**\), whether it's been worked on \(**State**\), and the kind of incident this is \(**Category**\).
    -   On the bottom, the **Details** tab shows many details in the record. This section is called the form pane. Notice that you can scroll this section. You can enter information in this section, for example when you get additional information from the requester.
    Basically, the **Activity** pane is where you communicate with the requester or make notes to yourself or other agents about your progress in dealing with this incident. On the far side, the Contextual Side panel is where you do your research to find solutions for the task at hand.

8.  Click through the tabs next to the **Details** tab to get information related to the open record, such as the service level agreement \(Task SLAs\) for this task, continuous integrations \(Affected CIs\) that might be affected, services impacted by the incident, related incidents, outages, and so on.

    These items that work like tabs are called the Related items menu.

9.  Click **Assign to me** to work on this incident.

10. Scroll down the stack of cards in Agent assist to solve this issue.

    The stack of cards is located on the side. If you don't see a card that suggests a solution, you could enter a search term beside the search icon \(![Search icon](../image/magnifying-glass.png)\). Notice that workspace automatically entered the value of the Short Description field from the record in the search field and used that to search.

    ![Search using Agent Assist.](../image/agent-assist-search.png)

11. Click the card if It looks like the **Reboot Windows Server** card might be the solution that you want.

    Agent assist gives you the opportunity to order a reboot.

    ![Reboot option.](../image/reboot-windows-server.png)

12. Click **Helpful** to provide guidance to the predictive intelligence software that this was a good solution for this incident.

13. Click **Order** to issue a change request to reboot the Windows server.

    Notice a new tab appears as a child tab of the same incident tab. These child tabs enable you to accomplish multiple tasks on one screen. All of the child tabs relate to the same incident, which is shown on the tab at the top.

    ![Order reboot.](../image/reboot-window.png)

14. If you were really solving this issue, you'd click **Submit** and then click the option to save the change request.

    The system would then create the change request, which someone would then perform.

15. Document what you've done.

    In **Activity**, in the **Compose** field, click **Comments** and enter a note to the requester explaining what you did.

    ![Enter a comment in Activity.](../image/enter-a-comment.png)

16. Click **Post Comments**.

    Workspace sends your comment to the requester and also adds it to the **Activity Stream**, which is the history of communications and actions you've taken.

    ![Activity stream entry.](../image/activity-stream-entry.png)

17. Click **Work notes \(Private\)**, enter a comment, and click **Post Comments** to save information that's only seen by fellow agents.

    You might use this internal commenting feature if you've not completely resolved an issue but want to document what you've done for other agents or yourself when you come back to the issue later.

18. In the form pane, scroll to the section, **Resolution Information**, and do the following.

    1.  In **Resolution code**, click on one of the choices from the menu, for example, **Solved \(Permanently\)**.

    2.  In **Resolution notes**, enter a description of your resolution.

    3.  In **Resolved by**, select your name.

    4.  In **Resolved**, select the date and time of the resolution.

        ![Fill form pane.](../image/form-pane-fill-it.png)

        This information becomes part of the record.

19. If you haven't resolved the issue but want to save your progress, click **Save**.

20. If you've resolve the issue, click **Resolved**.

    The incident no longer appears in the list of open records.


## What to do next

You've walked through finding and solving an incident that was in the database. Next, walk through [solving an issue that comes in through a phone call or a chat](workspace-tutorial-agents-chat.md).

