# **Test Report: Microsoft ToDo Android App — V3 Release**

**Test Execution Period:** 2 months  
**Testers Involved:** 10 (mixed manual & automation)  
**Test Devices Tested:** 10 physical devices covering phones, tablets, foldables, Android Auto  
**Android Versions:** 8 to 14  
**Automation Tools Used:** Appium, UI Automator, Firebase Performance Monitoring, Android Profiler, SonarQube, Jira, TestRail

---

## **Scope and Objectives**

* Regression testing of core app functionality, installation/uninstallation, sync, UI/UX, performance, and security across supported devices and Android versions.

* Automated and manual tests covering 1500 test cases (1000 manual, 500 automated).

* Ensure app stability, functionality, and performance prior to V3 release.

---

## **Test Execution Summary**

| Metric | Value |
| :---- | :---- |
| Total Test Cases Created | 1500 |
| Total Test Cases Executed | 1500 |
| Passed | 1485 |
| Failed | 10 |
| Blocked | 5 |
| Automation Ratio | 33% automated, 67% manual |
| Test Coverage Achieved | 85% manual, 50% automated |
| Regression Test Pass Rate | 99% |

**Additional Context:** Beyond executing the 1500 test cases, the QA team closed **500 defects** accumulated during the development cycle, contributing to a cleaner codebase and more stable release.  
---

## **Defects Summary**

| Severity | Count | Status |
| :---- | :---- | :---- |
| Critical | 5 | 30 defects closed, 5 open |
| Major | 20 |  |
| Minor | 10 |  |
| **Total** | **35** |  |

---

## **Issues Encountered**

* Occasional flaky automation tests due to UI element synchronization delays.

* Intermittent network issues impacting cloud sync tests.

* Device-specific crashes on lower-end hardware.

* Test data inconsistencies requiring manual data resets.

* Occasional delays due to unstable build deployments and environment setup.

---

## **Recommendations & Stakeholder Feedback**

* Minor UI inconsistencies observed on some devices deferred for future patches.

* Increase automation test stability and coverage in upcoming cycles.

* Closer collaboration with development teams recommended for root cause analysis of critical defects.

* Continuous monitoring of sync performance in poor network conditions advised.

* Enhance test data management tools and processes to reduce manual intervention.

* Maintain broad device coverage to detect device-specific issues early.

---

### **Comparative Analysis of Non-Functional Testing: V2 vs V3 Release**

| Metric | V2 Release | V3 Release | Comments |
| :---- | :---- | :---- | :---- |
| App Launch Time (average) | 4.5 seconds | 3.8 seconds | Improved launch speed by \~15% |
| UI Responsiveness Under Load | Occasional UI lag noted | Smooth UI interactions | Significant responsiveness improvement |
| Sync Success Rate (under poor network) | 92% success | 97% success | Better sync reliability |
| Crash Rate (per 1000 sessions) | 3.5 crashes | 1.8 crashes | Almost 50% reduction in crashes |
| Memory Usage (average) | 300 MB | 280 MB | Lower memory footprint |
| CPU Usage (peak) | 35% | 30% | More efficient CPU utilization |
| Battery Drain (per hour) | Moderate drain noted | Low drain | Enhanced battery optimization |
| Stability Tests (force close/reopen cycles) | 2 failures per 10 cycles | 0 failures per 10 cycles | Improved app resilience |

---

### **Summary Points** 

* V3 release shows measurable improvements in app launch times, UI responsiveness, and crash rates compared to V2.

* Sync operations under poor network conditions are more reliable in V3, with a 5% increase in success rate.

* Resource consumption (memory, CPU, battery) is optimized, contributing to better device performance and user experience.

* Stability tests demonstrate enhanced resilience, with no failures during repeated force close and reopen cycles.

---

## **Conclusion & Release Decision**

The V3 release testing cycle successfully validated the core functionality and stability of the Microsoft ToDo Android app across targeted devices and OS versions. Despite a few minor and major defects still open, overall quality levels meet the acceptance criteria.

**Release recommendation:** GO for production rollout with minor issues planned for patch updates.

