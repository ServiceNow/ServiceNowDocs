---
title: Group and find records using tags in workspace
description: Add tags to records to group and organize them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/setting-record-tags-agent-workspace.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working on records in your Workspace, Use, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Group and find records using tags in workspace

Add tags to records to group and organize them.

## Before you begin

Role required: agent

## About this task

Tags are labels you can add to records. The tag icon \(\[Omitted image "tag-outline.png"\] Alt text: No tag icon\) appears next to the primary value in the form header.

\[Omitted image "tag-in-form-header.png"\] Alt text: Tag in form header

Tags enable you to group and organize records. You create the tag name, which should name the reason for the tag. You can make the tags visible to everyone, some people, or just yourself. The visibility setting specifies who can use the tags to search for records.

An unfilled tag icon \(\[Omitted image "tag-outline.png"\] Alt text: No tag icon\) means that no tags have been assigned to the record. When tags are assigned and they're visible to you, the tag icon is filled \(\[Omitted image "tag-fill.png"\] Alt text: Tag icon with tags\).

After tagging records, you can use the tags to search for records in the [global search field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/search-workspace.md) or using the filter icon \(\[Omitted image "filter-outline.png"\] Alt text: Filter icon\) in List view.

\[Omitted image "global-search-1.png"\] Alt text: Global search

## Procedure

1.  Navigate to any open record in a workspace.

    For example, click the list icon \(\[Omitted image "icon-list-view.png"\] Alt text: List icon\), click a list filter, such as **Open incidents**, and click a record.

2.  Click the Tag icon \(\[Omitted image "tag-outline.png"\] Alt text: No tag icon\) next to the primary value in the form header.

3.  In **Add Tag**, enter a tag name.

    The tag name should reveal the organization principal of the tag, for example, all records stemming from a particular incident.

4.  Click **Enter** to save the tag with the record.

    You can add more tags.

    The tag visibility setting defaults to private, which means the tag is only visible to the person who created the tag. So, only that person can use the tag to search for records labeled with that tag.

5.  To change the visibility setting of the tag, click the tag and change the **Viewable by** setting.

    \[Omitted image "edit-tag.png"\] Alt text: Edit tag view

<table id="choicetable_n2j_xn4_c3b"><tbody><tr><td id="d53569e182">

**Me**

</td><td>

Tag is visible only to the person who created the tag. Only that person can use the tag to search for records. This setting is the default.

</td></tr><tr><td id="d53569e191">

**Groups and Users**

</td><td>

Tag is visible to specific groups or users. You can specify the groups and users who can view this tag.

</td></tr><tr><td id="d53569e200">

**Everyone**

</td><td>

Tag is visible to everyone. **Note:** This visibility setting is only available to an admin or tags\_admin role.

</td></tr></tbody>
</table>    A record can have multiple tags and each can have a different visibility setting.

    \[Omitted image "tags-all-levels.png"\] Alt text: Tags with visibility settings

6.  To remove a tag from a record, click a filled tag icon \(\[Omitted image "tag-fill.png"\] Alt text: Tag icon with tags\) to open the list of tags, then click the **X** next to the tag you want to remove.

7.  Search for your tag using the [global search field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/search-workspace.md).


