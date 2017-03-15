#### Date: 15/03/2017

#### Description: This document explains the code flow of editing group.

#### Step 1:

Function **controlGroupEditFlow** will be called first from index.php to controller which takes the inputs from the user. when user on group edit in group list view this function will call and using the wsdl it will edit group.

- Function **editContactsInputVO** takes the input data and prepares the input value object for edit contacts.
- In action, function **editContactsInputVO** will create the object array to edit contacts input data.
- Result will retrun the edit contacts input value object to controller.


#### Step 2:

- Function **editContactsToGroup** takes the input data and gives the edit contacts of group.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **editContactsToGroup** from GroupsWS.php is used to edit contacts for the group using wsdl calls(set_entries, set_relationship).
- The parameters will be name, group name,conatct name,phone,contact id,group id.
- Result returns the record id to controller.
- Header location will be redirected to group detail form based on the record id.
