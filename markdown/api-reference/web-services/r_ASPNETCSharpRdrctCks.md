---
title: Sample ASP.NET with C Sharp redirect with cookies
description: This sample ASP.NET code creates a simple authentication portal and passes an unencrypted HTTP header as a cookie.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Sample ASP.NET with C Sharp redirect with cookies

This sample ASP.NET code creates a simple authentication portal and passes an unencrypted HTTP header as a cookie.

**Note:** Functionality described here requires the **Admin** role.

**Note:** Cookies are domain specific and cannot be used across different network domains. The only domain that can read a cookie is the domain that sets it. It does not matter what domain name you set. If you do not have an option of your SSO portal being in the same network domain as your ServiceNow instance \(for example, in an on-premisis deployment, an alternative is to pass the SSO token using URL **GET** or **POST** parameters.

This sample assumes:

-   The web server supports ASP.NET and C\#
-   The target ServiceNow instance is `https://<instance name>.service-now.com/`
-   SiteMinder or another single sign-on application has pre-authenticated the user
-   The target ServiceNow instance expects an HTTP header of SM\_USER

Change the ASP code to redirect users to the proper ServiceNow instance.

```
<html xmlns="http://www.w3.org/1999/xhtml" >
<head runat="server">
    <title>Portal Page Login</title>
<%--    <meta http-equiv="REFRESH" content="0;url=https://<instance name>.service-now.com/">--%>
 
</head>
<body>
    <form id="form1" runat="server">
    <h2><b> Portal Page Login </b></h2>
        <hr style="position: static" />
         <br />
         <asp:Label ID="Label2" runat="server" Font-Size="Larger" Height="21px" Style="position: static"
            Text="Instance URL:" Width="113px"></asp:Label> 
        <asp:TextBox ID="urlBox" runat="server" Font-Size="Large" Style="position: static"></asp:TextBox><br />
        <br />
         <asp:Label ID="Label1" runat="server" Font-Size="Larger" Height="17px" Style="position: static;" Text="User Id:" Width="113px"></asp:Label> 
        <asp:TextBox ID="userNameBox" runat="server" Font-Size="Large" Style="position: static;"></asp:TextBox>
 
        <br />
        <br />
        <asp:Button ID="Button1" runat="server" Height="39px" Style="position: static;" Text="Ok"
            Width="88px" OnClick="Button1_click" />
    </form>
</body>
</html>
</asp>
```

The following C\# code handles the OnClick button event for the form. The code:

-   Creates the cookie "SM\_USER"
-   Performs a redirect to the URL specified on the ASP form.

Change the C\# code to create the proper cookie name.

```
using System;
using System.Data;
using System.Configuration;
using System.Web;
using System.Web.Security;
 
public partial class _Default : System.Web.UI.Page 
{
    protected void Page_Load(object sender, EventArgs e)
    {
 
    }
    protected void Button1_click(object sender, EventArgs e)
    {
        try
        {
            HttpCookie myCookie = new HttpCookie("SM_USER");
            myCookie.Value = userNameBox.Text;
            Response.Cookies.Add(myCookie);
            Response.Redirect(urlBox.Text);
 
        }catch {} 
    }
}
```

**Parent Topic:**[Inbound web service examples](../../../integrate/examples/concept/c_InboundWebServiceExamples.md)

