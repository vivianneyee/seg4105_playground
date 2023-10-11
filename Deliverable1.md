## Problem
As of right now, our mobile app has no login or signup options so users cannot save their data to their account. To be able to access the features of the app, users must have their own account and be authenticated. Users can have either a  student or teacher account, each having their own separate UIs and unique functions. The main goal of the app is to provide classroom and personal organization tools. There is no way to save users preferences, classes, and schedules without them having their own accounts. Without a way for users to access their account and a way for new users to create an account, the app is essentially pointless. 
## Appetite
Our goal is to create a simple signup and login experience that allows users to easily create a new account, and then login to their account. The user data will be stored in AtlasDB which will take care of password encryption. We also want to have a verification method where users will need to verify their account to ensure users are in fact real. The solution, including frontend, backend, and testing, should be implemented within a 6-week timeframe by a team of 2 developers. 
## Solution
The provided solution to this problem is to implement a login page and a signup page. The login page will ask users to input their credentials and then sign them into their account once successfully authenticated. If there are any errors within the login process (e.g. incorrect password), then the UI will display an error message. If the user does not have an account, they will be able to find a link to the signup page where they can input the necessary fields for their new account, including their email, a password, and which type of account they want to create (student or teacher). Once a user successfully creates their account, they will receive a pop up message telling them to verify their account and then be redirected back to the login page. If there are any errors creating an account (e.g. invalid input), the user will see an error message telling them what the issue is that is preventing the creation of their account.

The flow of the solution as well as the pieces needed to implement it can be seen by the breadboard below:
![image](https://github.com/vivianneyee/seg4105_playground/assets/55165979/d12f660c-3e5b-4238-a448-7ff4a296cdc8)

Additionally, a simple sketch of the idea can be seen below:
![image](https://github.com/vivianneyee/seg4105_playground/assets/55165979/1cccafb4-a37f-48b1-98ce-4d52982982fa)


## Rabbit Holes
One potential complication to this project is using school emails for authentication. It would be nice to have users use their school accounts to be able to sign in to our app, but this comes with several unknowns. One issue is that we would require permission and access to the school accounts which could be a tedious process or even a no-go. Another issue is that school accounts can be hosted by different third party services for each different school, which would push this project beyond the allotted time-frame. We should avoid this and allow users to use any email unless there is a simple and fast way to connect school accounts.

Another unknown is multifactor authentication. Although this would increase account security, it could introduce complexity that will push this project beyond the 6-week time frame. We should consider implementation details for multifactor authentication carefully before committing to this feature. 

## No Gos
One area that shall be avoided in this project is excessive data collection. Users will not be required to input any information beyond what is necessary for user authentication. They will only be expected to provide their email, password, and role (student or teacher). Any additional personal information is a security risk, especially since we are dealing with children. 
