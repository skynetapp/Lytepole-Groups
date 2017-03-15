#### Date: 15/03/2017

#### Description: This document explains the code flow of creating contacts for group.

#### Step 1:

Function **controlGroupCreateFlow** will be called first from index.php to controller which takes the inputs from the user. when user enters data in group new create form and click on save this function will call and using the wsdl it will create contacts for group.

- Function **createGroupListInputVO** takes the inputs array and send to data file and prepares the list object to get the group list. It pepares the input to group wsdl.
- In action, first getting the user id and append to input array by function **getUserID**.
- Function **createGroupListInputVO** in GroupsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create group.
- The parameters will be user id, Module name and Action name, query, sub action, offset.
- Result returns the group list value object array to controller.


#### Step 2:

- Function **createGroup** used create a new group.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **createGroup** in GroupsWS.php will create a new group using wsdl call **set_entry**.
- Result returns the group id to controller.

#### Step 3:

- Function **addContactsInputVO** takes the input data and prepares the input value object for crearing a new contact.
- In action, function **addContactsInputVO** gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to add contacts to group.
- The input parameters are contactsSelectedName,contactsSelectedPhone,contactsSelectedId,record,name.
- Result returns Add Contact list value object array to controller.


#### Step 4:

- Function **addContactsToGroup** used to call the wsdl call to add contacts to group.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **addContactsToGroup** in GroupsWS.php is used add contacts for the group the wsdl calls(set_entries, set_relationship).
- Creating parameters and set the relation which returns the contact id as result.
- Header location will be redirected to action -> DetailView with record id.



