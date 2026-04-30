---
title: Sample ASP Script for unencrypted single sign-on
description: This sample ASP.NET code creates a simple authentication portal and passes an unencrypted HTTP header as a URL parameter.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Sample ASP Script for unencrypted single sign-on

This sample ASP.NET code creates a simple authentication portal and passes an unencrypted HTTP header as a URL parameter.

This sample assumes:

-   The web server supports ASP.NET
-   The target instance is `https://<instance name>.service-now.com/`
-   SiteMinder or another single sign-on application has pre-authenticated the user
-   The target instance expects an HTTP header of SM\_USER

Change the ASP code to redirect users to the proper instance and create the proper HTTP header.

```
<html xmlns = "http://www.w3.org/1999/xhtml" > <head  runat = "server" > <title >Portal Page Login </ title > <%--    <meta http-equiv = "REFRESH" content = "0;url=https://<instance name>.service-now.com/">--%>
 
     <script  runat = "server" >
 
        public void go_to(object sender, EventArgs e)
        {
            ////Send URL parameters
            String URL = urlBox.Text + "?SM_USER=" + userNameBox.Text;
            Response.Redirect(URL);
        }
     </ script >  
 

  </ head > <body > <form id = "form1"  runat = "server" > <h2 >< b > Portal Page Login  </ b >< / h2 > <hr style = "position: static" / > <br / > <asp:Label ID = "Label2"  runat = "server"  Font- Size = "Larger" Height = "21px" Style = "position: static"Text = "Instance URL:" Width = "113px" >< / asp:Label> <asp:TextBox ID = "urlBox"  runat = "server"  Font- Size = "Large" Style = "position: static" >< / asp:TextBox> <br / > <br / > <asp:Label ID = "Label1"  runat = "server"  Font- Size = "Larger" Height = "17px" Style = "position: static;"Text = "User Id:" Width = "113px" >< / asp:Label> <asp:TextBox ID = "userNameBox"  runat = "server"  Font- Size = "Large" Style = "position: static;" >< / asp:TextBox> <br / > <br / > <asp:Button ID = "Button1"  runat = "server" Height = "39px" Style = "position: static;" Text = "Ok"Width = "88px" OnClick = "go_to" / > </ form > </ body > </ html >
```

![A designer](../image/Designer.jpg "Designer")

**Parent Topic:**[Inbound web service examples](../../../integrate/examples/concept/c_InboundWebServiceExamples.md)

