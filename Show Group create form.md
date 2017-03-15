#### Date: 15/03/2017

#### Description: This document explains the code flow of showing group create form.

#### Step 1:

Function **showGroupCreateForm** will be called first from index.php to controller. when user clicks on add button in groups it calls this function and this function redirect to the create form of group.

- Function **showGroupCreateForm** takes the list data object and gives to the group create view.
- In action, function **showGroupCreateForm** will be called from GroupsView.php which display the create form tpl page.
- The display tpl page will be **groupCreateForm.tpl** in views folder.
