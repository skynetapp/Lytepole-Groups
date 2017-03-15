#### Date: 15/03/2017

#### Description: This document explains the code flow of Groups.

#### The Folder Structure is as follows:

 Root Directory | Sub Directory 
------------ | -------------
index.php | 
Global | LytepoleWSConnection
Lib | Smarty,nusoap
Modules | Groups
Views | GroupsViewForm, GroupsViewPaginationForm, GroupsDetailView, groupCreateForm, ContactsListViewForm, groupEditForm


#### Architecture

- After login into lytepole, when we click on **Groups** which will be in the side menu.
- When user clicks in Groups, the list of groups will be shown with members count for that group.
- User can also delete the complete group.
- When user clicks on **Add Group**, form will appear. Here we have 3 steps of procedure to create a group.
  1. Need to enter group title and description and click on next.
  2. Secondly user needs to add the contacts which will be appearing on the left side and click on next.
  3. Lastly need to click on save which will create a group with the selected contacts.
  
- In group detail page, we can see all added contacts. If the user wants to delete any of the contact from the group, he can delete it.
- Search option for group members is available to search any of the members.
- If user wants to add more contacts in a group, click on **Add Contacts to group** and can add the remaining contacts.
