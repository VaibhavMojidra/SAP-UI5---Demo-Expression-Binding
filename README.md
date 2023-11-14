# SAP UI5 Demo Expression Binding

SAP UI5 provides Expression Binding as an enhancement of the SAPUI5 binding syntax, which allows for providing expressions instead of custom formatter functions. This saves the overhead of defining a function and is recommended in cases where the formatter function has a trivial implementation like comparison of values. Expression binding is especially useful in the context of SAPUI5 XML templating where XML views with templating are preprocessed so that the SAPUI5 controller is a natural place to put custom formatter functions that are not available.

### Code Explaination

Refer to [/webapp/controller/InvoicesList.controller.js](https://github.com/VaibhavMojidra/SAP-UI5---Demo-Expression-Binding/blob/master/webapp/controller/InvoicesList.controller.js "InvoicesList.controller.js")

The `ObjectListItem` tag is used to define the properties of each item in the list. The `numberState` property of the `ObjectListItem` tag is used to define the state of the number field based on the value of the `ExtendedPrice` property of the `invoice` model. 

The expression binding syntax is used to define the value of `numberState`. The expression is evaluated at runtime and the result is used to set the state of the number field. The expression is defined as follows:

```
{=${invoice>ExtendedPrice}>10?'Error':'Success'}
```

This expression checks if the value of `ExtendedPrice` is greater than 10. If it is, then the state of the number field is set to `Error`. Otherwise, the state is set to `Success`.

----

[![Vaibhav Mojidra - 1.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Expression-Binding/master/screenshot/1.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)