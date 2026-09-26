5 Smoke Test cases:

TC 1\.

1. Description : New User is signed in after first install  
2. Preconditions: Test Environment set up, Application/Build already deployed/installed, Credentials provided for an user with no previous data on the account  
3. Steps  
   1. Open application  
   2. Enter provided credentials (username/password)  
   3. Check main screen after log in  
4. Pass criteria : user is signed in \- check username on top of the left menu, and default app menu should be displayed, no data populated in the app  
5. Fail criteria : user is not signed in \- check username on top of the left menu, because of an error or the default app menu is not displayed after sign in or there is data available in the app  
6. Test duration : 30s  
7. Test Data : not needed for this test

TC 2\.

1.  Description :  Create a new task  
2. Preconditions: User is signed in, application opened on the main screen  
3. Steps:  
   1. Open Task  
   2. Open Plus icon  
   3. Add a name  
   4. Set a due date \- Pick date : this day next month  
   5. Add remind me  
   6. Repeat Daily  
   7. Press the arrow to confirm  
4. Pass criteria : the task was created and the task name is valid and the due date is valid and remind me is enabled and Repeat is set to Daily  
5. Fail criteria  : the task was not created or the task name is not valid or the due date is not the date set at step d. or remind me is not checked or repeat is not set to daily  
6. Test duration : 1 min  
7. Test data : app is populated with random data, including tasks.

TC 3\.

1. Description :  Add a new account in the app  
2. Precondition: Existing user1 already signed in, with data populated inside the app. User2 account already created.  
3. Steps:  
   1. Go to the signed in Account \- Add account  
   2. Sign in with another, existing account.  
   3. Check manage accounts  
4. Pass criteria: second user is signed in and both user appear as accounts  
5. Fail criteria : the second user is not visible/signed in or an error occurred while signing in  
6. Test duration: 30s  
7. Test data: one existing user already signed in, app is populated with random data

TC 4\.

1. Description :  Mark tasks as important  
2. Precondition: Existing user already signed in, with data populated inside the app, including different tasks  
3. Steps:  
   1. Go to Tasks tab  
   2. Click on the Star icon for the first and last task in the list  
   3. Go to Important tab  
4. Pass criteria: the first and the last tasks are present in the Important tab area  
5. Fail criteria : one or both tasks are not present in the Important tab area or other task than the two added is present  
6. Test duration: 30s  
7. Test data: one existing user already signed in, app is populated with random data including several tasks  
   

TC 5\.

1. Description : Sync data after login with the same user, on another device   
2. Precondition : Existing user signed in on device1, app is populated with data, all kinds of. device2 with only the app installed.  
3. Steps:  
   1. Go to device2 and open the app  
   2. Sign in with the same user  
   3. Check existing data after sign in  
4. Pass criteria : user is signed in with no errors and all data should be synced between devices  
5. Fail criteria: user is not signed in or at least one data/item is missing from the app on the second device.  
6. Test duration: 5 min  
7. Test data: data added in all areas of the app  
   

3 Critical test cases for Share a list

TC 1\.

1. Description : Share via invite link \- copy to clipboard  
2. Precondition : an user signed in, existing list with tasks prepopulated  
3. Steps:  
   1. Open existing list  
   2. Click on the Share list option  
   3. Choose Invite via option  
   4. Choose to copy to clipboard  
   5. Paste data into a notes app  
4. Pass criteria: check the pasted content to see its content \- it should contain a link  
5. Fail criteria: Share list option does not open, Invite via option does not open sharing Android menu, pasted data is invalid \- missing the link  
6. Test duration : 1 min  
7. Test data : a lists with several task 

TC 2\.

1. Description : Check the link validity through a 3rd party app  
2. Precondition : user signed in, existing list with tasks prepopulated, whatsapp android app installed, at least 1 contact created.  
3. Steps:  
   1. Open existing list  
   2. Click on Share list option  
   3. Choose Invite  via option  
   4. Choose to share it via whatsapp message  
   5. Select an existing whatsapp contact and Confirm  
   6. Check in whatsapp app the message received  
   7. Open the link  
4. Pass criteria: the link will open a sign in webpage and it contains a list invitation text from Microsoft TODO and a hyperlink to login in and a Create new user hyperlink  
5. Fail criteria: the opened webpage does not have the expected text or hyperlinks included  
6. Test duration : 2 minutes  
7. Test data: a lists with several tasks

TC 3\.

1. Description : the shared list is visible to the invited user  
2. Precondition: one user signed in on device1, second user signed in on device 2, a list with tasks created.  
3. Steps:  
   1. Open existing list  
   2. Click on Share list option  
   3. Choose invite via option  
   4. Choose to share it via clipboard  
   5. Paste only the url into a browser window  
   6. Login with second user credentials   
   7. Open application on device2 where second user is signed in  
4. Pass criteria: second user signed in on the second device can see the shared list with all details : list name and tasks should be accurate  
5. Fail criteria: shared list is not visible for the second user or tasks are missing from it  
6. Test duration : 3 minutes  
7. Test data : lists with tasks populated

Bug report  
Description : Application crashes after setting Airplane mode on the device and signing in.   
Summary : If the user signs in right after the device is set to Airplane mode, so no network connectivity, the application will crash with the following error.  
Steps to reproduce:   
	Open application  
	Enter user1 credentials but do not press Sign in  
	Switch the device to Airplane mode then press Sign in  
	Application will try to connect/sign in for 10s then will crash and throw the following error.  
Severity : Critical  
Attachments: device logs and dumps, screenshot with the error, OS and device specs, user credentials if needed  
Component : Authentication  
Sprint : Current sprint  
Parent Epic : Authentication

**Additional questions as if the testing  project is an outsourced one:**

What would you recommend to the client to accomplish all the testing that is required and not go over the  
monthly hours?  
From the 240h, 60 are needed for regression testing, one tester so there are 180h remaining to complete the new features testing, automation initiative, closing fixed defects and a final smoke test on the final build.  
So 180h over 4 weeks, 45h per week for 1 tester. This time can be split like:  20 hours for new features testing, 20h for automating the regression plan and 5h for closing fixed defects.

What combination of devices would you recommend for each test run?  
The client already specified the number of devices required, the combination is already mentioned in the test strategy document and it can be like : 1 top tier phone, 1 middle tier phone from another brand (for android) but with a different OS version, DPI/Resolution and screen ratio, 1 low end tier phone from a 3rd brand, but with a different OS version, with a different DPI/Resolution and screen ratio \- in this case we cover 3 hardware specs, 3 resolution/DPi and screen aspect ratio. Then two tablets, one top tier and one low tier, with different hardware specs, different OS versions, different brand and screen specs.  
Same for IOS devices, with the difference that instead of brand it should be phone versions.

The Client typically releases every week on Friday afternoon  
○ Weeks 1 & 3 are new feature releases   
○ Weeks 2 & 4 are bug fix & regression releases  
○ If there is a 5th Friday to the month they take the week off from a release  
The strategy here should be : Friday afternoon smoke test on the new build. Week1 and week3 \- manual testing and test case writing for new features. Weeks 2 and 4 \- bug validation and automation initiative for the regression plan and if time allows, new features  
In the week with no build, only automation should be done

What additional questions would you need to ask the customer in order to start testing, or to finalize your test strategy?   
How many new features vs bug fixes would a release contain : counts for testing estimations  
Can they assure the QA team receives an installable/stable build, do they do any inhouse testing before handing the build for testing?  
How would they want to measure testing progress \- daily/weekly reports, zoom meetings, emails etc  
Does the DEV team have a unit testing framework set in place?  
Request a contact person and their availability \- PM and DEV manager

The customer would like to know when you could start off with the first testing run. What would be your answer?  
Testing can start when a stable/installable build is provided and at least one new feature in it. If it's a build with only bug fixes, as soon as there are, lets say, 5 bug fixes

