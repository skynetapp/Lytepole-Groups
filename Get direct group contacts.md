#### Date: 15/03/2017

#### Description: This document explains the code flow of getting group contacts directly.

#### Step 1:

Function **controlDirectGetGroupContacts** will be called first from index.php to controller calls the group contacts using ajax.

- Function **getDirectGroupsContactList** takes the input data and gives the contacts list directly from DB without using WSDL.
- in action, first it calls the user id and append to input array using function **getUserID**.
- wsdl client connection will be set by function **setWSDLHandle**.
- Function **getDirectGroupContactSListArray** is used to get the contacts list array using database.
- It gets the DB connection and prepares the query which returns the contacts list array as result.

