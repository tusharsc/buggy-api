# Problem Report
as Problem statement provides 
* The app when it comes up will have 2 users created in the system -
  * `user1@gmail.com` with password `user1ABC`
  * `user2@gmail.com` with password `user2ABC`
  
  * user1@gmail.com cant login but user2@gmail.com can
* Similarly I try it out feature on the swagger page with for the `/login` API to simulate this.
 then i fixed this problem checking database, becoz in database there is duplicate LoginId in user table, thats why it gets fails to login with user1. 
 
 *In this scenario there is db folder , in that using liquibase library values are inserted in table user while database get created.
 * that values 1 st row is repeated,that i remove from changelog.xml file
 * after that i again run the application and debug and execute the login api with user1 , it get successful.
