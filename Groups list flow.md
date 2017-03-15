#### Date: 15/03/2017

#### Description: This document explains the code flow of getting display of all the groups list.

#### Step 1:

Function **controlGroupsListFlow** will be called first from index.php to controller which takes the inputs from the user. when user clicks on groups in side bar it will call this function. From this function we call the wsdl to get the groups list and displays.

- Function **createGroupListInputVO** takes the inputs array and send to data file and prepares the list object to get the group list. It pepares the input to group wsdl.
- In action, first getting the user id and append to input array by function **getUserID**.
- Function **createGroupListInputVO** in GroupsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create group.
- The parameters will be user id, Module name and Action name, query, sub action, offset.
- Result returns the group list value object array to controller.


#### Step 2:

- Function **getGroupsList** used to call the wsdl call for getting the Group list.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getListArray** in GroupsWS.php is used to send data to wsdl for getting the group list array using the **get_entry_list**.
- Creating the parameters and passing the parameters to wsdl call which returns the groups list result to controller.


#### Step 3:

- If **ajaxcall == yes**, function **showGroupPaginationList** takes the list data object and gives to the group view Pagination to display the group list.
- In action, function **showGroupPaginationListView** from GroupsView.php will display the groups list in pagination view.
- The display tpl page will be **GroupsViewPaginationForm.tpl** in views folder.

#### Step 4:

- If **ajaxcall != yes**, function **showGroupList** takes the list data object and gives to the group view to display the group list.
- In action, function **showGroupListView** from GroupsView.php will display the groups list view.
- The display tpl page will be **GroupsViewForm.tpl** in views folder.
