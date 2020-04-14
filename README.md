# Introduction
This is a CRM system that deals with member data which are affiliated with custom groups. Member data contains basic information about member, his/her affiliation, contact details & his family tree. 
There are two types of users in the system.
1. Member
2. Admin Users

##### Member
Member is a person whose data is available in the system. He/She only have permission to view his own or his immediate family tree's information. he cannot browse through member's database. At any point he is capable to login to the system using 1FA authentication system. To enter new data or modify available data.
Member's ability in our system is limited to above summary.

##### Admin Users
Admin users are maintainers of the application. New users can be created by already existing member. A member is authenticated with a password &/or one time otp sent to his mobile number.
An admin user has the ability to Create New Members, Import/Export bulk data, Modify existing data. However SuperAdmin has  the ability to create new roles for admin users. Which will limit each admin users to his allowed actions.

## System Summary
This is an SPA which is powered by Laravel at the back. And uses [VUE.JS V2](http://vuejs.org/v2/) for the frontend.

### Backend / Laravel
We use Laravel framework built on top of PHP in order to power this SPA. At the time of writing this document it is `~6`. 

### Frontend / Vue.js
Vue.js is used with document structure of a vue-router project. Api calls are provided by axios library.
