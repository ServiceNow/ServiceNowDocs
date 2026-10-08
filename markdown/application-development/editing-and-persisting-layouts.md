---
title: Editing and persisting layouts
description: Configuration mode unlocks every region on a page. Each region edits and saves independently. Learn about layout ownership, persistence, and editor limitations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/editing-and-persisting-layouts.html
release: brazil
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 8
keywords: [Editing and persisting layouts, Configuration mode and regions, Each region is its own session, Layout editing as ownership, Persistence, Restore defaults deletes the row, A save ends the session, Drag preview and cross-region moves, Empty containers, Known limitations, Related]
breadcrumb: [Layout configuration, Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Editing and persisting layouts

Configuration mode unlocks every region on a page. Each region edits and saves independently. Learn about layout ownership, persistence, and editor limitations.

## Configuration mode and regions

Configuration mode unlocks every region on the page when it opens. There are no modes to enter or leave. The toolbar displays one label, **Configuration**. Each boundary on the page identifies its container type on its own tab.

A region that cannot be loaded gets no session and no canvas. The system does not display an error message. With every region loaded at once, a page with one unsupported region among four would otherwise announce a refusal the administrator never asked for. The region's outline carries the reason instead. Typically reasons for the editor not loading a region include the editor not being able to reconstruct the region or a region that contains a `<raw>` block.

## Each region is its own session

A page has several regions, and each one is a separate override row with its own baseline, pending text, and working tree. Sessions are therefore keyed `ownerTag::regionName` which is the same pair `sys_aix_page_region` is unique on. The separator is a doubled colon rather than a single one because a region name may contain `.`, `-`, and `_` but not a colon. An owner tag is a custom-element name, so a doubled colon cannot occur inside either half and the split needs no escaping.

One editor instance exists per region, built as configuration mode opens and torn down as it closes. A single active region key says which region the selection, the open menu, and any gesture in flight belong to. It is not a mode, and nothing is locked while it points at one region. Switching regions clears the selection rather than carrying a path that addresses a different tree. The system prevents switching while a drag or a resize is live.

## Layout editing as ownership

An override is a new row, and from the moment it is saved the region's layout stops taking upgrades while the widgets inside it keep taking theirs. A modal dialog displays this information before the action occurs.

The system prompts on the first edit of an unstored region, not on entry. There is no entry to gate, and asking on entry would mean one modal per region the instant the editor opened, about layouts the administrator may never touch. The first edit is the moment the consequence becomes real, because that edit is what creates the row. A region already stored is already overridden, and is never asked about.

A recording edit is held back and re-run through the same path on confirmation, so it gets the same validation and announcement it would have had. A pick-up for a drag is refused outright instead. There is nothing to replay, because where a drop goes depends on where the pointer goes next, so the administrator drags again after they have confirmed.

## Persistence

Region overrides are written to sys\_aix\_page\_region directly through the Table API, deliberately rather than through a framework service route. A region override is one field on one platform row, and the Table API already enforces the write access control.

-   `(widget, region)` is unique on the table, so a read for one region returns at most one row. An empty result indicates that the region is code-authored with no override yet and drives an insert. A thrown error means the read itself failed, and is never collapsed into "no override," so a refused read does not get reported as an absent one.
-   An insert is valid only when the read came back empty; the unique index refuses a second insert for an existing pair.
-   An update patches the existing row's **layout** field.

## Restore defaults deletes the row

The region's gear menu holds one item, and it is the inverse of taking ownership: the region stops being overridden. Confirming it stages the deletion of the region's row, so the layout the app ships stands again and takes upgrades again.

**Warning:** The action deletes the row rather than clearing the **layout** field. A row with an empty **layout** field still takes precedence over the app's shipped layout, rendering the region as empty.

A 404 response on the delete is treated as success. The row being absent is the intended outcome. The action is available whenever a row exists, regardless of whether the current session has unsaved edits. A region overridden in an earlier session opens without pending changes, which is the common case where restoring the app's shipped layout is relevant.

The deletion is staged, not applied immediately. It enables **Save** and is discarded by exiting the editor, the same as a layout edit. Staging a restore drops any staged layout text for that region. A subsequent edit drops the staged delete. Because both are writes to the same row, a save applies only the later instruction.

What is on screen follows immediately, because a staged restore that left the overridden layout rendered would be a menu item with no visible effect until a reload. Dropping the override is also what makes the default layout readable to the editor for the first time. An overridden region has no recorded default until its override goes away.

## A save ends the session

Saving persists the layout and exits configuration mode. Because every region is unlocked for the entire session, remaining after a save leaves the administrator on a page full of editing controls with nothing left to commit. Every save path exits, not only the **Save** toolbar button. When a save fails, the editor stays in its current state and displays the reason on the toolbar.

## Drag preview and cross-region moves

While a widget is being dragged, the region shows the layout the release produces. The stand-in is a real element and is the node in flight. Pick-up takes the widget out and holds its element detached, and every seam the pointer crosses moves the stand-in there using the same placement the release would use. Release swaps the widget's element back into the slot the stand-in was holding. The element that lands is the element that was picked up, so the widget keeps its state and does not re-run its loader.

A destination indicated by the pointer does not land until it has been rested on briefly. Applying a placement reshapes the region. Applied on every pointer move, a traveling pointer walked the region through every intermediate shape on the way to the one it wanted. Each of those shapes moved the boxes the administrator was aiming at. Resting first makes the aim a fixed question. A release never waits; a cancel discards.

A widget may not leave its region. A move is a path into one region's tree, committed by printing that region's text. No action in the grammar takes a node out of one region and puts it into another. It would be a delete from one stored row and an insert into a second. That means two prints, two overrides, and a widget whose **aiux-config-id** may already be taken in the destination. A drag that arrives in a different region is therefore cancelled with a banner, not merely refused in place. The alternative leaves the administrator holding a ghost over a region that cannot take it, with nothing saying so.

A pointer in the space outside all regions, such as the page margin or the gap between two regions, does not trigger a cross-region move. The system treats it as a pointer in transit.

## Empty containers

Three rules, and the difference between them is authorship rather than shape.

-   An empty column the layout arrived with is kept, and wears an **Add widget** affordance at its center. An author's empty column, or one an administrator added and has not filled, is a slot waiting for a widget.
-   A row that arrives with no columns is refused. The parser rejects a column-less row outright: nothing in it can hold a widget, so it is not a layout. A region holding one does not parse, the editor never loads it, and the region's blocked reason carries the parser's message.
-   A container this edit emptied is swept after every mutation. Every column with nothing left in it goes, then every row with no columns, bottom-up, so emptying a column can empty the row that held it. Widths go back to the line, and a wrapper left standing around nothing is unwrapped.

## Known limitations

-   A widget with no **aiux-config-id** cannot be configured. Its surface carries no pencil, only the chevron. The attribute has to be added to the region's code template, and no control writes it. An **id** written by an administrator would be an address with no rows behind it, and no way to tell it from one the author meant. Widgets the editor adds are stamped automatically.
-   Undo and redo do not cover region layout edits, and neither does any per-region revert. The undo stack is a widget-property stack. There is no step-by-step history of layout edits, and no way to drop one region's session edits while keeping another's. Exiting the editor discards every pending change at once, and "Restore defaults" is a different act.
-   Widget-internal state and scroll are lost on every structural edit. A structural change remounts every widget in the region by design; only the region's own scroll offsets are preserved. A move is the exception, because the dragged widget's element is put back rather than rebuilt. A placement that synthesizes a container still remounts the rest of the region.

