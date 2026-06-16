---
title: Kanban board component release notes
description: Version history for the Kanban board component application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-ui-kanban-board-component.html
release: store
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Kanban board component release notes

Version history for the Kanban board component application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 26.0.1 - February 2026**

    Fixed an issue where refreshing a page with Kanban caused a entire tab to show blank screen.

-   **Version 26.0.0 - December 2025**
    -   This release introduces comprehensive improvements to keyboard navigation, ARIA announcements, high-contrast support, theming, and multi-select behaviour across the board and card interactions.
    -   1. Keyboard Navigation Enhancements
        -   1.1 Arrow-Key Navigation
            -   Right arrow navigation is blocked after reaching the last element in the rightmost lane.
            -   Screen reader announces: “Last work item. Right navigation blocked.”Left arrow navigation is blocked after reaching the first element in the leftmost lane.
            -   Screen reader announces: “Last work item. Left navigation blocked.”Up/Down/Left/Right arrows move focus in their respective logical directions across lanes and cards. Arrow navigation now matches the visual layout precisely for predictable movement.
    -   2. ARIA Screen Reader Improvements
        -   For both leftmost and rightmost boundaries:
            -   ARIA label reads out the card content, prefixed with:
                -   “Right navigation blocked. Last work item.” \(right boundary\) “Left navigation blocked. Last work item.” \(left boundary\)Ensures non-visual users understand navigation limits without confusion. All card content continues to be read as part of the ARIA label.
    -   3. Tab Order &amp; Focus Behavior
        -   3.1 Standardized Tab Navigation
            -   Visual tab order now matches actual DOM tab order. Tab moves focus forward; Shift+Tab moves focus backward. No positive tabindex values are used to avoid unpredictable ordering. Tab order for:
                -   Cards Lanes Drag handles Inline actionsfollows the structure defined in Figma.
        -   3.2 Focus Visibility
            -   A clear, high-contrast ≥2px focus ring is applied to all interactive elements. Focus styles are distinct from hover and selected states. Focus rings remain visible in:
                -   Light theme Dark theme Windows High Contrast ModeFocus is never hidden under sticky headers or drag overlays.
    -   4. Color, Contrast &amp; Theming Compliance All green checklist indicators validated per design.
        -   ✔ 4.1 Text &amp; Non-Text Contrast
            -   Normal text: ≥ 4.5:1 Large text: ≥ 3:1 Non-text elements: ≥ 3:1
            -   Card borders Column dividers Icons Focus rings Drag handles
            -   All thresholds met. ✔
        -   4.2 Dark Theme Enhancements
            -   Avoided pure black/white to preserve contrast:
                -   Board background: \#121212 Columns: \#1E1E1E Cards: \#262626
                -   All shadows, borders, and surfaces maintain ≥3:1 contrast.
        -   4.3 Status Colors
            -   High-contrast, theme-friendly variants added \(e.g., Success 600/200\). Status chips remain readable in both themes and forced colors.
    -   5. Windows High Contrast \(Forced Colors\) Mode
        -   5.1 Automatic Forced-Colors Support
            -   The board respects system-defined colors:
                -   color: ButtonText; background-color: ButtonFace; border-color: WindowText;No UI element disables forced color adjustments.
        -   5.2 Icons &amp; Indicators
            -   Icons/SVGs dynamically adjust to forced colors. Removed reliance on gradients and background-images that break in HCM.
        -   5.3 Drag &amp; Drop in High Contrast
            -   Dragged card displays a strong system-highlight outline. Drop targets visibly adapt to system colors.
        -   5.4 Essential Visual Indicators
            -   States are communicated via text + shape; never color alone. Priority, warnings, WIP limits, etc., all include non-color cues.
    -   6. Disabled, Inactive &amp; Read-Only States
        -   Each state is visually and programmatically distinct. Meets ≥3:1 non-text contrast ratio. States exposed correctly to screen readers.
    -   7. Keyboard Multi-Select Enhancements
        -   7.1 Multi-Select via Keyboard
            -   Multi-select now supported with:
                -   Command + Return \(Mac\) Ctrl + Enter \(Windows\)If a card is already selected:
                    -   Pressing the same shortcut again deselects it.Works consistently across:
                        -   Single card Multiple cards Cards across lanes
        -   7.2 Fully Accessible Multi-Select
            -   No mouse required. Selection state announced to screen readers.
-   **Version 25.5.0 - August 2025**
    -   Attachment Support: Files and Hyperlinks New Features Added
        -   Downloadable Files:
            -   Users can download files directly from Kanban cards.
            -   An icon appears with an associated click-to-download interaction.
        -   Hyperlinks:
            -   Clickable URLs open in a separate browser tab.
    -   Truncation and Tooltip Behavior
        -   If filename or hyperlink label exceeds visual width:
            -   Label is truncated
            -   Full content available via tooltip on hover
    -   Drag-and-Drop Experience Updates Visual Enhancements
        -   Drop Target Highlighting:
            -   Clear screen-level drop indicators added for better UX
            -   Enhanced drop zone visual cues when dragging across the board
        -   Three-Dot Menu Drag Option:
            -   Users can drag a card using the ... context menu
            -   Works for both single and multi-card selections
            -   Visual feedback shows active state of selected items
    -   Multi-Level Lane Header Support Configurable Labels in Lanes
        -   Support for up to 3 header lines per Kanban lane
        -   If more than 3 lines:
            -   Additional lines go into a Show More collapsed section
        -   Paragraphs not supported:
            -   Each line is fixed-height
            -   Longer text gets truncated with tooltip shown on hover Multi-Card Drag Feature Bulk Card Selection and Move
        -   Users can now select multiple cards \(multi-select\)
        -   All selected cards can be dragged together and dropped in a new lane
        -   Behavioral Conditions:
            -   If multiple cards are selected and dragged: lane dragging is disabled
            -   If lane is dragged \(and not the cards\):
                -   Multi-card selection is retained
                -   Cards remain selected until actioned or deselected
-   **Version 25.4.5 - February 2025**
    -   New:
        -   Ability to configure secondary header.
        -   Ability to select multiple cards for the purpose of bulk edits, drag and drop multiple selected cards.
        -   Ability to select dependency lines
-   **Version 25.0.6 - February 2024**
    -   New:
        -   Render, expand and collapse the row header
        -   Render, show and hide dependency lines between cards
        -   Configure color dependency lines
        -   Draw new dependency lines along with mouse scroll
        -   Handle dependency lines for different types of drag and drop
        -   Tweak hover styles for cards and dependency lines
    -   Fixed: Forced color issues in Kanban component to improve accessibility \[WCAG 2.1 AA\] support
-   **Version 24.0.7 - September 2023**

    A UI Builder enabled visual board component to be used in configurable workspaces.


