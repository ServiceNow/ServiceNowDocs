---
title: Update the state model script include
description: Update the ChangeRequestStateModel\_normal script include to add new functions for the Complete state.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Tutorial: add a new change management state, Reference section for Change Management, Change Management, IT Service Management]
---

# Update the state model script include

Update the ChangeRequestStateModel\_normal script include to add new functions for the **Complete** state.

## Before you begin

Role required: admin

## About this task

You update the ChangeRequestStateModel\_normal with the following configuration.

-   Add new *canMove* and *moving* functions for the **Complete** state. These functions can return a value of **true** since there are no special conditions for or extra actions to perform when moving to the **Complete** state.
-   Modify the definition of the existing object for the **Implement** state to ensure that the next state is **Complete**.
-   Add an object for the **Complete** state, which defines **Review** and **Closed** as the next two states.

    **Note:** The *canMove* functions for the transition to these states from **Complete** checks the **Needs review** custom field to determine the correct next state.


## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Open the ChangeRequestStateModel\_normal script include and modify the script as follows.

    1.  Add the following line at the end of the script include but before the line that starts with **type**:

        ```
        toComplete_moving: function() {
                      return true; 
                 },              
        
                 toComplete_canMove: function() {      
                       return true;       
                 },
        ```

        ![Revised script](../image/NewStateTutUpdScrptIncl2.png)

    2.  Modify the existing *implement* object to *toComplete*:

        ```
        implement: {
                    nextState: [ "complete" ],
        
                    complete: { 
                        moving: function() {                
                            return this.toComplete_moving(); 
                        },             
        
                        canMove: function() {                
                            return this.toComplete_canMove();            
                        }       
                    },        
        
                    canceled: {  
                        moving: function() {               
                           return this.toCanceled_moving();   
                        },             
        
                        canMove: function() {               
                           return this.toCanceled_canMove(); 
                        }        
                    }    
                },
        ```

3.  Add the following new state object for *complete*.

    ```
    complete: {
                 nextState : [ "review", "closed" ],         
    
                 review : {            
                       moving : function() {
                             return this.toReview_moving();            
                       },             
    
                       canMove : function() {              
                              if (this._gr.getValue("u_needs_review") == "Yes")   
                                   return true;                            
                          
                              return false;
                       }        
                 },                     
    
                 closed : {            
                       moving : function() {  
                             return this.toClosed_moving();
                       },             
    
                       canMove : function() {              
                              if (this._gr.getValue("u_needs_review") == "No")
                                   return true;    
                            
                      return false;
                      }       
                 },  
    
                 canceled : { 
                       moving : function() {                
                             return this.toCanceled_moving();     
                       },             
    
                       canMove : function() {                
                              return this.toCanceled_canMove(); 
                       }   
                 }    
            },
    ```

4.  Click **Update**.


**Parent Topic:**[Tutorial: add a new change management state](t_AddNewStateTutorial.md)

**Previous topic:**[Update the state handler script include](t_UpdateStateHandlerScriptInclude.md)

**Next topic:**[Create a UI action](t_CreateNewUIAction.md)

