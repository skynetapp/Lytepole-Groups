#### Step 1:

Function **showAddContactsForm** will be called first from index.php to controller which takes the inputs from the user. when user clicks on add contacts in group detail view this function will call and shows the eisting contacts.

- Function **createGroupListInputVO** takes the inputs array and send to data file and prepares the list object to get the group list. It pepares the input to group wsdl.
- In action, first getting the user id and append to input array by function **getUserID**.
- Function **createGroupListInputVO** in GroupsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create group.
- The parameters will be user id, Module name and Action name, query, sub action, offset.
- Result returns the group list value object array to controller.


#### Step 2:

- Function **getContactsList** used to call the wsdl call for getting the Group contacts list.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getContactListArray** will be called from GroupsWS.php which is used to send data to wsdl for getting the contacts list array using the **get_entry_list_con**.
- The parameters are session id, module name,query,orderby,offset,max result,deleted.
- Result returns the contacts list array to controller.


#### Step 3:

- Function **createContactListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createContactListDataObject** will be called from GroupsData.php which gets the values from input array and sets the values for list data object to pass for create contactsdata.
- Result returns Contacts data object array to controller.


#### Step 4:

- Function **showAddContactsForm** takes the list data object and gives to the group create contact view.
- In action, function **showContactListView** which calls the view page to show the group contact create form.
- The display tpl page will be **ContactsListViewForm.tpl** in views folder.
