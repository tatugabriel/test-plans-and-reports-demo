**Microsoft ToDO Android app Test strategy**

1. Scope  
   1. Supported Android versions : lowest android versions supported \- *i would suggest here doing a research for the most 3 to 5 versions used at the point of testing*  
   2. Android Devices coverage : phones, tablet, android tv, android auto, foldables \- these include form factors, multitasking, screen resolution, aspect ratio, DPI \- *i would suggest here a research for the most 10 used devices from each category, make sure to cover all specifics*  
   3. Functional areas to cover  
      1. Application deployment \- AUTOMATED  
         1. App installation/uninstallation \- from google play or from APK directly  
         2. Fresh installs and app upgrades/reinstalls  
         3. Local data/cache cleaning after uninstall  
         4. Resync with cloud app data after reinstall+login  
         5. Installation with/without internet connectivity/airplane device mode  
         6. Installation/uninstallation while in a managed environment or restricted one)  \- *MDM enrolled device*  
            1. policies/restrictions regarding app signin/permissions/clipboard sharing/backup or sync  
            2. Parental control settings  
            3. Android restrictions : battery saving mode, background data restrictions, notifications permissions, rooted/jailbroken device  
      2. Core features \- functionality  \- AUTOMATED  
         1. My day : Visual inspection and interaction for Empty menu, Add new task/Open/Delete task. Add to important, Complete.   
         2. Important :  Visual inspection and interaction for the Empty menu, Adding/Opening/Removing items.  
         3. Planned :  Visual inspection and interaction for the Empty menu, Adding/Opening/ Removing items, Sort from This week to All.  
         4. Assigned to me : Visual inspection and interaction for the Empty menu, Adding/Opening/Removing items.  
         5. Tasks : Visual inspection and interaction for the Empty menu, Adding/Opening/Removing items.  
         6. New list : Create/Remove a list, Add tasks, Invite/Share  
         7. Groups : Create/Remove/Edit a Group, Add/remove lists  
         8. Suggestions : Open and create  
         9. Bullet points menu: Check all options  
         10. Account management : signin/signout, switch accounts, account changes at domain level (deleted user,password expire, lack of permissions etc)  
         11. Cloud sync : between devices, online/offline sync, file conflicts with the same user, poor network connectivity \- wifi/2g/3g etc  
      3. UI/UX \- functionality  
         1. Display validation with different screen layouts, DPI, resolution, aspect ratio, screen orientation and size  
         2. Android themes, default custom, animation loading  
         3. Localization \- different supported languages  
      4. Accessibility \- functionality  
         1. Screen reader  
         2. Font size/scale and color schemes  
         3. Touch interaction \- for example with gloves, multitasking in the same screen  
      5. Data retention and integrity  
         1. Device restart/Android Upgrades  
         2. App upgrades  
         3. User signout/signin  
         4. Altering cache files  
   4. Non functional areas to cover \- AUTOMATED  
      1. Performance  
         1. App launches while device is in different operating conditions/loads  
         2. UI responsiveness under device load  
         3. Sync between devices or cloud sync  under device/network loads  
      2. Application stability and resilience  
         1. Heavy data load in app \- monitor crashes or low UI performance  
         2. Force closing and reopening quickly and in sequence  
         3. Heave device load \- memory, cpu, storage  
      3. Security and data privacy  
         1. Secure authentication and sync  
         2. Data encryption \- locally or while syncing  
         3. Non authorized access attempts  
      4. Compatibility : OS versions, device coverage, Android flavours (Samsung, Pixel etc)  
      5. Battery and device resource usage : battery drain, cpu/memory drains, memory leaks, network drain   
2. Test approach  
   1. Test methods: unit, integration, system, regression, UAT  
   2. Test types : manual automated, non functional  
   3. Test design : blackbox, exploratory, whitebox   
   4. Defects and Test case tracking and management : tools like Jira, Test Rail   
   5. Smoke test plan  \- AUTOMATED  
      1. When is executed  
      2. Scope : test scenarios and end goal  
      3. Entry and Exit criteria : 2 devices and testing environment, one test data, all tests passed  
      4. Tools : manual and automation test case execution  
3. Test environments  
   1. Devices : cover a wide range of devices, from low end to high end devices, phones, tables, foldables  
   2. Android versions : Android 8 to 14 (latest)  
   3. Network : wifi/2g-5g,hotspot, airplane mode  
   4. Test accounts : different microsoft accounts, shared accounts, limited permission accounts  
   5. Emulators : Android emulator, Google Play Services  
4. Test Data \- AUTOMATED  
   1. Accounts variation  
   2. Data generation tools for quickly adding/removing items  
   3. Data security/privacy tools for monitoring sync   
5. Test Automation tools  
   1. UI testing : Appium, UI Automator  
   2. Performance : firebase, android profiler  
   3. Network simulator : android profiler  
   4. Code quality and coverage : sonarqube  
6. Entry criteria  
   1. Test environments availability  
   2. Test data availability   
   3. Test cases readiness  
   4. Tools availability  
7. Exit criteria  
   1. Test execution completion  
   2. Defects fixed and closed based on severity  
   3. Test coverage : manual and automation in % (80% automated, 20% manual)  
   4. Regression tests % execution : should be 100% and no more than 2% failed. The failed tests should not have critical/blocker issues linked to them  
   5. Sign off document : for stakeholders  
8. Risks   
   1. Device and Environment availability and readiness  
   2. Network conditions  
   3. Test data accuracy and integrity  
   4. Application stability \- too many builds in short periods of time, especially before release  
   5. Limited testing time especially for regression  
   6. Automation coverage  
9. Testing schedule  
   1. Test phases : per each testing phase \- time estimation, number of features and test cases, number of testers  
   2. Milestones and deadlines : testing signoff date, final build availability, feature freeze, code freeze, regression start/end date  
   3. Buffer time   
10. Test deliverables   
    1. Test cases : number of cases in management test cases tool, number of automated test cases  
    2. Test execution report : extracted report from management test cases tools   
    3. Defects report : new defects found in new features, regression defects, reopened defects  
    4. Performance testing report : application limits and stability overview  
    5. Test environments : configuration reports  
11. Conclusions  
    1. Summary of test strategy : overview of functional, non functional, tools, environments used for testing  
    2. Objectives set up at the beginning of testing phase : quality levels, stakeholder reporting, acceptable issues (some or minor issues can remain unfixed after release then patched)  
    3. Final Recommendations for testing : prioritization (manual vs automation), ensure collaboration between devs, PM, Qa teams and Customer, AUTOMATE the regression plan 100% 