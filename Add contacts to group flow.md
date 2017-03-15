#### Step 1:

Function **controlAddContactsToGroupFlow** will be called first from index.php to controller which takes the inputs from the user. when user clicks on add contacts in group detail view and select the required contacts and click on next then this function will call to add contacts to group.

- Function **addContactsInputVO** takes the input data and prepares the input value object for creating a new contact.
- In action, function **addContactsInputVO** will be called from GroupsData.php which gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to add contacts to group.
- The parameters are contactsSelectedName,contactsSelectedPhone,contactsSelectedId,record,name.
- Result returns the add contact list value object array to controller.


#### Step 2:

- Function **addContactsToGroup** used to call the wsdl call to add contacts to group.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **addContactsToGroup** in GroupsWS.php is used to add contacts for the group using the wsdl calls(set_entries, set_relationship).
- Will create the parameters and set the relation which returns the contact id as result.
- The header location will be sending data to detail view and display the output.


