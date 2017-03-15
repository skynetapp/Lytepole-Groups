#### Date: 15/03/2017

#### Description: This document explains the code flow of detail view of selected group.

#### Step 1:

Function **controlGroupDetailViewFlow** will be called first from index.php to controller which takes the inputs from the user. when user clicks on arrow button in groups list it shows the detail view of the select group based on the record id.

- Function **createGroupListInputVO** takes the inputs array and send to data file and prepares the list object to get the group list. It pepares the input to group wsdl.
- In action, first getting the user id and append to input array by function **getUserID**.
- Function **createGroupListInputVO** in GroupsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create group.
- The parameters will be user id, Module name and Action name, query, sub action, offset.
- Result returns the group list value object array to controller.


#### Step 2:

- Function **getGroupsContactList** used to call the wsdl call for getting the Group contacts list.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getGroupContactSListArray** in GroupsWS.php is used to send data to wsdl for getting the group contact list array using the **get_entry_list**.
- Creating the parameters and passing the parameters to wsdl call which returns the groups contact list result to controller.


#### Step 3:

- Function **createGroupsContactsListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- In action, function **createGroupsContactsListDataObject** will be called from GroupsData.php which gets the values from input array and sets the values for list data object to pass for creating group contact data.
- The input list array parameters are next_offset,query_date,name,id,email,phone,work phone,mobilephone,iphone.
- Result returns the group contacts data object array to controller.


#### Step 4:

- Function **showGroupDetailView** takes the list data object and gives to the group Detail view.
- In action, function **showGroupDetailView** will call the display page from GroupsView.php.
- The display tpl page will be **GroupsDetailView.tpl** in views folder.
