---
title: SAP Connector methods
description: The SAP connector provides various methods that you can use to automate workflows on SAP graphical user interface \(GUI\) interfaces. SAP connector methods are available at different levels - connector, screen, and element.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [SAP connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# SAP Connector methods

The SAP connector provides various methods that you can use to automate workflows on SAP graphical user interface \(GUI\) interfaces. SAP connector methods are available at different levels - connector, screen, and element.

## SAP Connector methods

The SAP Connector methods are available at three levels.

-   **Application**: You can find these methods when you double-click the SAP connector object. To access these methods, do the following steps:
    1.  Add the SAP connector under the **Global Objects** in the **Project Explorer** pane.

        For more information, see [Configure the SAP connector](../task/configure-the-sap-connector.md).

    2.  Double-click the SAP connector object.

        The methods appear in the Object Explorer pane.

-   **Screen**: Use these methods to automate tasks on an SAP application screen that you have added. For example, automate the maximizing of an application window. To access these methods, do the following steps:
    1.  Add one or more SAP application screens. To learn to configure, see [Configure the SAP connector](../task/configure-the-sap-connector.md).
    2.  Double-click the screen that you've added.

        The methods appear in the Object Explorer pane.

-   **Element**: Use these methods to automate actions on the SAP screen UI elements, for example, a button or a check box. For example, automate the selecting of a button. To access these methods, do the following steps:
    1.  Add one or more SAP application screens. To learn to configure, see [Configure the SAP connector](../task/configure-the-sap-connector.md).
    2.  Capture one or more screen elements. To learn to capture, see [Use the Capture element dialog](../task/use-context-dialog.md).

        The screen elements appear under the captured SAP screen.

    3.  Double-click the screen element.

        The methods appear in the Object Explorer pane.


## Use the methods

To create an automation by using the methods, drag them from the Object Explorer pane to the Design surface and connect them.

![Methods connected.](../image/SAP-connector-methods-connected.png)

## Application-level methods

-   **OpenConnection**

    Establishes a connection between the connector and the SAP application. You must first use this method before executing an automation.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |name|Name of the connection.|Data In|String|None|Yes|
    |username|User name for making the connection.|Data In|String|None|Yes|
    |password|Password for making the connection.|Data In|String|None|Yes|

-   **SetDefaultSession**

    Makes the selected session a default session.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |sessionId|Unique Id of the session that you want to set as default.|Data In|String|None|Yes|

-   **CloseConnection**

    Closes the connection between the connector and the SAP application.


## Screen-level methods

-   **ClickMenuItem**

    Selects the menu item that you specify the ID of on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuId|The ID of the menu that must be selected.|Data In|String|None|Yes|

-   **Close**

    Closes the session of the SAP screen.

-   **CreateSession**

    Creates a session of the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |tCode|Transaction code that enables you to access specific part of the SAP application.|Data In|String|NA|Yes|
    |Return|Returns the Id of the session created.|Data Out|String|NA|NA|

-   **EndSession**

    Ends the open session.

-   **EndTransaction**

    Ends a transaction.

-   **Focus**

    Sets the focus on the open session.

-   **GetMenuItem**

    Gets the name of the specified menu item.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuId|ID of the menu item to get the name.|Data In|String|None|Yes|
    |Return|Returns the name of the menu item|Data Out|String|None|NA|

-   **GetMenuItemsIdsByName**

    Retrieves the ID of the menu that you specify by its name.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuItemName|Name of the menu item.|Data Out|List|None|NA|

-   **GetWindowHandle**

    Returns the window handle of the SAP application screen.

-   **IsCreated**

    Returns `true` if the session is created, `false` if the session isn’t created.

-   **IsSessionBusy**

    Returns `true` if the session is busy, and `false` if the session isn’t busy.

-   **Maximise**

    Maximizes the SAP screen.

-   **Minimise**

    Minimizes the SAP screen.

-   **Resize**

    Resizes the SAP screen according to the dimensions specified.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |xPos|Position of the screen along the X-axis.|Data In|Integer|None|Yes|
    |yPos|Position of the screen along the Y-axis.|Data In|Integer|None|Yes|
    |Width|Width of the screen.|Data In|Integer|None|Yes|
    |Height|Height of the screen.|Data In|Integer|None|Yes|

-   **Restore**

    Restores the screen to its original dimensions.

-   **ScreenId**

    Returns the ID of the SAP application screen as a string.

-   **SendKeys**

    Sends the keyboard strokes to the SAP application screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |Keys|Keyboard strokes that you want to send to the SAP screen.|Data In|String|NA|Yes|

-   **StartTransaction**

    Starts a transaction.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |tCode|Transaction code that enables you to access specific part of the SAP application.|Data In|String|NA|Yes|

-   **WaitForCreate**

    Waits for the specified duration while the screen is being created. This enables all the dynamic controls to load after the screen is created.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |timeoutInSeconds|Duration after which the method times out.|Data In|Integer|None|Yes|
    |MatchAllChildren|Option to indicate whether before loading the screen, the method matches all the captured children screens and elements with the screen.|Data In|Boolean|False|No|


## Element-level methods

In the SAP connector, you can use these element-level methods to identify elements, verify their presence on the screen, or define actions to be performed on the elements.

The following tables include elements and their available methods. For the description of these methods and their parameters, see [SAP Connector methods](sap-connector-methods.md).

|Element|Methods|
|-------|-------|
|GuiButton|[Click](sap-element-methods.md#dlentry_owc_313_12c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiCheckBox|[Check](sap-element-methods.md#dlentry_bfc_yrb_s1c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsChecked](sap-element-methods.md#dlentry_nhz_grc_s1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[Uncheck](sap-element-methods.md#dlentry_mkk_hsb_s1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiComboBox|[Get](sap-element-methods.md#dlentry_ufs_xgl_q1c)|
|[GetIconName](sap-element-methods.md#dlentry_sqn_phl_q1c)|
|[GetList](sap-element-methods.md#dlentry_as5_ygl_q1c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[Set](sap-element-methods.md#dlentry_gcm_hhl_q1c)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiCtrlGridView|[ClickButtonCell](sap-element-methods.md#dlentry_jgp_njc_b2c)|
|[ClickCell](sap-element-methods.md#dlentry_u1t_z3c_b2c)|
|[DeselectAllRows](sap-element-methods.md#dlentry_bkz_z3c_b2c)|
|[GetCellType](sap-element-methods.md#dlentry_tlf_1jc_b2c)|
|[GetCellValue](sap-element-methods.md#dlentry_vdm_1jc_b2c)|
|[GetColumns](sap-element-methods.md#dlentry_sns_1jc_b2c)|
|[GetColumnsKeyValuePair](sap-element-methods.md#dlentry_pdz_1jc_b2c)|
|[GetRowCount](sap-element-methods.md#dlentry_c5g_bjc_b2c)|
|[GetRows](sap-element-methods.md#dlentry_dkr_bjc_b2c)|
|[GetRowsByColumn](sap-element-methods.md#dlentry_o3z_bjc_b2c)|
|[GetSelectedColumns](sap-element-methods.md#dlentry_g2g_cjc_b2c)|
|[GetSelectedRows](sap-element-methods.md#dlentry_m5n_cjc_b2c)|
|[GetSingleRow](sap-element-methods.md#dlentry_sm5_cjc_b2c)|
|[GetVisibleRows](sap-element-methods.md#dlentry_vwb_djc_b2c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[SelectAllRows](sap-element-methods.md#dlentry_nfj_djc_b2c)|
|[SelectCell](sap-element-methods.md#dlentry_mlv_djc_b2c)|
|[SelectContextMenuItemById](sap-element-methods.md#dlentry_d52_2jc_b2c)|
|[SelectContextMenuItemByPosition](sap-element-methods.md#dlentry_cpl_2jc_b2c)|
|[SelectContextMenuItemByText](sap-element-methods.md#dlentry_zqs_2jc_b2c)|
|[SelectSingleRow](sap-element-methods.md#dlentry_unz_2jc_b2c)|
|[SelectToolbarMenuItemById](sap-element-methods.md#dlentry_w1g_fjc_b2c)|
|[SelectToolbarMenuItemByPosition](sap-element-methods.md#dlentry_h14_fjc_b2c)|
|[SelectToolbarMenuItemByText](sap-element-methods.md#dlentry_cfv_fjc_b2c)|
|[SetCellValue](sap-element-methods.md#dlentry_qxb_gjc_b2c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiLabel|[GetText](sap-element-methods.md#dlentry_ess_zzb_s1c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiPassword|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetCaretPosition](sap-element-methods.md#dlentry_k53_c1c_s1c)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[SetText](sap-element-methods.md#dlentry_mwk_b1c_s1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiRadioButton|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsChecked](sap-element-methods.md#dlentry_nhz_grc_s1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[Select](sap-element-methods.md#dlentry_f5z_pqc_s1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiStatusBar|[GetStatus](sap-element-methods.md#dlentry_hmv_glk_q1c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiTab|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[SelectTab](sap-element-methods.md#dlentry_orm_thd_s1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiTableControl|[DeselectAllVisibleRows](sap-element-methods.md#dlentry_gzn_rvs_q1c)|
|[DeselectRow](sap-element-methods.md#dlentry_nbh_5vs_q1c)|
|[DeselectVisibleRow](sap-element-methods.md#dlentry_zm1_tvs_q1c)|
|[GetAllVisibleRows](sap-element-methods.md#dlentry_a33_1ws_q1c)|
|[GetColumnNames](sap-element-methods.md#dlentry_h4m_fws_q1c)|
|[GetMaximumScrollOffset](sap-element-methods.md#dlentry_qbs_mws_q1c)|
|[GetScrollPosition](sap-element-methods.md#dlentry_str_rys_q1c)|
|[GetSingleRow](sap-element-methods.md#dlentry_kdv_gws_q1c)|
|[GetTable](sap-element-methods.md#dlentry_hsp_kws_q1c)|
|[GetVisibleRowCount](sap-element-methods.md#dlentry_zg5_cws_q1c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[ScrollDownByOneRow](sap-element-methods.md#dlentry_ojz_1zs_q1c)|
|[ScrollToHorizontalPosition](sap-element-methods.md#dlentry_f3x_bzs_q1c)|
|[ScrollToNextPage](sap-element-methods.md#dlentry_wm1_5gw_12c)|
|[ScrollToPreviousPage](sap-element-methods.md#dlentry_xm1_5gw_12c)|
|[ScrollToVerticalPosition](sap-element-methods.md#dlentry_lqf_dzs_q1c)|
|[ScrollUpByOneRow](sap-element-methods.md#dlentry_gcb_zys_q1c)|
|[SelectAllRows](sap-element-methods.md#dlentry_cnl_pvs_q1c)|
|[SelectSingleRow](sap-element-methods.md#dlentry_gq5_xqs_q1c)|
|[SelectVisibleRow](sap-element-methods.md#dlentry_d2y_mvs_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiTextBox|[GetText](sap-element-methods.md#dlentry_ess_zzb_s1c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetCaretPosition](sap-element-methods.md#dlentry_k53_c1c_s1c)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[SetText](sap-element-methods.md#dlentry_mwk_b1c_s1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiTree|[Check](sap-element-methods.md#dlentry_yqk_2rw_12c)|
|[ClickNodeItem](sap-element-methods.md#dlentry_hdq_bqw_12c)|
|[CollapseNodeItem](sap-element-methods.md#dlentry_epf_4mf_b2c)|
|[DoubleClickNode](sap-element-methods.md#dlentry_nhq_prw_12c)|
|[DoubleClickNodeItem](sap-element-methods.md#dlentry_kfj_trw_12c)|
|[GetColumnsKeyValuePair](sap-element-methods.md#dlentry_ad3_bqw_12c)|
|[GetTreeType](sap-element-methods.md#dlentry_ggf_1qw_12c)|
|[GetNodeKeyByPath](sap-element-methods.md#dlentry_dtx_bqw_12c)|
|[GetNodeKeyByText](sap-element-methods.md#dlentry_crf_cqw_12c)|
|[GetNodeItemText](sap-element-methods.md#dlentry_vqn_cqw_12c)|
|[GetSelectedNodes](sap-element-methods.md#dlentry_unv_cqw_12c)|
|[GetNodeItemCheckBoxState](sap-element-methods.md#dlentry_jbw_25w_12c)|
|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[PressNodeItemButton](sap-element-methods.md#dlentry_ff4_xxw_12c)|
|[SelectTab](sap-element-methods.md#dlentry_orm_thd_s1c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[SelectNodeItem](sap-element-methods.md#dlentry_ubf_2yw_12c)|
|[SelectNode](sap-element-methods.md#dlentry_z3g_mnf_b2c)|
|[SelectContextMenuItemById](sap-element-methods.md#dlentry_gqd_dqw_12c)|
|[SelectContextMenuItemByText](sap-element-methods.md#dlentry_iyr_dqw_12c)|
|[SelectContextMenuItemByPosition](sap-element-methods.md#dlentry_ehb_2qw_12c)|
|[Uncheck](sap-element-methods.md#dlentry_cdy_hrw_12c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

|Element|Methods|
|-------|-------|
|GuiUserArea|[Highlight](sap-element-methods.md#dlentry_ks3_jlk_q1c)|
|[IsCreated](sap-element-methods.md#dlentry_l11_llk_q1c)|
|[MouseClick](sap-element-methods.md#dlentry_a5s_qlk_q1c)|
|[ScrollToNextPage](sap-element-methods.md#dlentry_h53_znw_12c)|
|[ScrollToPreviousPage](sap-element-methods.md#dlentry_x2t_znw_12c)|
|[SendKeys](sap-element-methods.md#dlentry_jnx_rjl_zdc)|
|[SetFocus](sap-element-methods.md#dlentry_j5g_nlk_q1c)|
|[SetHorizontalScroll](sap-element-methods.md#dlentry_vh1_cdl_q1c)|
|[SetVerticalScroll](sap-element-methods.md#dlentry_gsv_4dl_q1c)|
|[WaitForCreate](sap-element-methods.md#dlentry_lvb_5lk_q1c)|

