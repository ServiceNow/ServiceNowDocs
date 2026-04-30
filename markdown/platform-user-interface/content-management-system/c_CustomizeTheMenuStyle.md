---
title: Menu style customization
description: You can customize menu styles in the style sheets your site uses.
locale: en-US
release: zurich
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Menu types, Create a navigation menu block, Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Menu style customization

You can customize menu styles in the style sheets your site uses.

Navigate to **Content Management** &gt; **Design** &gt; **Style Sheets** to customize style sheets.

## Supplementary page navigation menu example code

In the following example, look at the CSS class selectors and rules. Also, review how the block containers \(div.cms\_menu\_section\_blocks\) are defined based on the outer container \(TD.layout\_content\_submenu\_column\). The outer container is actually a part of the site layout.

This concept is clearer if you compare the styles to the styles used in the super menu further down in the example. This example shows that there is no need to make a completely new menu system. You can use CSS to change the look and feel of existing menus.

```
/*********************************************************************************************************************************************************
   SUB MENU VARIATIONS FOR HORIZONTAL MENUS - Section Blocks Menu (cms_menu_section_blocks UI Macro)
*********************************************************************************************************************************************************/
TD.layout_content_submenu_column DIV.cms_menu_section_blocks {
    width: 156px;
    height: auto;
    float: left;
    position: relative;
    border-style: solid;
    margin: 0px 0px 0px 0px;
    border: 0px solid #e0e0e0;
    padding: 0px;
    background: none;
    padding: 24px 12px 0px 12px;
}
 
TD.layout_content_submenu_column DIV.sub_menu_section {
    width: 156px;
    height: 20px;
    float: left;
    border-style: solid;
    border: 0px solid #e0e0e0;
    padding: 0px;
    background: none;
    padding: 0px 12px 0px 12px;
}
 
SPAN.cms_sub_menu_list_link, TD.submenu_cell A   {
    color: #FFF;
}
 
TD.layout_content_submenu_column IMG.menu_bullet{
	display: none;
}
 
TD.cms_menu_section_blocks_title h2, TD.cms_menu_section_blocks_title h2 a, TD.cms_menu_tab_blocks_text h2 {
    margin:0;
    padding: 0px;
    font-size: 11px;
    text-transform: uppercase;
    color: #42C4DD;
    font-weight: normal;
    white-space: nowrap;
}
 
TD.layout_content_submenu_column a.cms_menu_block_item {
    margin:0;
    padding: 0px;
    font-size:11px;
    color:#FFF;
}
 
TR.layout_content_submenu_row TD.layout_content_submenu_column{
	background: transparent url(sub_menu_background.gifx) repeat-y center top !important; 
}

```

## Super menu sections example code

The following menu is a simple float grid. The defaults are written first. Then, below the "SUPER MENU VARIATIONS..." comment, the defaults are overwritten by adding a containing div with a unique class. In the code that renders the header for the base system, the bottom menu resides in a table cell with the class of `cms_header_bottom_menu` \(refer to the TD.cms\_header\_bottom\_menu CSS selector\).

```
/*********************************************************************************************************************************************************
   SUB MENU VARIATIONS FOR HORIZONTAL MENUS - Section Blocks Menu (cms_menu_section_blocks UI Macro)
*********************************************************************************************************************************************************/
 
TD.layout_content_submenu_column DIV.cms_menu_section_blocks {
    width: 156px;
    height: auto;
    float: left;
    position: relative;
    border-style: solid;
    margin: 0px 0px 0px 0px;
    border: 0px solid #e0e0e0;
    padding: 0px;
    background: none;
    padding: 24px 12px 0px 12px;
}
 
TD.layout_content_submenu_column DIV.sub_menu_section {
    width: 156px;
    height: 20px;
    float: left;
    border-style: solid;
    border: 0px solid #e0e0e0;
    padding: 0px;
    background: none;
    padding: 0px 12px 0px 12px;
}
 
SPAN.cms_sub_menu_list_link, TD.submenu_cell A   {
    color: #FFF;
}
 
TD.layout_content_submenu_column IMG.menu_bullet{
	display: none;
}
 
TD.cms_menu_section_blocks_title h2, TD.cms_menu_section_blocks_title h2 a, TD.cms_menu_tab_blocks_text h2 {
    margin:0;
    padding: 0px;
    font-size: 11px;
    text-transform: uppercase;
    color: #42C4DD;
    font-weight: normal;
    white-space: nowrap;
}
 
TD.layout_content_submenu_column a.cms_menu_block_item {
    margin:0;
    padding: 0px;
    font-size:11px;
    color:#FFF;
}
 
TR.layout_content_submenu_row TD.layout_content_submenu_column{
	background: transparent url(sub_menu_background.gifx) repeat-y center top !important; 
}


4.2 2. Super Menu Sections Example Code

This menu is essentially a simple float grid. The defaults are written first. Then, below the "SUPER MENU VARIATIONS..." comment, the defaults are overwritten by adding a containing div with a unique class. In the code that renders the header for the base system, the bottom menu resides in a table cell with the class of "cms_header_bottom_menu" (note the TD.cms_header_bottom_menu CSS selector).

/*******************************************************************************************
   Section Blocks Menu (cms_menu_section_blocks UI Macro)
*******************************************************************************************/
div.cms_menu_section_blocks {
    width: 260px;
    height: 260px;
    float: left;
    border-style: solid;
    margin: 0px 0px 12px 12px;
    border: 1px solid #e0e0e0;
    padding: 10px;
    background: url(blue/portal_horizontal_bkg.pngx) repeat-x center bottom; 
}
 
p.cms_menu_separator {
    border-top:1px dotted #ccc;
    margin-top: 6px;
    margin-bottom: 6px;
}
 
td.cms_menu_section_blocks_title h2, td.cms_menu_section_blocks_title h2 a, td.cms_menu_tab_blocks_text h2 {
    margin:0;
    padding: 0px;
    font-size: larger;
    font-weight: normal;
    color:#444;
}
 
a.cms_menu_block_item {
    margin:0;
    padding: 0px;
    color:#999;
    font-size: inherit; 
}
 
/*******************************************************************************************
   SUPER MENU VARIATIONS FOR HORIZONTAL MENUS - Section Blocks Menu (cms_menu_section_blocks UI Macro)
*******************************************************************************************/
TD.cms_header_bottom_menu .cms_menu_super_menu_bar { /*style the super menu drop down bar */
   z-index: 199;
   float: left;
   background: none;
   margin-left: 44px;
}
 
TD.cms_header_bottom_menu div.cms_menu_section_blocks {
    width: 200px;
    float: left;
    border: 0px;
    margin: 0px 0px 12px 0px;
    padding: 0px;   
    background: none; 
}
 
TD.cms_header_bottom_menu p.cms_menu_separator {
    border-top:0px dotted #ccc;
    margin-top: 0px;
    margin-bottom: 0px;
}
 
TD.cms_header_bottom_menu  .cms_menu_super_menu_bar_item {  /*style an item on the super menu drop down bar*/ 
   z-index: 200;
   float: left; 
   padding-left: 12px; 
   padding-right: 12px;
   padding-bottom: 8px;
   padding-top: 4px;
   cursor: pointer;
   cursor: hand;
   font-weight: bold;
   color: #000;
   border-left: 1px solid #FFF;
   border-top: 1px solid #FFF;
}
 
TD.cms_header_bottom_menu  .cms_menu_super_menu_bar_item_selected {  /*style a selected item on the super menu drop down bar*/ 
   z-index: 200;
   float: left; 
   padding-left: 12px; 
   padding-right: 12px;
   padding-bottom: 8px;
   padding-top: 4px;
   cursor: pointer;
   cursor: hand;
   background: #fff url(super_menu_bkg.gifx) no-repeat left top;
   font-weight: bold;
   border-right: 0px solid #CCC;
   border-bottom: 0px solid #CCC;
   border-left: 1px solid #DDD;
   border-top: 1px solid #EEE;
 
}
 
TD.cms_header_bottom_menu  .cms_menu_super_menu_content { /* style super menu content block */
   position: absolute;
   z-index: 999;
   height:260px;
   display: none;
   padding: 18px;
   background: #dedfe0 url(super_menu_bkg.gifx) no-repeat left top;
   border-right: 1px solid #CCC;
   border-bottom: 1px solid #CCC;
   border-left: 1px solid #DDD;
   box-shadow: 5px 5px 6px #666;
   -webkit-box-shadow: 5px 5px 6px #666;
   -moz-box-shadow: 5px 5px 6px #666;
   filter: progid:DXImageTransform.Microsoft.dropShadow(color=#666, offX=5, offY=5, positive=true);
}
 
TABLE.super_menu_video_table {
    background: #787878 url("grey_background.pngx") repeat-y scroll center top;
	width: 184px;
}
```

**Parent Topic:**[Menu types](../reference/r_MenuTypes.md)

