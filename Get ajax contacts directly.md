#### Step 1:

Function **getAjaxContactsAddJob** will be called first from index.php to controller which is used to get all contacts directly from database using ajax without using the wsdl call in add invitees in create job while group edit.

- Function **createContactListInputVO** will be called from module **Contacts -> ContactsAction.php** takes the input data and prepares the input value object to get the contact list. Its pepare the input to contact wsdl.
- In action, first getting the user id and append to input array by function **getUserID**.
- Function **createContactListInputVO** in ContactsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create group.
- The parameters will be user id, Module name and Action name, query, sub action, offset.
- Result returns the contact list value object array to controller.


#### Step 2:

- Function **getContactsList** used to call the wsdl call for getting the contacts list.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getContactListArray** will be called from ContactsWS.php which is used to send data to wsdl for getting the contacts list array using the **get_entry_list_con**.
- The parameters are session id, module name,query,orderby,offset,max result,deleted.
- Result returns the contacts list array to controller.


#### Step 3:

- Getting the entry list values in for loop and displaying the contacts directly.
