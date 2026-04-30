---
title: Approval assignment scripts
description: This is a searchable version of the useful approval and assignment scripts.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Field script use cases, Useful scripts, Scripting, API implementation, API implementation and reference]
---

# Approval assignment scripts

This is a searchable version of the useful approval and assignment scripts.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

For see [Viewing my approvals](https://www.servicenow.com/docs/access?context=viewing-my-approvals&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

-   **Assign a group for ESS requests**

    The following Assignment Rulescript automatically assigns a group for all ESS Requests.

    ```
    if(current.opened_by.roles==""){
        current.assignment_group.setDisplayValue('Network');
        current.update();}
    ```

-   **Assign catalog item to group based on delivery plan task**

    This assignment rule assigns a service catalog item to the database group if it uses a delivery plan that has a catalog task assigned to the desktop group.

    ```
    //Return catalog items that have no group but do have a delivery plan assigned
    var ri =new GlideRecord("sc_cat_item");
    ri.addQuery("group","=",null);
    ri.addQuery("delivery_plan","!=",null);
    ri.query();
    while(ri.next()){
        gs.log("Found an item");
        //Return tasks that point to the same delivery plan as the above item
        var dptask =new GlideRecord("sc_cat_item_delivery_task");
        dptask.addQuery("delivery_plan","=",ri.delivery_plan);
        dptask.query();while(dptask.next()){
            gs.log("Found a task");var gp = dptask.group.getDisplayValue();
            gs.log(gp);//If the task is assigned to desktop, assign the item's group to desktop
            if(dptask.group.getDisplayValue()=="Desktop"){
                ri.group.setDisplayValue("Desktop");
                gs.log("updating "+ ri.getDisplayValue());
                ri.update();break;}}}
    ```

-   **Assign items with one task**

    This assignment rule automatically assigns any catalog items with only one task associated to a particular group.

    ```
    //Get the catalog item for the current requested item
    var scCatItem =new GlideRecord("sc_cat_item");
    if(scCatItem.get('sys_id', current.cat_item)){
    // If the catalog item already has an assignment group or if using workflow we don't need to make an assignment
      if(!scCatItem.delivery_plan.nil()&& scCatItem.group.nil()){
            var dpTask =new GlideRecord("sc_cat_item_delivery_task");
            dpTask.addQuery("delivery_plan","=",scCatItem.delivery_plan);
            dpTask.query();
            if(dpTask.getRowCount()==1&& dpTask.next()){
            // Check that there is only 1 record in the GlideRecord
                dpTask.group;}}}
    ```

-   **Assignment based on workload**

    Type: Business Rule.

    Description: Populate the assigned to based on the assignment group member who has the least amount of active incidents.

    Parameters:

    -   order: &gt;1000 if you want to execute after assignment rules
    -   condition: current.assigned\_to == '' &amp;&amp; current.assignment\_group != ''
    -   when: before, insert/update
    ```
    var assignTo = getLowestUser();
    gs.addInfoMessage("assigning to is "+ assignTo);
    current.assigned_to= assignTo;
     
    function getLowestUser(){
      var userList =new Array();
      var cg =new GlideRecord('sys_user_grmember');
      cg.addQuery('group', current.assignment_group);
      cg.query();
      while(cg.next()){
        var tech = cg.user.toString();
        var cnt = countTickets(tech);
        gs.addInfoMessage("Tech counts "+ cg.user.name+' '+ cnt +" "+ tech);
        userList.push({ sys_id: tech,name: cg.user.name, count: cnt });}
    
      for(var i=0; i < userList.length; i++){
        gs.addInfoMessage(userList[i].sys_id+" "+ userList[i].name+" "+ userList[i].count);}
      userList.sort(function(a, b){
        gs.addInfoMessage("Sorting: "+ a.sys_id+"("+ a.count+");
        "+ b.sys_id+"("+ b.count+")");
        return a.count- b.count;});
    
      if(userList.length<=0)return"";
      return userList[0].sys_id;}
     
    function countTickets(tech){
      var ct =new GlideRecord('incident');
      ct.addQuery('assigned_to',tech);
      ct.addQuery('active',true);
      ct.query();
      return ct.getRowCount();}
    ```

-   **Run assignment rules when category is changed**

    Type: Client script.

    Table: Incident.

    Description: This example is an onChange client script on the category field within Incident. Note: this script used to use synchronous AJAX \(asynchronous behavior is specified by the third parameter of the ajaxRequest call\). The implementation below uses asynchronous AJAX. The drawback of using the synchronous version is that a network response problem could cause the browser to hang.

    ```
    // Make an AJAX request to the server to get who this incident would be
    // assigned to given the current values in the record. This runs the assignment 
    // rules thathave been defined in System Policy and returns the assigned_to and 
    // the assignment_group
     
    function onChange(control, oldValue, newValue, isLoading){
      if(isLoading){return;
      // No change, do not do anything
      }
    
       // Construct the URL to ask the server for the assignment
      var url ="xmlhttp.do?sysparm_processor=AJAXAssignment&sys_target=incident";
      var uv = gel('sys_uniqueValue');
      if(uv){
            url +="&sys_uniqueValue="+ uv.value;}
      // Make the AJAX request to the server and get the response
      var serial = g_form.serialize();
      // get all values currently assigned to the incident
      var response = ajaxRequest(url, serial,true, responseFunc);}
     
    // This callback function handles the AJAX response.
    function responseFunc(response){
      varitem= response.responseXML.getElementsByTagName("item")[0];
      // Process the item returned by the server
      if(item){
      // Get the assigned_to ID and its display value and put them on the form
        varname=item.getAttribute("name");
        var name_label =item.getAttribute("name_label");
        if(name_label &&name){
          g_form.setValue('assigned_to',name, name_label);}
        else{
          g_form.setValue('assigned_to','','');}
        // Get the assignment_group ID and its display value and put then on the form
        var group =item.getAttribute("group");
        var group_label =item.getAttribute("group_label");
        if(group_label && group){
          g_form.setValue('assignment_group', group, group_label);}
        else{
          g_form.setValue('assignment_group','','');}}}
    ```

-   **Custom approval UI macro**

    For information on creating a custom approval UI macro, see [UI macros](../../server-scripting/concept/c_UIMacros.md#).


**Parent Topic:**[Field script use cases](r_UsefulFieldScripts.md)

