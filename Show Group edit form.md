#### Date: 15/03/2017

#### Description: This document explains the code flow of showing group edit form.

#### Step 1:

Function **showGroupEditForm** will be called first from index.php to controller. when user clicks on edit button in group it calls this function and this function redirect to the group edit form.

- Function **showGroupEditForm** takes the list data object and gives to the group edit view.
- In action, function **showGroupEditForm** will be called from GroupsView.php which displays the tpl page.
- The display of tpl page will be **groupEditForm.tpl** in views folder.
