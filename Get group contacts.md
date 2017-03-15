#### Date: 15/03/2017

#### Description: This document explains the code flow of getting group contacts.

#### Step 1:

Function **controlGetGroupContacts** will be called first from index.php to controller which calls the group contacts using ajax.

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

- Function **GetGroupsContactsListDataObjectArr** creates a list object array for the data get from wsdl and passes to view page.
- Return result N/A.
