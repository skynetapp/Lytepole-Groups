#### Date: 15/03/2017

#### Description: This document explains the code flow of deleting the group.

#### Step 1:

Function **controlGroupDeleteFlow** will be called first from index.php to controller which takes the inputs from the user. when user clicks on delete button in group list.

- Function **createGroupListInputVO** takes the inputs array and send to data file and prepares the list object to get the group list. It pepares the input to group wsdl.
- In action, first getting the user id and append to input array by function **getUserID**.
- Function **createGroupListInputVO** in GroupsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create group.
- The parameters will be user id, Module name and Action name, query, sub action, offset.
- Result returns the group list value object array to controller.


#### Step 2:

- Function **deleteGroup** used to call the wsdl call to delete group.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **delteGroup** in GroupsWS.php will delete the group by wsdl calls as **set_entry**.
- Header location will be redirected to group list form.
