---
title: CartJS - Scoped
description: The CartJS API provides methods that enable you to access a user's shopping cart.Creates an instance of the CartJS class with the name of a defined cart for the user who is currently logged in.Adds the request for a catalog item to the current cart.Specifies if the current user has the required role to edit the Request for field.Performs the cart checkout. If the two-step checkout is enabled, returns the order summary. If the two-step checkout is disabled, the cart is submitted and details of the generated request are returned.Deletes the current cart.Returns the cart details.Returns the ID of the current cart.Returns a GlideRecord object containing records for items in the current cart.Returns the delivery address for the current cart.Returns the sys\_id of the user for whom the cart is requested.Returns the name of the user for whom the current cart is requested.Returns the special instructions for the current cart.Orders a single item. If two-step checkout is enabled, the method adds the specified item to the cart and returns the sys\_id of the cart. If two-step checkout is disabled, the method completes the purchase of the specified item and returns the sys\_id of the generated request.Sets the delivery address for the current cart.Sets the sys\_id in the sys\_user record of the user for whom the cart is requested.Sets the special instructions for the current cart.Updates special instructions, requested for, and delivery address from the request parameter and performs the cart checkout. Use this API to modify the mentioned parameters of the cart and perform the cart checkout simultaneously. Missing parameters in the request object will have their default value.Updates an item in the cart.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CartJS- Scoped

The CartJS API provides methods that enable you to access a user's shopping cart.

This API runs in the `sn_sc` namespace. The Service Catalog Scoped API plugin \(ID: com.glideapp.servicecatalog.scoped.api\) that is enabled by default is required to access the CartJS API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CartJS - CartJS\(String cartName\)

Creates an instance of the CartJS class with the name of a defined cart for the user who is currently logged in.

|Name|Type|Description|
|----|----|-----------|
|cartName|String|Optional. Name of a defined cart for the user who is currently logged in.|

```
var cart = new sn_sc.CartJS(cart1);
```

## CartJS - addToCart\(Map request\)

Adds the request for a catalog item to the current cart.

<table id="table_ecz_zjy_5z" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

request

</td><td>

Map

</td><td>

A JSON object that contains the details of the catalog item to be added to the cart.The structure of the request object is:

 ```
{
'sysparm_id': item_id,
'sysparm_quantity': item_quantity,
'variables':{
'var_name': 'var_value',
...
}
}
```

 -   item\_id: sys\_id of the item to be added to the cart
-   item\_quantity: Number of items to be added. Default value is 1.
-   var\_name: Name of the question.
-   var\_value: Value of the answer \(Not the display value\).

</td></tr></tbody>
</table><table id="table_fcz_zjy_5z" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON

</td><td>

Structure of the current cart.```
{
'subtotal': value,
'items':[
{
itemName:'',
quantity:'', 
price:'', 
recurring_price:''
} ...]
}
```

</td></tr></tbody>
</table>This example shows how you can add multiple items to the cart. Note that `var cart = new sn_sc.CartJS();` is inside the loop. You must call `sn_sc.CartJS()` multiple times to be able to add multiple items to the cart.

```
for (i = 0; i < 2; i++) { 
var cart = new sn_sc.CartJS();
var item =
{
'sysparm_id': '0d08837237153000158bbfc8bcbe5d02',
'sysparm_quantity': '1',
'variables':{
'carrier': 'at_and_t_mobility',
'data_plan': '500MB',
'duration': 'eighteen_months',
'color': 'slate',
'storage': 'sixtyfour' 
}};
var cartDetails = cart.addToCart(item);
gs.info(JSON.stringify(cartDetails));
}
```

Output

```
//The cart after the first item is added
{
  "cart_id": "c0f5828a1b476010593876a61a4bcb71",
  "subtotal": "$599.99",
  "items": [
    {
      "catalog_item_id": "0d08837237153000158bbfc8bcbe5d02",
      "quantity": "1",
      "localized_price": "$599.99",
      "price": "$599.99",
      "recurring_frequency": "Monthly",
      "localized_recurring_price": "$30.00",
      "recurring_price": "$29.00",
      "item_name": "Apple iPhone 5",
      "cart_item_id": "40f5828a1b476010593876a61a4bcb72"
    }
  ]
}

//The cart after the second item is added
{
  "cart_id": "c0f5828a1b476010593876a61a4bcb71",
  "subtotal": "$1,199.98",
  "items": [
    {
      "catalog_item_id": "0d08837237153000158bbfc8bcbe5d02",
      "quantity": "1",
      "localized_price": "$599.99",
      "price": "$599.99",
      "recurring_frequency": "Monthly",
      "localized_recurring_price": "$30.00",
      "recurring_price": "$29.00",
      "item_name": "Apple iPhone 5",
      "cart_item_id": "40f5828a1b476010593876a61a4bcb72"
    },
    {
      "catalog_item_id": "0d08837237153000158bbfc8bcbe5d02",
      "quantity": "1",
      "localized_price": "$599.99",
      "price": "$599.99",
      "recurring_frequency": "Monthly",
      "localized_recurring_price": "$30.00",
      "recurring_price": "$29.00",
      "item_name": "Apple iPhone 5",
      "cart_item_id": "98f5828a1b476010593876a61a4bcb75"
    }
  ]
}
```

## CartJS - canViewRF\(\)

Specifies if the current user has the required role to edit the **Request for** field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ky1_pzt_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user has the required role to edit the requested for field.Possible values:

-   true: User has the required role.
-   false: User does not have the required role.

Data type: Boolean

</td></tr></tbody>
</table>This background script code example shows how to check if the current user has the role needed to edit the requested for field.

```
gs.log(sn_sc.CartJS.canViewRF());
```

Response:

```
true
```

## CartJS - checkoutCart\(\)

Performs the cart checkout. If the two-step checkout is enabled, returns the order summary. If the two-step checkout is disabled, the cart is submitted and details of the generated request are returned.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wqd_hsd_zz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON

</td><td>

If the two-step checkout is enabled, the summary of the items in the cart is returned.```
{ "subtotal_price":"",
  "subtotal_recurring_frequency":"",
  "delivery_address":"",
  "special_instructions":"",
  "total_title":"",
  "requested_for_user":"System Administrator",
  "requested_for":"6816f79cc0a8016401c5a33be04be441",
  "daily": ["frequency_subtotal":"", "items":[{}, {}, ...], …],
  "monthly":["frequency_subtotal":"", "items":[{}, {}, ...], …],
  "annually":["frequency_subtotal":"", "items":[{}, {}, ...], …],
  "none":["frequency_subtotal":"", "items":[{}, {}, ...], …],
}
```

 If the two-step checkout is disabled:

```
{
  'request_id' : "sys_id of the generated request",
  "request_number" : "Number of the generated request"
}
```

</td></tr></tbody>
</table>```
var cart = new sn_sc.CartJS();
var checkoutInfo = cart.checkoutCart();
gs.info(checkoutInfo);

```

Output

```
If two step checkout enabled:
{"subtotal_price":"$2,748.49","subtotal_recurring_frequency":"","delivery_address":"","special_instructions":"","total_title":"Total","requested_for_user":"System Administrator","requested_for":"6816f79cc0a8016401c5a33be04be441","weekly":{"subtotal_price":"$399.50","subtotal_recurring_frequency":"Weekly","subtotal_recurring_price":"$0.00","total_title":"Total","items":[{"catalog_item_id":"e90a0f7237153000158bbfc8bcbe5d7f","variables":{},"quantity":"1","localized_price":"$399.50","price":"$399.50","recurring_frequency":"Weekly","localized_recurring_price":"$0.00","recurring_price":"$0.00","item_name":"Brother Network-Ready Color Laser Printer","cart_item_id":"f3f5c9b3c322320076173b0ac3d3ae00","delivery_time":"2 Days"}],"show_subtotal_price":"true","subtotal_title":"Subtotal"},"show_subtotal_price":"true","cart_id":"251c0562c326320076173b0ac3d3aeb4","subtotal_recurring_price":"$131.00","monthly":{"subtotal_price":"$849.99","subtotal_recurring_frequency":"Monthly","subtotal_recurring_price":"$31.00","total_title":"Total","items":[{"catalog_item_id":"d82ea08510247200964f77ffeec6c4ee","variables":{"Monthly data allowance":"500MB","Storage":"64GB","Color":"Space Gray","Is this a replacement for a lost or broken iPhone?":"No","What was the original phone number?":""},"quantity":"1","localized_price":"$799.99","price":"$849.99","recurring_frequency":"Monthly","localized_recurring_price":"$30.00","recurring_price":"$31.00","item_name":"Apple iPhone 6s Plus","cart_item_id":"18c509b3c322320076173b0ac3d3aef4","delivery_time":"2 Days"}],"show_subtotal_price":"true","subtotal_title":"Subtotal"},"yearly":{"subtotal_price":"$1,499.00","subtotal_recurring_frequency":"Annually","subtotal_recurring_price":"$100.00","total_title":"Total","items":[{"catalog_item_id":"774906834fbb4200086eeed18110c737","variables":{"Adobe Photoshop":"false","Adobe Acrobat":"false","Optional Software":"","Additional software requirements":"","Eclipse IDE":"true"},"quantity":"1","localized_price":"$1,499.00","price":"$1,499.00","recurring_frequency":"Annually","localized_recurring_price":"$100.00","recurring_price":"$100.00","item_name":"Developer Laptop (Mac)","cart_item_id":"6306c9b3c322320076173b0ac3d3ae89","delivery_time":"5 Days"}],"show_subtotal_price":"true","subtotal_title":"Subtotal"},"subtotal_title":"Subtotal"}
If two step checkout disabled:
{"request_number":"REQ0010001","request_id":"2f2789f3c322320076173b0ac3d3ae62"}

```

## CartJS - empty\(\)

Deletes the current cart.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var cart = new sn_sc.CartJS();
      cart.empty();
```

## CartJS - getCartDetails\(\)

Returns the cart details.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object pointing to the current cart details.|

Example:

```
var cart=new sn_sc.CartJS();
	console.log (cart.getCartDetails());
```

Output:

```
delivery_address : "Brasilia,Brasil" 
        name : "DEFAULT" 
        requested_for : "62826bf03710200044e0bfc8bcbe5df1" 
        requested_for_display_name : "Abel Tuter" 
        special_instructions : "" 
        sys_id : "c2ac090087150300318d05a888cb0bd7" 

```

## CartJS - getCartID\(\)

Returns the ID of the current cart.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id for the current cart.|

Returns the sys\_id of the current cart.

```
var cart = new sn_sc.CartJS();
var cartId = cart.getCartID();
gs.info(cartId);
```

Output

```
039c516237b1300054b6a3549dbe5dfc
```

## CartJS - getCartItems\(\)

Returns a GlideRecord object containing records for items in the current cart.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord object including records and fields from the Item \[sc\_cart\_item\] table that describe an item in the current cart.|

Returns quantity and Catalog Item field values for items in the current cart.

```
var cart = new sn_sc.CartJS();

var cartItems = cart.getCartItems();
while (cartItems.next()) {
  gs.info(cartItems.getElement('quantity').getDisplayValue()
  + " x "
  + cartItems.getElement('cat_item').getDisplayValue());
}
```

Output

```

1 x Apple iPhone 6s Plus
1 x Apple iPhone 6s
1 x Apple MacBook Pro 15"
```

## CartJS - getDeliveryAddress\(\)

Returns the delivery address for the current cart.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Delivery address for the current cart.|

Sets and then returns the delivery address for the current cart.

```
var cart = new sn_sc.CartJS();
cart.setDeliveryAddress("Brasilia, Brasil");
var deliveryAddress = cart.getDeliveryAddress();
gs.info(deliveryAddress);
```

Output

```
Brasilia, Brasil
```

## CartJS - getRequestedFor\(\)

Returns the sys\_id of the user for whom the cart is requested.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xds_4ly_5z" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Sys\_id of the user record for whom the cart is requested.Table: User \[sys\_user\]

</td></tr></tbody>
</table>Returns the user sys\_id associated with the cart.

```
var cart = new sn_sc.CartJS();
cart.setRequestedFor("039c516237b1300054b6a3549dbe5dfc")
var userId = cart.getRequestedFor();
gs.info(userId);
```

Output:

```
039c516237b1300054b6a3549dbe5dfc
```

## CartJS - getRequestedForDisplayName\(\)

Returns the name of the user for whom the current cart is requested.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_z4j_dmy_5z" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Name of the user for whom the current cart is requested.Table: User \[sys\_user\]

</td></tr></tbody>
</table>Returns the name of the user associated with the cart.

```
var cart = new sn_sc.CartJS();
var userName = cart.getRequestedForDisplayName();
gs.info(userName);
```

Output:

```
Abel Tuter
```

## CartJS - getSpecialInstructions\(\)

Returns the special instructions for the current cart.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Special instructions for the current cart.|

This example shows how to set and retrieve the special instructions for the current cart.

```
var cart = new sn_sc.CartJS();
cart.setSpecialInstructions("Delivery before 8 AM.");
var specInstruction = cart.getSpecialInstructions();
gs.info(specInstruction);
```

Output

```
Delivery before 8 AM.
```

## CartJS - orderNow\(Map request\)

Orders a single item. If two-step checkout is enabled, the method adds the specified item to the cart and returns the sys\_id of the cart. If two-step checkout is disabled, the method completes the purchase of the specified item and returns the sys\_id of the generated request.

<table id="table_n4w_b4d_zz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

request

</td><td>

Map

</td><td>

JSON object that contains details of the catalog item to order.

</td></tr><tr><td>

request.delivery\_address

</td><td>

String

</td><td>

Address to which to deliver the items.Default: Address of user

</td></tr><tr><td>

request.sysparm\_id

</td><td>

String

</td><td>

Required. The sys\_id of the item to purchase.

</td></tr><tr><td>

request.special\_instructions

</td><td>

String

</td><td>

Instructions to follow when processing the order.

</td></tr><tr><td>

request.sysparm\_quantity

</td><td>

String

</td><td>

Quantity of the specified item to purchase.Default: 1

</td></tr><tr><td>

request.sysparm\_requested\_for

</td><td>

String

</td><td>

The sys\_id of the user for whom the item is requested.Default: Session user

</td></tr><tr><td>

request.variables

</td><td>

Array

</td><td>

Questions and customer answers associated with the item.

</td></tr><tr><td>

request.variables.var\_name

</td><td>

String

</td><td>

Name of the question.

</td></tr><tr><td>

request.variables.var\_value

</td><td>

String

</td><td>

Customer's response to the associated question.

</td></tr></tbody>
</table><table id="table_o4w_b4d_zz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON key/value pairs

</td><td>

Output if two-step checkout is enabled:```
{
  'cart_id' : '<sys_id of the cart to which the items were added>'
}
```

 Output if two-step checkout is disabled:

 ```
{
  'request_id' : '<sys_id of the generated request>',
  'request_number' : '<Number of the generated request>'
}
```

</td></tr></tbody>
</table>```

var cart = new sn_sc.CartJS();
var request =
{
  'sysparm_id': '0d08837237153000158bbfc8bcbe5d02',
  'sysparm_quantity': '1',
  'variables':{
    'carrier': 'at_and_t_mobility',
    'data_plan': '500MB',
    'duration': 'eighteen_months',
    'color': 'slate',
    'storage': 'sixtyfour'
  }
}
var cartDetails = cart.orderNow(request);
gs.info(cartDetails);
```

Output

```

// If two-step checkout is enabled:
{"cart_id":"55384df3c322320076173b0ac3d3aec5"}

// If two-step checkout is disabled:
{"request_id":"4c690137c322320076173b0ac3d3ae03", "request_number": "REQ0010003"}
```

## CartJS - setDeliveryAddress\(String address\)

Sets the delivery address for the current cart.

|Name|Type|Description|
|----|----|-----------|
|address|String|Delivery address for the current cart.|

|Type|Description|
|----|-----------|
|void| |

```

      var cart = new sn_sc.CartJS();
      cart.setDeliveryAddress("Brasilia, Brasil"); 
      
```

## CartJS - setRequestedFor\(String user\)

Sets the sys\_id in the sys\_user record of the user for whom the cart is requested.

|Name|Type|Description|
|----|----|-----------|
|user|String|sys\_id to be set in the sys\_user record of the user for whom the cart is requested.|

|Type|Description|
|----|-----------|
|void| |

```

var cart = new sn_sc.CartJS();
cart.setRequestedFor("039c516237b1300054b6a3549dbe5dfc")

```

## CartJS - setSpecialInstructions\(String specialInstructions\)

Sets the special instructions for the current cart.

|Name|Type|Description|
|----|----|-----------|
|specialInstructions|String|Special instructions for the current cart.|

|Type|Description|
|----|-----------|
|void| |

```

      var cart = new sn_sc.CartJS();
      cart.setSpecialInstructions("Delivery before 8 AM."); 
   
```

## CartJS - submitOrder\(Map request\)

Updates special instructions, requested for, and delivery address from the **request** parameter and performs the cart checkout. Use this API to modify the mentioned parameters of the cart and perform the cart checkout simultaneously. Missing parameters in the **request** object will have their default value.

<table id="table_ymx_brd_zz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

request

</td><td>

Map

</td><td>

JSON object that contains details of the cart to be submitted. ```
{
  'special_instructions': "String",
  'requested_for': '"String",
  'delivery_address': "String"
}
```

</td></tr><tr><td>

request.special\_instructions

</td><td>

String

</td><td>

Special instructions to include with the order.

</td></tr><tr><td>

request.requested\_for

</td><td>

String

</td><td>

Sys\_id of the user who the order is requested for.Default: The current user.

Table: User \[sys\_user\]

</td></tr><tr><td>

request.delivery\_address

</td><td>

String

</td><td>

Delivery address for the order.

</td></tr></tbody>
</table><table id="table_zmx_brd_zz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON

</td><td>

Structure of the cart.```
{
  'request_id' : 'sys_id of the generated Request',
  'request_number' : 'Number of the generated Request'
}
```

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var cart = new sn_sc.CartJS();
var request =
{
  'special_instructions' : 'Delivery only in working hours',
  'requested_for' : '62826bf03710200044e0bfc8bcbe5df1',
  'delivery_address' : "Brasilia, Brasil",
};
var requestDetails = cart.submitOrder(request);
gs.info(JSON.stringify(requestDetails));
```

Output:

```
{"request_id":"6eed229047801200e0ef563dbb9a71c2", "request_number": "REQ0000001"}
```

## CartJS - updateItem\(Map request, String cart\_item\_id\)

Updates an item in the cart.

<table id="table_zvx_npd_zz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

request

</td><td>

Map

</td><td>

A JSON object that contains details of the catalog item to be updated.The structure of the request object is:

 ```
{
    'sysparm_quantity' : item_quantity,
  'sysparm_requested_for' : requested_for,
  'variables' : {
    'var_name' : 'var_value',
    ...
  }
}
```

 -   item\_quantity: Number of items to be added. Default value is 1.
-   var\_name: Name of the question.
-   var\_value: Value of the answer \(Not the display value\).

</td></tr><tr><td>

cart\_item\_id

</td><td>

String

</td><td>

sys\_id of the cart item to be modified.

</td></tr></tbody>
</table><table id="table_awx_npd_zz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON

</td><td>

Details of the cart.```
{
  'subtotal': value,
  'items':[
    {
    itemName:'',
    quantity:'',
    price:'',
    recurring_price:''
    }
    ...],
  ...
}
```

</td></tr></tbody>
</table>```
var cart = new sn_sc.CartJS();
var request =
{
  'sysparm_quantity': '1',
  'variables':{
    'carrier': 'at_and_t_mobility',
    'data_plan': '500MB',
    'duration': 'eighteen_months',
    'color': 'slate',
    'storage': 'sixtyfour'
  }
};
var cart_item_id = "4d69b672c322320076173b0ac3d3ae79";
var cartDetails = cart.updateItem(request, cart_item_id);
gs.info(cartDetails);

```

Output

```

{ "cart_id":"35ec9e8947a13200e0ef563dbb9a7109", "items":[ { "cart_item_id":"35ec9e8947a13200e0ef563dbb9a710a", "catalog_item_id":"0d08837237153000158bbfc8bcbe5d02", "item_name":"Apple iPhone 5", "localized_price":"$799.99", "localized_recurring_price":"$30.00", "price":"$799.99", "quantity":"1", "recurring_frequency":"Monthly", "recurring_price":"$29.00" } ] "subtotal":"$799.99" }
```

