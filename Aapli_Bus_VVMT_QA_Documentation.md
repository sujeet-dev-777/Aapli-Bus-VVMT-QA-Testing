# Aapli Bus VVMT Mobile Application Testing – QA Documentation

> **Honesty note:** Test cases are *designed* from the scope you provided. Only observations you reported are recorded in *Actual Result*. Everything else is `Not Executed`. 'Requirements' below are **derived test objectives** (not official VVMT requirements) and must be confirmed.

## 1. Project Information

| Field | Value |
|---|---|
| Project Name | Aapli Bus VVMT Mobile Application Testing |
| Priority | High |
| LAB | ASSIGNMENT |
| Document Owner | Sujeet Sahani |
| Date of Creation | [ENTER DATE] |
| Date of Review | [ENTER DATE] |
| Application | Aapli Bus VVMT |
| Testing Type | Manual / Functional / Exploratory Testing |
| Device | [ENTER DEVICE MODEL] |
| OS | [ENTER ANDROID VERSION] |
| Network | 4G |
| Role | QA Tester / Manual Tester |
| Document Type | LAB ASSIGNMENT / QA Testing Project (personal portfolio project, not production work) |

## 2. Test Environment

| Item | Details |
|---|---|
| Platform | Android mobile application |
| Device | [ENTER DEVICE MODEL] |
| Android Version | [ENTER ANDROID VERSION] |
| App Version | [ENTER APP VERSION] |
| Network | 4G (also Wi-Fi / No Internet for network cases) |
| Location | GPS ON / GPS OFF |
| Tools | Android Device, MS Excel, Jira (if used), Screenshots / Screen Recording, Test Documentation |
| Evidence | [Attach your own screenshots/recordings – none are included here] |

## 3. Test Data

| Data Type | Values | Note |
|---|---|---|
| Bus numbers | 101, 102, 103, 104, 105, 106 (available in your testing); 107 (not found) | 107 is a data point to verify, not a confirmed defect |
| Route | 202 to Vasai Phata | As seen on the map |
| Bus stop | Nalasopara Phata | Opens blank in observation |
| Location names | Polhar Highway Rasta; Pelhar / Vasai Phata (tester expectation) | Official name to be verified |
| Network | 4G, Wi-Fi, No Internet |  |
| Location | GPS ON, GPS OFF |  |
| Language | [LIST LANGUAGES ACTUALLY AVAILABLE IN THE APP] | Do not add languages that the app does not offer |
| Invalid inputs | 99999, ABC, @#$%, space-only, 100+ character string, XYZ123 | Test inputs only |

## 4. Test Scenarios (Module Overview)

| Module | Name | No. of Test Cases | Test Case ID Range |
|---|---|---|---|
| M01 | Application Installation and Launch | 16 | TC-001 to TC-016 |
| M02 | Application Navigation | 10 | TC-017 to TC-026 |
| M03 | Language / Localization | 13 | TC-027 to TC-039 |
| M04 | Announcements | 11 | TC-040 to TC-050 |
| M05 | Bus Search | 15 | TC-051 to TC-065 |
| M06 | Bus Details and Map | 15 | TC-066 to TC-080 |
| M07 | Live Bus Tracking | 14 | TC-081 to TC-094 |
| M08 | GPS / Location | 16 | TC-095 to TC-110 |
| M09 | Location / Area Name Accuracy | 4 | TC-111 to TC-114 |
| M10 | Bus Stops | 16 | TC-115 to TC-130 |
| M11 | Journey Planning | 17 | TC-131 to TC-147 |
| M12 | Ticket Booking | 17 | TC-148 to TC-164 |
| M13 | Payment | 12 | TC-165 to TC-176 |
| M14 | Jobs | 10 | TC-177 to TC-186 |
| M15 | Games | 21 | TC-187 to TC-207 |
| M16 | Network Testing | 16 | TC-208 to TC-223 |
| M17 | UI / UX Testing | 18 | TC-224 to TC-241 |
| M18 | Compatibility Testing | 10 | TC-242 to TC-251 |
| M19 | Performance Observation (Manual) | 10 | TC-252 to TC-261 |

## 5. Complete Test Case Repository

### Document Header

| Field | Value |
|---|---|
| Project Name | Aapli Bus VVMT Mobile Application Testing |
| Priority | High |
| LAB | ASSIGNMENT |
| Document Owner | Sujeet Sahani |
| Date of Creation | [DATE] |
| Date of Review | [DATE] |
| Application | Aapli Bus VVMT |
| Testing Type | Manual / Functional / Exploratory Testing |
| Device | [DEVICE] |
| OS | [ANDROID VERSION] |
| Network | 4G |

### Module 1: Application Installation and Launch

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-001 | Verify application installation | Verify that the application can be installed from the official app store | 1. Open Google Play Store<br>2. Search for 'Aapli Bus VVMT'<br>3. Tap Install and wait for completion<br>4. Check the app drawer for the app icon | Application should install successfully without error and the app icon should be available on the device | Not Executed | Not Executed |
| TC-002 | Verify application identity | Verify that the app icon and app name are displayed correctly after installation | 1. Install the application<br>2. Open the device app drawer<br>3. Observe the app icon and label | Correct app icon and name should be displayed without distortion or truncation | Not Executed | Not Executed |
| TC-003 | Verify first launch | Verify that the application launches successfully for the first time after installation | 1. Install the application on a device with no previous install<br>2. Tap the app icon<br>3. Observe launch and any permission/onboarding prompts<br>4. Wait for the home screen | Application should open for the first time, display required prompts correctly and reach the home screen | Not Executed | Not Executed |
| TC-004 | Verify splash screen | Verify that the splash screen is displayed correctly during launch | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Tap the app icon<br>3. Observe the screen immediately after tapping<br>4. Verify logo/branding is displayed without distortion | Splash screen should be displayed and transition to the next screen without freezing | Not Executed | Not Executed |
| TC-005 | Verify loading behaviour | Verify that a loading indicator or loading state is displayed while the app loads | 1. Tap the app icon<br>2. Observe the screen between splash and home screen | A loading indicator/state should be visible and the screen should not remain blank | Not Executed | Not Executed |
| TC-006 | Verify launch with Internet | Verify that the application launches successfully with an active 4G connection | 1. Ensure 4G data is ON and Wi-Fi is OFF<br>2. Close the app completely<br>3. Tap the app icon<br>4. Wait for the home screen | Application should launch and display the home screen with data loaded | Not Executed | Not Executed |
| TC-007 | Verify launch without Internet | Verify application behaviour when launched with no Internet connection | 1. Turn OFF mobile data and Wi-Fi<br>2. Force stop the app<br>3. Tap the app icon<br>4. Observe the screen and any message | Application should either open with available content or show a clear message; exact behaviour: Requirement Confirmation Required | Exploratory observation (formal execution pending): Internet appears necessary during initial app opening. Exact behaviour/message to be recorded during formal execution. | Not Executed |
| TC-008 | Verify launch with GPS disabled | Verify application behaviour when launched with device location turned OFF | 1. Turn OFF device location<br>2. Force stop the app<br>3. Launch the app<br>4. Observe prompts and the home screen | Application should launch without crashing and handle disabled location gracefully (prompt or fallback); exact behaviour: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-009 | Verify app restart | Verify that the app can be closed and reopened normally | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app and reach the home screen<br>3. Close the app using the Back button/exit<br>4. Tap the app icon again<br>5. Observe the home screen | Application should relaunch successfully and display the home screen | Not Executed | Not Executed |
| TC-010 | Verify launch after force stop | Verify that the app launches normally after being force stopped | 1. Open Settings > Apps > Aapli Bus VVMT<br>2. Tap Force Stop<br>3. Launch the app from the app icon<br>4. Observe the home screen | Application should launch without crash or error after force stop | Not Executed | Not Executed |
| TC-011 | Verify background/foreground behaviour | Verify that the app resumes correctly after being sent to background | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app and open any screen (e.g. map)<br>3. Press the Home button and wait 1 minute<br>4. Reopen the app from recent apps<br>5. Observe the screen state | Application should resume on the same screen without crash, blank screen or data loss | Not Executed | Not Executed |
| TC-012 | Verify app after device restart | Verify that the app works normally after rebooting the device | 1. Launch the app and use it briefly<br>2. Restart the device<br>3. Launch the app after reboot<br>4. Verify the home screen and search | Application should launch and function normally after the device restart | Not Executed | Not Executed |
| TC-013 | Verify app after update | Verify application behaviour after updating to a newer version (only if an update is available) | 1. Note the current app version and data<br>2. Update the app from Play Store<br>3. Launch the app<br>4. Verify main functions and language setting | Application should launch after update and retain core functionality; if no update is available mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-014 | Verify launch stability | Verify that the app does not crash across repeated launches | 1. Launch the app and wait for the home screen<br>2. Close the app<br>3. Repeat the launch 5 times<br>4. Record any crash or error dialog | Application should launch successfully every time without crash or 'App not responding' message | Not Executed | Not Executed |
| TC-015 | Verify app freeze/ANR | Verify that the app does not freeze during launch or first interaction | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app<br>3. Tap on a home screen option immediately after it appears<br>4. Observe responsiveness for 30 seconds | Application should respond to touch without freezing or ANR dialog | Not Executed | Not Executed |
| TC-016 | Verify launch interruption | Verify app behaviour when interrupted by an incoming call or notification during launch | 1. Tap the app icon<br>2. Trigger an incoming call/notification during loading<br>3. Dismiss the interruption<br>4. Return to the app | Application should resume without crash and complete loading normally | Not Executed | Not Executed |

### Module 2: Application Navigation

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-017 | Verify home screen | Verify that the home screen displays all main options/sections correctly | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app<br>3. Wait for the home screen to load<br>4. Observe all visible sections and options | All main sections should be displayed, readable and tappable | Not Executed | Not Executed |
| TC-018 | Verify navigation menu | Verify that each navigation menu option opens the correct screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app<br>3. Tap each menu/section option one by one<br>4. Verify the screen opened<br>5. Return to home each time | Each option should open its intended screen | Not Executed | Not Executed |
| TC-019 | Verify Back button | Verify that the device Back button returns to the previous screen from each main screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a section (e.g. Bus Search)<br>3. Press the device Back button<br>4. Observe the screen<br>5. Repeat for other sections | Back button should return to the previous screen without crash or blank screen | Not Executed | Not Executed |
| TC-020 | Verify forward navigation | Verify that moving forward through a flow (search > result > map) works correctly | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Search a bus and select it<br>4. Open map and then tap a bus icon<br>5. Observe each transition | Each forward step should open the correct screen without error | Not Executed | Not Executed |
| TC-021 | Verify screen transitions | Verify that screen transitions are smooth with no flicker or blank screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Navigate between at least 5 different screens<br>3. Observe the transitions<br>4. Note any flicker, delay or blank screen | Transitions should be smooth and complete without visual glitches | Not Executed | Not Executed |
| TC-022 | Verify navigation after refresh | Verify that refreshing a screen retains the user on the same screen with correct data | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a screen that supports refresh<br>3. Perform refresh<br>4. Observe the screen and data | Screen should refresh and remain on the same screen with valid data | Not Executed | Not Executed |
| TC-023 | Verify invalid navigation | Verify behaviour on rapid or repeated taps on navigation options | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app<br>3. Tap a menu option 5 times rapidly<br>4. Tap two different options quickly<br>5. Observe the screen | Application should open the screen once without duplicate screens, crash or freeze | Not Executed | Not Executed |
| TC-024 | Verify unexpected back navigation | Verify Back button behaviour on the home screen and mid-load | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a screen that takes time to load<br>3. Press Back while loading<br>4. Return to home and press Back<br>5. Observe behaviour | Application should handle Back during loading safely; home screen Back should follow exit behaviour | Not Executed | Not Executed |
| TC-025 | Verify exit behaviour | Verify how the application exits from the home screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app and stay on home<br>3. Press the Back button<br>4. Observe any exit prompt<br>5. Confirm exit if prompted | Application should exit cleanly (or show a confirmation); exact behaviour: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-026 | Verify navigation state after background | Verify that navigation state is retained after the app is backgrounded | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map screen<br>3. Switch to another app for 30 seconds<br>4. Return to Aapli Bus VVMT<br>5. Press Back | App should return to the same screen and Back should follow the previous navigation path | Not Executed | Not Executed |

### Module 3: Language / Localization

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-027 | Verify language change | Verify that the user can change the application language | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app<br>3. Open the language selection option<br>4. Select a different language<br>5. Observe the screen | Language change option should be available and the selected language should apply | Not Executed | Not Executed |
| TC-028 | Verify UI translation | Verify that UI/paragraph content is displayed in the selected language | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a non-English language<br>3. Navigate through the main screens<br>4. Observe paragraphs and headings | UI and paragraph content should be displayed in the selected language | Exploratory observation (formal execution pending): UI/paragraph content changes when the language is changed. | Not Executed |
| TC-029 | Verify buttons translation | Verify that button labels change with the selected language | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Change the language<br>3. Open different screens<br>4. Observe button labels | Button labels should appear in the selected language without truncation | Not Executed | Not Executed |
| TC-030 | Verify menu translation | Verify that menu items are translated after changing language | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Change the language<br>3. Open the navigation menu<br>4. Observe menu items | Menu items should be displayed in the selected language | Not Executed | Not Executed |
| TC-031 | Verify labels translation | Verify that field labels and headings are translated | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Change the language<br>3. Open search, map and bus stop screens<br>4. Observe labels and headings | Labels should be displayed in the selected language with correct fit | Not Executed | Not Executed |
| TC-032 | Verify error message translation | Verify that error/validation messages appear in the selected language | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a non-English language<br>3. Trigger an error (e.g. search an invalid bus or switch OFF Internet)<br>4. Read the message | Error messages should appear in the selected language | Not Executed | Not Executed |
| TC-033 | Verify search text translation | Verify that search placeholder and hint text change with language | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Change the language<br>3. Open the search screen<br>4. Observe placeholder, hints and buttons | Search text should be displayed in the selected language | Not Executed | Not Executed |
| TC-034 | Verify bus stop information language | Verify the language of bus stop related text after changing language | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Change the language<br>3. Open bus stops<br>4. Observe stop-related labels and names | Static labels should follow the selected language; bus stop names: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-035 | Verify announcement localization | Verify that announcement content changes according to the selected language | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Announcements and note the content<br>3. Change the application language<br>4. Reopen Announcements<br>5. Open an announcement using the eye button<br>6. Compare content before and after | Announcement content should change to the selected language if localization of announcements is expected; Requirement Confirmation Required | Exploratory observation (formal execution pending): UI/paragraph content changed but announcement content did not appear to change. Whether announcements are expected to be localized is unconfirmed. | Not Executed |
| TC-036 | Verify language persistence | Verify that the selected language remains after restarting the app | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a language<br>3. Close the app completely<br>4. Relaunch the app<br>5. Observe the language | Selected language should be retained after restarting the app | Not Executed | Not Executed |
| TC-037 | Verify language after device restart | Verify that the selected language persists after device restart | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a language<br>3. Restart the device<br>4. Launch the app<br>5. Observe the language | Selected language should be retained | Not Executed | Not Executed |
| TC-038 | Verify repeated language switching | Verify that switching language multiple times does not cause crash or mixed languages | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Switch language 5 times between all available languages<br>3. Visit home, search and map after each switch<br>4. Observe text and stability | App should remain stable and show a single consistent language each time | Not Executed | Not Executed |
| TC-039 | Verify language switch on active screen | Verify that language change is applied correctly while on a screen (immediate vs after restart) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map screen<br>3. Change the language from settings<br>4. Return to the map<br>5. Observe text | Language should be applied; whether immediate or after restart: Requirement Confirmation Required | Not Executed | Not Executed |

### Module 4: Announcements

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-040 | Verify announcement list | Verify that the announcement list is displayed | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app<br>3. Open the Announcements section<br>4. Observe the list | Available announcements should be listed with readable titles | Not Executed | Not Executed |
| TC-041 | Verify announcement loading | Verify that announcements load without long delay or blank state | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Announcements on 4G<br>3. Observe loading time and indicator<br>4. Wait for the list | Announcements should load and a loading indicator should be shown while waiting | Not Executed | Not Executed |
| TC-042 | Verify eye/view button opens announcement | Verify that tapping the eye/view button opens the announcement | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the Announcements section<br>3. Tap the eye/view button on an announcement<br>4. Observe the screen | Announcement should open and display its content | Tapping the eye/view button opened the announcement. | PASS |
| TC-043 | Verify announcement content display | Verify that the opened announcement content is complete and readable | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open an announcement using the eye button<br>3. Read the title and body<br>4. Scroll if required | Complete content should be displayed with readable text and no overlap | Not Executed | Not Executed |
| TC-044 | Verify close announcement | Verify that an opened announcement can be closed | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open an announcement<br>3. Close it using the close option/Back button<br>4. Observe the screen | Announcement should close and return to the list | Not Executed | Not Executed |
| TC-045 | Verify multiple announcements | Verify that multiple announcements can be opened one after another | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the first announcement and close it<br>3. Open the second and third announcements<br>4. Verify each content | Each announcement should show its own correct content | Not Executed | Not Executed |
| TC-046 | Verify long announcement | Verify the display of a long announcement | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the longest available announcement<br>3. Scroll to the end<br>4. Observe text wrapping and cut-offs | Long content should be fully readable with scrolling and no truncation | Not Executed | Not Executed |
| TC-047 | Verify empty announcements | Verify behaviour when no announcements are available (only if reproducible) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Announcements when no announcement exists<br>3. Observe the screen | An appropriate empty-state message should be displayed rather than a blank screen; if not reproducible mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-048 | Verify announcements without Internet | Verify announcement behaviour after network is turned OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the Announcements list<br>3. Turn OFF Internet<br>4. Open an announcement and refresh<br>5. Observe behaviour | Behaviour (cached content or error message) should be clear and the app should not crash; exact behaviour: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-049 | Verify announcement refresh | Verify that announcements can be refreshed and reflect updates | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Announcements<br>3. Perform refresh (pull-to-refresh/reopen)<br>4. Observe the list | List should refresh without duplicates or crash | Not Executed | Not Executed |
| TC-050 | Verify announcement persistence after restart | Verify announcements after app restart | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Announcements<br>3. Close and relaunch the app<br>4. Open Announcements again | Announcements should be displayed consistently after restart | Not Executed | Not Executed |

### Module 5: Bus Search

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-051 | Verify search by valid bus number | Verify that searching for an existing bus number displays the bus | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Enter a valid bus number (e.g. 101, 102, 103, 104, 105, 106)<br>4. Submit the search<br>5. Observe the result | Bus should be displayed if it exists in the application's current route data | Bus numbers 101-106 were available and found during exploratory testing. | PASS |
| TC-052 | Verify search by invalid bus number | Verify the message for a non-existent bus number | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Enter a clearly invalid number (e.g. 99999)<br>4. Submit the search<br>5. Observe the message | A 'no result' message should be displayed; app should not crash | Not Executed | Not Executed |
| TC-053 | Verify search for bus 107 | Verify search result for bus number 107 | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Enter 107<br>4. Submit the search<br>5. Observe the result<br>6. Check official route data for bus 107 | Bus should be displayed if it exists in the application's current route data | Exploratory observation (formal execution pending): Bus 107 was not found. Not classified as a defect until 107 is confirmed as an officially supported route. | Not Executed |
| TC-054 | Verify empty search | Verify behaviour when search is submitted with empty input | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Leave the field empty<br>4. Tap search/submit<br>5. Observe behaviour | No crash; message or default list should be displayed; exact behaviour: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-055 | Verify partial bus number | Verify search with a partial bus number | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Enter '10'<br>4. Observe suggestions/results<br>5. Select one result | Matching buses should be listed or suggested; exact matching rule: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-056 | Verify alphabetic input | Verify search with alphabetic input | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Enter 'ABC'<br>4. Submit the search<br>5. Observe the response | Application should show no results or a validation message without crashing | Not Executed | Not Executed |
| TC-057 | Verify special characters | Verify search with special characters | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Enter '@#$%'<br>4. Submit the search<br>5. Observe the response | Application should handle input safely without crash or incorrect results | Not Executed | Not Executed |
| TC-058 | Verify spaces in search | Verify search with leading/trailing/only spaces | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Enter ' 102 ' with spaces<br>4. Submit the search<br>5. Enter only spaces and submit | Leading/trailing spaces should be handled; space-only input should not crash; exact behaviour: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-059 | Verify very long input | Verify search with a very long text string | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Paste 100+ characters<br>4. Submit the search<br>5. Observe response | Application should handle long input without crash or UI break | Not Executed | Not Executed |
| TC-060 | Verify multiple results | Verify behaviour when multiple buses match | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Enter a prefix expected to match several buses (e.g. '10')<br>4. Observe the list<br>5. Scroll through results | All matching buses should be listed correctly with no duplicates | Not Executed | Not Executed |
| TC-061 | Verify bus stop search | Verify that a bus stop can be searched by name | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the search section<br>3. Enter a valid bus stop name (e.g. Nalasopara Phata)<br>4. Observe the results | Matching bus stops should be listed | Bus stops could be searched during exploratory testing. | PASS |
| TC-062 | Verify search result selection | Verify that selecting a search result opens the correct details | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Search a valid bus<br>3. Tap the result<br>4. Observe the opened screen | Selected result should open its correct details/map | Not Executed | Not Executed |
| TC-063 | Verify clear search | Verify that the search field can be cleared | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enter text in the search field<br>3. Tap the clear (X) option or delete text<br>4. Observe the field and results | Field should clear and the result list should reset | Not Executed | Not Executed |
| TC-064 | Verify search after network loss | Verify search behaviour when Internet is lost | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Turn OFF Internet<br>4. Search a bus number<br>5. Observe behaviour | Result or error message should be clear and app should not crash; exact behaviour: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-065 | Verify search with GPS disabled | Verify that search works when device location is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF device location<br>3. Open Bus Search<br>4. Search a valid bus number<br>5. Observe the result | Search should work as designed without location; whether GPS is required: Requirement Confirmation Required | Not Executed | Not Executed |

### Module 6: Bus Details and Map

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-066 | Verify selecting a bus opens map | Verify that selecting a bus (e.g. Bus 102) from search opens the map | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Bus Search<br>3. Search Bus 102<br>4. Select the bus from the result<br>5. Observe the screen | Map should open for the selected bus | Searched Bus 102 and selected it; the map opened. | PASS |
| TC-067 | Verify map loading | Verify that the map loads completely | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a bus to open the map<br>3. Observe the map tiles and route<br>4. Wait until fully loaded | Map tiles, route and bus markers should load without blank areas | Not Executed | Not Executed |
| TC-068 | Verify bus icon display | Verify that bus icons are visible on the route | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map for a bus (e.g. 102)<br>3. Observe the route<br>4. Look for bus icons | Bus icons should be visible on the route | Bus icons were visible on the route. | PASS |
| TC-069 | Verify bus number/details on icon tap | Verify that tapping a bus icon displays bus number/details | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map for Bus 102<br>3. Tap a bus icon<br>4. Observe the details shown | Bus number/details should be displayed | Tapping a bus icon displayed the bus number/details. | PASS |
| TC-070 | Verify bus number display | Verify that the bus number shown matches the searched bus | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Search Bus 102<br>3. Open the map<br>4. Compare the number on the screen/icon with 102 | Displayed bus number should match the selected bus | Not Executed | Not Executed |
| TC-071 | Verify route information | Verify that route information (start/end/stops) is displayed | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map for a bus<br>3. Observe the route information panel<br>4. Verify start and end | Route information should be displayed and consistent with route data | Not Executed | Not Executed |
| TC-072 | Verify bus location on route | Verify that bus icons lie on the displayed route | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Zoom to a bus icon<br>4. Compare position with the route line | Bus icon should be positioned on/near the route | Not Executed | Not Executed |
| TC-073 | Verify map zoom | Verify map zoom in and zoom out | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Use pinch zoom in and zoom out<br>4. Use double-tap<br>5. Observe the map | Map should zoom smoothly in both directions | Not Executed | Not Executed |
| TC-074 | Verify map movement | Verify map panning | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Drag the map in all directions<br>4. Observe the map | Map should move smoothly and tiles should load | Not Executed | Not Executed |
| TC-075 | Verify map refresh | Verify map/bus data refresh | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Perform refresh (or wait for auto refresh)<br>4. Observe bus positions | Bus data should refresh without map reset or crash | Not Executed | Not Executed |
| TC-076 | Verify multiple buses on map | Verify display of multiple buses on the same route | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a route with more than one bus<br>3. Observe the icons<br>4. Tap each icon | Each bus should be displayed with its own number/details | Not Executed | Not Executed |
| TC-077 | Verify bus stops on map | Verify that bus stops are displayed along the route | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map for a bus<br>3. Observe the bus stop markers<br>4. Tap a bus stop | Bus stops should be displayed and show details on tap | Not Executed | Not Executed |
| TC-078 | Verify map with GPS disabled | Verify map behaviour when device location is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF device location<br>3. Open the map for a bus<br>4. Observe the map and buses | Map should open; behaviour regarding user location: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-079 | Verify map with network disabled | Verify map behaviour when Internet is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Turn OFF Internet<br>4. Pan/zoom and refresh<br>5. Observe behaviour | App should not crash; behaviour of map/bus data: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-080 | Verify back from map | Verify Back navigation from the map | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Press Back<br>4. Observe the screen | App should return to the previous screen without crash | Not Executed | Not Executed |

### Module 7: Live Bus Tracking

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-081 | Verify bus location display | Verify that live bus location is shown on the map | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map for a running bus<br>3. Observe the bus position<br>4. Compare with the expected route | Bus location should be displayed on the map | Not Executed | Not Executed |
| TC-082 | Verify bus movement | Verify that a bus icon moves over time | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Observe a bus icon for 2-3 minutes<br>4. Note position changes | Bus position should update as the bus moves; update behaviour: Requirement Confirmation Required | Exploratory observation (formal execution pending): A yellow bus appeared to be moving. Not verified against real-world movement. | Not Executed |
| TC-083 | Verify bus status | Verify that bus status information is shown | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Tap a bus icon<br>3. Read the status/details<br>4. Note available fields | Bus status information should be consistent with the application's defined statuses; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-084 | Verify bus icon consistency | Verify consistent icon appearance for all buses | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map with multiple buses<br>3. Compare icon shape/size<br>4. Zoom in/out | Icons should be consistent and clearly visible | Not Executed | Not Executed |
| TC-085 | Verify bus colour indicators | Verify that the bus colour indicator corresponds to the status defined by the application | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Observe bus icons (green/yellow observed)<br>4. Tap each coloured bus<br>5. Compare with in-app legend/help or official documentation | Verify that the bus color indicator corresponds to the status defined by the application; Requirement Confirmation Required | Exploratory observation (formal execution pending): Green and yellow bus indicators were observed. Meaning not documented/confirmed. | Not Executed |
| TC-086 | Verify tracking refresh | Verify refresh behaviour of tracking data | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Perform manual refresh<br>4. Observe icon updates | Data should refresh and positions update | Not Executed | Not Executed |
| TC-087 | Verify location update interval | Verify how frequently bus locations update | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Note position and time of a bus<br>4. Re-check every 30 seconds for 3 minutes | Positions should update periodically; interval: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-088 | Verify multiple buses tracking | Verify simultaneous tracking of multiple buses | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a route with multiple buses<br>3. Observe all icons for 2 minutes<br>4. Tap each icon | All buses should be tracked without icon overlap issues or lag | Not Executed | Not Executed |
| TC-089 | Verify tracking with GPS disabled | Verify live tracking when device location is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF device location<br>3. Open the map<br>4. Observe bus icons and movement for 2 minutes | Tracking behaviour should be recorded; whether tracking depends on user GPS: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-090 | Verify tracking with network disabled | Verify tracking behaviour after Internet is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map showing buses<br>3. Turn OFF Internet<br>4. Observe icons for 2 minutes<br>5. Turn ON Internet and observe | Behaviour (frozen/cached/updating) should be identified; recovery on reconnect should work; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-091 | Verify delayed bus | Verify how a delayed bus is represented (if observable) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Look for a bus with delay/idle indication<br>4. Tap the bus<br>5. Compare with timing information | Delayed bus information should be clear; indicator definition: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-092 | Verify bus unavailable | Verify behaviour when no bus is currently running on a route | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a route with no active bus<br>3. Open the map<br>4. Observe the screen | An appropriate message or empty state should be shown instead of a blank map; if not reproducible mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-093 | Verify route change | Verify behaviour when switching from one bus/route to another | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map for Bus 102<br>3. Go back and select Bus 103<br>4. Observe route and icons | Previous route data should be cleared and new route displayed correctly | Not Executed | Not Executed |
| TC-094 | Verify stale data | Verify whether stale data is indicated when updates stop | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Turn OFF Internet for 5 minutes<br>4. Observe icons and any timestamp/warning | Stale data should be indicated or clearly identifiable; Requirement Confirmation Required | Not Executed | Not Executed |

### Module 8: GPS / Location

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-095 | Verify location permission allowed | Verify behaviour when location permission is allowed | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Fresh install or clear permissions<br>3. Launch the app<br>4. Allow location permission<br>5. Open the map/nearby features | App should use location and show current location/nearby data | Not Executed | Not Executed |
| TC-096 | Verify location permission denied | Verify behaviour when location permission is denied | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Reset permissions<br>3. Launch the app<br>4. Deny location permission<br>5. Use search/map/nearby features | App should not crash and should explain or provide fallback | Not Executed | Not Executed |
| TC-097 | Verify location disabled | Verify behaviour when device location is turned OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF device location<br>3. Open the app<br>4. Open map and nearby features<br>5. Observe prompts | App should handle it gracefully (prompt/fallback); exact behaviour: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-098 | Verify location enabled | Verify behaviour when device location is turned ON | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn ON device location<br>3. Open the app<br>4. Open map and nearby features | Location-based features should work correctly | Not Executed | Not Executed |
| TC-099 | Verify first permission request | Verify that the first permission request is clear and displayed once | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Install fresh<br>3. Launch the app<br>4. Observe the permission dialog<br>5. Select an option | Permission request should be clear and not repeat unnecessarily | Not Executed | Not Executed |
| TC-100 | Verify permission revoked while running | Verify behaviour when permission is revoked from settings while the app is in background | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Use the app with permission allowed<br>3. Revoke location permission from Settings<br>4. Return to the app<br>5. Use location features | App should not crash and should re-request or show a message | Not Executed | Not Executed |
| TC-101 | Verify app after permission change | Verify the app after changing permission from Deny to Allow | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Deny permission and use the app<br>3. Enable permission from Settings<br>4. Return to the app<br>5. Use location features | Location features should work after permission is allowed | Not Executed | Not Executed |
| TC-102 | Verify current location | Verify that the user's current location is displayed correctly | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable location<br>3. Open the map<br>4. Locate the current-location marker<br>5. Compare with actual position | Current location marker should be displayed near the actual position | Not Executed | Not Executed |
| TC-103 | Verify nearby bus stops | Verify that nearby bus stops are listed based on location | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable location<br>3. Open nearby bus stops<br>4. Compare listed stops with surroundings | Nearby stops should be listed and relevant to the current location | Not Executed | Not Executed |
| TC-104 | Verify nearby buses | Verify that nearby buses are shown (if feature exists) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable location<br>3. Open nearby buses/map<br>4. Observe listed buses | Nearby buses should be shown; if the feature is absent mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-105 | Verify location accuracy | Verify accuracy of the displayed user location | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable high-accuracy location<br>3. Open the map outdoors<br>4. Compare marker with a known landmark | Marker should reasonably match the actual position; accuracy tolerance: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-106 | Verify location refresh | Verify that location updates when the user moves | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Move to another location or simulate movement<br>4. Observe the marker update | Marker should update with the new location | Not Executed | Not Executed |
| TC-107 | Verify buses visible with location OFF - previously loaded data | Verify whether previously loaded bus data remains visible after turning location OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map with buses loaded<br>3. Turn OFF device location<br>4. Observe icons | Behaviour should be recorded; previously loaded data may remain visible; Requirement Confirmation Required | Exploratory observation (formal execution pending): Buses can still be visible when device location is OFF. Not yet determined whether this is previously loaded data or live data. | Not Executed |
| TC-108 | Verify live data updates with location OFF | Verify whether live bus data continues updating when location is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF device location<br>3. Open the map<br>4. Observe bus positions for 3 minutes | Updates should continue only if tracking does not depend on user GPS; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-109 | Verify current location feature with location OFF | Verify user current location feature when location is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF device location<br>3. Tap the current-location option<br>4. Observe prompt/behaviour | App should prompt to enable location or show a clear message | Not Executed | Not Executed |
| TC-110 | Verify nearby functionality with location OFF | Verify nearby bus stops/buses when location is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF device location<br>3. Open nearby bus stops<br>4. Observe the result | Nearby feature should show a message/fallback and not crash; Requirement Confirmation Required | Not Executed | Not Executed |

### Module 9: Location / Area Name Accuracy

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-111 | Verify accuracy of displayed location/area name | Verify accuracy of displayed location/area name | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable location at the test spot<br>3. Open the screen that shows the area name<br>4. Note the displayed name (e.g. 'Polhar Highway Rasta')<br>5. Compare with the official name from Google Maps/VVMT sources | Displayed area name should match the officially verified name of the location; official name needs verification before conclusion | Exploratory observation (formal execution pending): App displayed 'Polhar Highway Rasta'; tester expected a possibly more accurate name such as 'Pelhar / Vasai Phata'. Official name not yet verified. | Not Executed |
| TC-112 | Verify location name against official source | Verify the displayed name against at least two independent sources | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Record the app's displayed name<br>3. Check Google Maps and official VVMT stop list<br>4. Record both names<br>5. Compare | Differences should be documented; defect only if the app's name is confirmed incorrect | Not Executed | Not Executed |
| TC-113 | Verify location name consistency across screens | Verify the same location is named consistently across screens | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Note the area name on the map<br>3. Check the same place in search, bus stop list and route details<br>4. Compare names | Name should be consistent across screens | Not Executed | Not Executed |
| TC-114 | Verify location name after refresh/movement | Verify the area name updates correctly after refresh or movement | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Note the current area name<br>3. Refresh or move to another area<br>4. Observe the updated name | Area name should update to match the new location | Not Executed | Not Executed |

### Module 10: Bus Stops

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-115 | Verify bus stop search | Verify that bus stops can be searched by name | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open bus stop search<br>3. Enter a valid stop name<br>4. Observe the results | Matching stops should be listed | Not Executed | Not Executed |
| TC-116 | Verify bus stop selection | Verify that a bus stop can be selected from the result list | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Search a bus stop<br>3. Tap a result<br>4. Observe the screen | Selected stop should open | Not Executed | Not Executed |
| TC-117 | Verify Nalasopara Phata bus stop opens correctly | Verify that selecting 'Nalasopara Phata' displays bus stop details | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open bus stop search<br>3. Search or select 'Nalasopara Phata'<br>4. Observe the screen that opens<br>5. Wait 30 seconds<br>6. Retry 3 times and note result | Relevant bus stop details should be displayed | Exploratory observation (formal execution pending): Screen opens but appears blank. Reproduction to be confirmed during formal execution. | Not Executed |
| TC-118 | Verify bus stop details | Verify the details shown for a bus stop | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a bus stop that loads<br>3. Observe name, routes and timings<br>4. Verify against known data | Bus stop name and relevant routes/details should be displayed | Not Executed | Not Executed |
| TC-119 | Verify nearby bus stops | Verify nearby bus stops list | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable location<br>3. Open the nearby bus stops section<br>4. Observe the list | Nearby stops should be displayed relevant to the location | Not Executed | Not Executed |
| TC-120 | Verify 'See All' meaning | Verify whether 'See All' shows all bus stops or only nearby bus stops | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open nearby bus stops<br>3. Tap See All<br>4. Observe the list and heading<br>5. Compare against the full bus stop list<br>6. Check help/official documentation | 'See All' behaviour should match the application's defined meaning (all stops vs all nearby stops); Requirement Confirmation Required | Exploratory observation (formal execution pending): 'See All' shows nearby bus stops. Intended meaning not confirmed. | Not Executed |
| TC-121 | Verify 'See All' list completeness | Verify that the 'See All' list loads fully and scrolls | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Tap See All<br>3. Scroll to the end<br>4. Observe count and duplicates | List should load fully with no duplicates or missing items | Not Executed | Not Executed |
| TC-122 | Verify bus stop map | Verify that the bus stop location is shown on the map | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a bus stop<br>3. Open its map view<br>4. Verify the marker location | Stop marker should be shown at the correct location | Not Executed | Not Executed |
| TC-123 | Verify bus routes at stop | Verify that bus routes passing through a stop are displayed | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a bus stop<br>3. Observe the list of routes/buses<br>4. Tap a route | Relevant routes should be displayed and open correctly | Not Executed | Not Executed |
| TC-124 | Verify other bus stops open correctly | Verify that other bus stops open details (compare with Nalasopara Phata) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open 5 different bus stops<br>3. Observe each screen<br>4. Record any blank screens | Each bus stop should open with its details | Not Executed | Not Executed |
| TC-125 | Verify empty bus stop | Verify a stop with no upcoming bus information | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a stop expected to have no buses<br>3. Observe the screen | An appropriate empty-state message should be displayed instead of a blank screen | Not Executed | Not Executed |
| TC-126 | Verify invalid bus stop | Verify search for a non-existent bus stop | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open bus stop search<br>3. Enter 'XYZ123'<br>4. Observe the result | No-result message should be displayed without crash | Not Executed | Not Executed |
| TC-127 | Verify bus stop with GPS disabled | Verify bus stop functionality with location OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF device location<br>3. Open bus stops<br>4. Search and open a stop<br>5. Observe | Searching/opening stops should work; nearby feature behaviour: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-128 | Verify bus stop with network disabled | Verify bus stop screen when Internet is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a bus stop<br>3. Turn OFF Internet<br>4. Refresh or reopen<br>5. Observe | App should not crash; message or cached content; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-129 | Verify bus stop refresh | Verify refresh on the bus stop screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a bus stop<br>3. Perform refresh<br>4. Observe data | Data should refresh without error | Not Executed | Not Executed |
| TC-130 | Verify Back navigation from bus stop | Verify Back behaviour from stop details and See All | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open See All<br>3. Open a stop<br>4. Press Back twice<br>5. Observe screens | Back should return correctly step by step | Not Executed | Not Executed |

### Module 11: Journey Planning

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-131 | Verify journey planning availability | Verify whether a journey planning feature exists in the application | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app<br>3. Look for a journey planner/route planner option<br>4. Open it if present | If the feature exists proceed; otherwise mark all journey cases NOT APPLICABLE | Not Executed | Not Executed |
| TC-132 | Verify source selection | Verify that a source can be selected | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open journey planning<br>3. Tap the source field<br>4. Search and select a source stop | Selected source should be displayed | Not Executed | Not Executed |
| TC-133 | Verify destination selection | Verify that a destination can be selected | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open journey planning<br>3. Tap the destination field<br>4. Select a destination | Selected destination should be displayed | Not Executed | Not Executed |
| TC-134 | Verify same source and destination | Verify behaviour when both are the same | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select the same stop as source and destination<br>3. Tap search | Validation message should be displayed or no route shown | Not Executed | Not Executed |
| TC-135 | Verify valid route | Verify route result for a valid source and destination | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select valid source and destination<br>3. Search routes<br>4. Observe the result | Valid route(s) should be displayed | Not Executed | Not Executed |
| TC-136 | Verify invalid route | Verify behaviour for invalid input | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enter an invalid source/destination<br>3. Tap search<br>4. Observe | Validation/no-result message without crash | Not Executed | Not Executed |
| TC-137 | Verify no route available | Verify the message when no route exists | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select two stops with no direct route<br>3. Search<br>4. Observe | A clear no-route message should be displayed | Not Executed | Not Executed |
| TC-138 | Verify multiple routes | Verify that multiple route options are displayed | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a pair with several options<br>3. Search<br>4. Compare the options | Multiple routes should be listed clearly | Not Executed | Not Executed |
| TC-139 | Verify bus number in route | Verify the bus number shown in route results | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Plan a journey<br>3. Open a route<br>4. Verify bus numbers | Displayed bus numbers should be valid and correct | Not Executed | Not Executed |
| TC-140 | Verify bus stops in route | Verify the bus stops listed in route details | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open route details<br>3. Check the sequence of stops | Stops should be listed in the correct order | Not Executed | Not Executed |
| TC-141 | Verify route details and timing | Verify route details and timing information | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open route details<br>3. Observe duration/timing<br>4. Compare with known data | Route and timing information should be consistent | Not Executed | Not Executed |
| TC-142 | Verify route refresh | Verify refresh in journey results | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Search a route<br>3. Refresh the results<br>4. Observe | Results should refresh without crash | Not Executed | Not Executed |
| TC-143 | Verify journey with GPS | Verify journey planning with 'current location' as source | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn ON location<br>3. Choose current location as source<br>4. Plan a route | Current location should be used as the source correctly | Not Executed | Not Executed |
| TC-144 | Verify journey without network | Verify journey planning with no Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Plan a route<br>4. Observe | Clear error message without crash | Not Executed | Not Executed |
| TC-145 | Verify journey Back button | Verify Back from route results/details | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Plan a route<br>3. Open details<br>4. Press Back | Back should return to the previous screen retaining inputs | Not Executed | Not Executed |
| TC-146 | Verify long route | Verify long routes with many stops | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select far-apart stops<br>3. Open route details<br>4. Scroll | Route should be displayed completely and be scrollable | Not Executed | Not Executed |
| TC-147 | Verify incorrect route data | Verify that route data is consistent with real routes | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Pick a route<br>3. Compare against official VVMT route information | Route data should match official data; mismatches documented | Not Executed | Not Executed |

### Module 12: Ticket Booking

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-148 | Verify ticket feature availability | Verify whether ticket booking exists in the application | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Launch the app<br>3. Look for a ticket/pass option<br>4. Open it if present | If present proceed; otherwise mark all ticket cases NOT APPLICABLE | Not Executed | Not Executed |
| TC-149 | Verify ticket selection | Verify that a ticket type can be selected | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the ticket feature<br>3. Select a ticket type | Selected ticket type should be highlighted/applied; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-150 | Verify source selection | Verify source selection for ticket | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open ticket booking<br>3. Select source | Source should be selected and displayed; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-151 | Verify destination selection | Verify destination selection for ticket | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open ticket booking<br>3. Select destination | Destination should be selected and displayed; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-152 | Verify fare calculation | Verify fare for a source/destination | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select source and destination<br>3. Observe the fare<br>4. Compare with official fare chart | Fare should match the official fare; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-153 | Verify ticket quantity | Verify changing the ticket quantity | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Increase and decrease quantity<br>3. Observe fare update | Fare should update correctly; limits: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-154 | Verify valid ticket booking | Verify booking with valid data | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select valid details<br>3. Confirm<br>4. Observe result | Ticket should be generated successfully; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-155 | Verify invalid ticket booking | Verify booking with invalid data | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enter invalid combination<br>3. Attempt to confirm | Validation message should be displayed; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-156 | Verify empty fields | Verify booking with empty mandatory fields | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Leave source/destination empty<br>3. Tap confirm | Validation message should be displayed; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-157 | Verify booking confirmation | Verify the confirmation screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Complete a booking<br>3. Observe confirmation | Confirmation with correct details should be displayed; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-158 | Verify ticket generation | Verify the generated ticket content | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the generated ticket<br>3. Verify fields | Ticket should contain correct source, destination, fare, date/time; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-159 | Verify duplicate ticket | Verify behaviour on repeated booking taps | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Tap confirm multiple times quickly<br>3. Check tickets generated | Only one ticket should be generated per confirmed booking; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-160 | Verify ticket cancellation | Verify cancellation if supported | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a ticket<br>3. Look for cancel option<br>4. Cancel | Cancellation should work as per rules; if unsupported mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-161 | Verify ticket history | Verify ticket history list | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open ticket history<br>3. Observe entries | Previous tickets should be listed correctly; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-162 | Verify ticket details | Verify details of a past ticket | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a ticket from history<br>3. Verify details | Details should match the booked ticket; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |
| TC-163 | Verify QR ticket | Verify QR/digital ticket display | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a ticket<br>3. Observe QR/barcode | QR should be displayed clearly if available; otherwise NOT APPLICABLE | Not Executed | Not Executed |
| TC-164 | Verify ticket after app restart | Verify the ticket after restarting the app | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Generate a ticket<br>3. Close and relaunch the app<br>4. Open the ticket | Ticket should remain available; if the Ticket Booking feature does not exist mark NOT APPLICABLE | Not Executed | Not Executed |

### Module 13: Payment

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-165 | Verify payment availability | Verify whether payment functionality exists | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Explore the app for payment options<br>3. Open payment screen if present | If payment exists proceed; otherwise mark payment cases NOT APPLICABLE | Not Executed | Not Executed |
| TC-166 | Verify successful payment | Verify a successful payment flow (test mode/low-value only if safe) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start a booking<br>3. Proceed to payment<br>4. Complete payment | Payment should succeed and status should be displayed; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-167 | Verify failed payment | Verify behaviour for failed payment | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start payment<br>3. Simulate failure (invalid/insufficient method in test mode) | Failure message should be displayed; no ticket issued; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-168 | Verify cancelled payment | Verify behaviour when payment is cancelled | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start payment<br>3. Cancel on the payment screen | User should return safely with no charge/ticket; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-169 | Verify payment timeout | Verify behaviour on payment timeout | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start payment<br>3. Wait without action | Timeout message should be displayed; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-170 | Verify network interruption during payment | Verify behaviour if Internet drops mid payment | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start payment<br>3. Turn OFF Internet<br>4. Observe<br>5. Turn ON Internet | Clear status shown; no duplicate/uncertain charge; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-171 | Verify Back button during payment | Verify Back button on payment screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start payment<br>3. Press Back<br>4. Observe | Confirmation or safe exit; no crash; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-172 | Verify duplicate payment | Verify protection against duplicate payment | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Tap pay repeatedly<br>3. Check status | Only one payment should be processed; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-173 | Verify payment status | Verify the payment status screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Complete a payment<br>3. Observe status | Correct status should be displayed; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-174 | Verify ticket generation after payment | Verify ticket after successful payment | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Complete payment<br>3. Check tickets | Ticket should be generated after success only; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-175 | Verify payment history | Verify payment history | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open payment history<br>3. Observe entries | History should list payments correctly; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |
| TC-176 | Verify app crash during payment | Verify recovery after app is closed during payment | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start payment<br>3. Force close the app<br>4. Reopen and check status | Payment/ticket status should be consistent; applicable only if payment exists, otherwise NOT APPLICABLE. Do not perform real financial transactions unless safe and appropriate | Not Executed | Not Executed |

### Module 14: Jobs

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-177 | Verify Jobs page loading | Verify that the Jobs page loads | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the Jobs section<br>3. Wait for load<br>4. Observe | Page should load without crash | Not Executed | Not Executed |
| TC-178 | Verify Jobs empty state | Verify the Jobs page when no jobs are shown | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Jobs<br>3. Observe the screen<br>4. Check for message/blank | If no jobs exist, a clear 'No jobs available' type message should be displayed; blank screen without message is a potential UI/UX defect | Exploratory observation (formal execution pending): Jobs section did not show any jobs. Presence/absence of empty-state message to be recorded. | Not Executed |
| TC-179 | Verify 'No jobs' message | Verify the wording and visibility of the no-jobs message | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Jobs when empty<br>3. Read the message | Message should be clear and readable | Not Executed | Not Executed |
| TC-180 | Verify job listing | Verify job listing display (if jobs are available) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Jobs when jobs exist<br>3. Observe list | Jobs should be listed with titles | Not Executed | Not Executed |
| TC-181 | Verify job details | Verify job details (if jobs are available) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a job<br>3. Read the details | Details should be complete | Not Executed | Not Executed |
| TC-182 | Verify Jobs search | Verify search in Jobs if available | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Look for Jobs search<br>3. Search a keyword | Relevant jobs shown; if absent NOT APPLICABLE | Not Executed | Not Executed |
| TC-183 | Verify Jobs filter | Verify filters if available | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Look for filter<br>3. Apply a filter | Results filtered; if absent NOT APPLICABLE | Not Executed | Not Executed |
| TC-184 | Verify Apply button | Verify Apply action if available | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a job<br>3. Tap Apply | Apply should work or redirect; if absent NOT APPLICABLE | Not Executed | Not Executed |
| TC-185 | Verify Jobs with network failure | Verify Jobs behaviour without Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Open Jobs<br>4. Observe | Error/empty message should be shown; no crash | Not Executed | Not Executed |
| TC-186 | Verify Jobs refresh/back | Verify refresh and Back in Jobs | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Jobs<br>3. Refresh<br>4. Press Back | Refresh works and Back returns safely | Not Executed | Not Executed |

### Module 15: Games

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-187 | Verify games list | Verify that the games list is displayed | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open Games<br>3. Observe the list | Available games should be listed | Exploratory observation (formal execution pending): Multiple games are available. | Not Executed |
| TC-188 | Verify game loading | Verify that a game loads | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a game<br>3. Observe loading | Game should load without crash | Not Executed | Not Executed |
| TC-189 | Verify game start | Verify that a game starts | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Load a game<br>3. Tap Start/Play | Game should begin | Not Executed | Not Executed |
| TC-190 | Verify game controls | Verify that controls respond | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Play a game<br>3. Use all available controls | Controls should respond accurately | Not Executed | Not Executed |
| TC-191 | Verify level progression | Verify progression to the next level | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Complete level 1<br>3. Observe next level | Next level should unlock/start | Not Executed | Not Executed |
| TC-192 | Verify level completion | Verify the level completion screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Complete a level<br>3. Observe the screen | Completion feedback should be displayed | Not Executed | Not Executed |
| TC-193 | Verify score | Verify score updates | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Play a game<br>3. Observe score | Score should update correctly | Not Executed | Not Executed |
| TC-194 | Verify progress persistence after refresh | Verify that completed level persists after refresh | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Complete a level<br>3. Refresh the game<br>4. Observe the level | Completed progress should persist if persistence is intended; Requirement Confirmation Required | Exploratory observation (formal execution pending): Previously completed level remained after refresh. Intent of persistence not confirmed. | Not Executed |
| TC-195 | Verify exit confirmation | Verify the exit confirmation when pressing Back during a game | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start a game<br>3. Press Back<br>4. Observe the dialog | An exit confirmation with Cancel and Exit options should be displayed | Back navigation displayed an exit confirmation containing Cancel and Exit options. | PASS |
| TC-196 | Verify cancel exit | Verify that Cancel keeps the user in the game | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Press Back in a game<br>3. Tap Cancel<br>4. Observe | Game should continue | Not Executed | Not Executed |
| TC-197 | Verify confirm exit | Verify that Exit leaves the game | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Press Back in a game<br>3. Tap Exit<br>4. Observe | User should return to the previous screen | Not Executed | Not Executed |
| TC-198 | Verify progress after app restart | Verify game progress after closing the app | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Complete a level<br>3. Close and reopen the app<br>4. Open the game | Progress should persist if intended; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-199 | Verify game audio | Verify audio during gameplay and level completion | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Play with volume up<br>3. Complete a level<br>4. Listen | Audio/music should play correctly | Exploratory observation (formal execution pending): Audio/music can be heard during gameplay/after levels. | Not Executed |
| TC-200 | Verify mute | Verify muting behaviour | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Mute the device/in-game audio<br>3. Play<br>4. Observe | No sound should play when muted | Not Executed | Not Executed |
| TC-201 | Verify advertisement display | Verify that advertisements are displayed during games | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Play a game<br>3. Complete levels<br>4. Observe ads | Ads display correctly and do not crash the app | Exploratory observation (formal execution pending): Ads appear while playing and can appear after levels. Ads are not treated as defects by themselves. | Not Executed |
| TC-202 | Verify advertisement close | Verify closing an advertisement | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. When an ad appears<br>3. Close it<br>4. Observe | Ad should close and return to the game | Not Executed | Not Executed |
| TC-203 | Verify repeated advertisements | Verify the frequency of ads | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Close an ad<br>3. Observe if another ad appears<br>4. Count ads in 10 minutes | Ad frequency should be acceptable and not disrupt gameplay; acceptable frequency: Requirement Confirmation Required | Exploratory observation (formal execution pending): After closing/canceling an ad, another ad may appear. Impact on usability to be assessed. | Not Executed |
| TC-204 | Verify game lag | Verify game performance during gameplay | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Play for 10 minutes<br>3. Observe lag/stutter<br>4. Record when it occurs | Game should run smoothly; performance expectation: Requirement Confirmation Required | Exploratory observation (formal execution pending): Game can become laggy. Needs investigation as a potential performance issue. | Not Executed |
| TC-205 | Verify game crash | Verify stability during long play | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Play for 20 minutes<br>3. Switch levels<br>4. Observe crash | Game should not crash | Not Executed | Not Executed |
| TC-206 | Verify game restart | Verify restarting a game | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Play a game<br>3. Restart<br>4. Observe | Game should restart correctly | Not Executed | Not Executed |
| TC-207 | Verify game under network conditions | Verify games on slow/no network | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Open a game<br>4. Play | Game behaviour should be recorded; Requirement Confirmation Required | Not Executed | Not Executed |

### Module 16: Network Testing

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-208 | Verify behaviour on 4G | Verify application on 4G | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable 4G only<br>3. Use search, map, stops | App should function normally | Not Executed | Not Executed |
| TC-209 | Verify behaviour on Wi-Fi | Verify application on Wi-Fi | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable Wi-Fi only<br>3. Use main features | App should function normally | Not Executed | Not Executed |
| TC-210 | Verify behaviour with no Internet | Verify behaviour when no Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF data and Wi-Fi<br>3. Open the app and features | Clear messages or cached data without crash | Not Executed | Not Executed |
| TC-211 | Verify network switching | Verify switching 4G to Wi-Fi | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Use the map on 4G<br>3. Switch to Wi-Fi<br>4. Observe | App should continue without crash | Not Executed | Not Executed |
| TC-212 | Verify slow network | Verify slow network (e.g. throttled) | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Use a slow connection<br>3. Open map and search | App should show loading and remain stable | Not Executed | Not Executed |
| TC-213 | Verify network interruption | Verify interruption mid action | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start a search<br>3. Turn OFF Internet<br>4. Observe | Clear error/message; no crash | Not Executed | Not Executed |
| TC-214 | Verify network recovery | Verify recovery after Internet returns | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Use the app<br>4. Turn ON Internet<br>5. Observe | App should recover and refresh data | Not Executed | Not Executed |
| TC-215 | Verify app launch without Internet | Verify cold launch without Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Force stop<br>3. Turn OFF Internet<br>4. Launch | Behaviour recorded; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-216 | Verify search without Internet | Verify search without Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Search bus/stop | Message or cached results; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-217 | Verify map without Internet | Verify map without Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Turn OFF Internet<br>4. Observe | Behaviour recorded; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-218 | Verify bus tracking without Internet | Verify tracking when Internet is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open tracking<br>3. Turn OFF Internet<br>4. Observe | Updates stop or message shown; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-219 | Verify bus stop without Internet | Verify stops without Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Open a stop | Message or cached content; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-220 | Verify ticket without Internet | Verify tickets without Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Open the tickets feature | Behaviour recorded; NOT APPLICABLE if ticket absent | Not Executed | Not Executed |
| TC-221 | Verify game without Internet | Verify games without Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Open a game | Behaviour recorded; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-222 | Verify Jobs without Internet | Verify Jobs without Internet | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Turn OFF Internet<br>3. Open Jobs | Error/empty message; no crash | Not Executed | Not Executed |
| TC-223 | Verify cached vs static vs live data | Determine the nature of bus information visible after Internet is OFF | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Load buses on the map<br>3. Turn OFF Internet<br>4. Observe icons for 5 minutes<br>5. Turn ON Internet<br>6. Compare position changes | Data should be identified as cached, static, previously loaded or still updating; Requirement Confirmation Required | Exploratory observation (formal execution pending): Bus information can remain visible after network is turned OFF. Not yet classified as cached/static/live. | Not Executed |

### Module 17: UI / UX Testing

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-224 | Verify alignment | Verify alignment of elements | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open all main screens<br>3. Observe alignment | Elements should be aligned | Not Executed | Not Executed |
| TC-225 | Verify buttons | Verify button appearance and state | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open screens<br>3. Observe buttons | Buttons should be visible and consistent | Not Executed | Not Executed |
| TC-226 | Verify fonts | Verify font consistency and size | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open screens<br>3. Observe fonts | Fonts should be consistent and readable | Not Executed | Not Executed |
| TC-227 | Verify text visibility | Verify contrast and visibility | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open screens in daylight/dark<br>3. Read | Text should be clearly readable | Not Executed | Not Executed |
| TC-228 | Verify icons | Verify icon clarity | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Observe icons | Icons should be clear and meaningful | Not Executed | Not Executed |
| TC-229 | Verify spacing | Verify spacing and padding | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Observe screens | Spacing should be consistent | Not Executed | Not Executed |
| TC-230 | Verify screen responsiveness | Verify layout fits the screen | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open screens<br>3. Scroll<br>4. Observe | No cut-off/overlap | Not Executed | Not Executed |
| TC-231 | Verify map layout usable space | Verify that the map provides sufficient usable space with route/bus stop panels visible | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map for a bus (e.g. '202 to Vasai Phata')<br>3. Observe the proportion occupied by the info panel<br>4. Try to pan/zoom<br>5. Collapse/expand the panel if possible<br>6. Assess visibility of the route | Map area should be sufficient for use; panel size should not obstruct map interaction; usability impact must be confirmed before reporting | Exploratory observation (formal execution pending): Route/bus-stop information such as '202 to Vasai Phata' occupies a large portion of the screen. Usability impact not yet confirmed. | Not Executed |
| TC-232 | Verify bottom panels | Verify bottom panel behaviour | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open the map<br>3. Drag/tap the bottom panel | Panel should open/close smoothly | Not Executed | Not Executed |
| TC-233 | Verify bus information display | Verify bus info layout | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Tap a bus<br>3. Observe the info | Information should be readable | Not Executed | Not Executed |
| TC-234 | Verify bus stop information display | Verify stop info layout | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open a stop<br>3. Observe info | Information should be readable | Not Executed | Not Executed |
| TC-235 | Verify empty screens | Verify empty-state messages | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open screens with no data<br>3. Observe | Meaningful empty-state message | Not Executed | Not Executed |
| TC-236 | Verify blank screens | Verify no unexplained blank screens occur | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Navigate through all screens<br>3. Record any blank screen | No unexplained blank screens | Not Executed | Not Executed |
| TC-237 | Verify error messages | Verify clarity of error messages | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Trigger errors<br>3. Read messages | Messages should be clear and actionable | Not Executed | Not Executed |
| TC-238 | Verify loading indicators | Verify loading indicators | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open data screens<br>3. Observe | Loading indicator should appear during loading | Not Executed | Not Executed |
| TC-239 | Verify touch targets | Verify tap target size | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Tap small buttons/icons | Targets should be easily tappable | Not Executed | Not Executed |
| TC-240 | Verify navigation UI | Verify navigation controls | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Use navigation elements | Controls should be intuitive and functional | Not Executed | Not Executed |
| TC-241 | Verify consistency | Verify UI consistency across modules | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Compare styles of screens | Consistent look and feel | Not Executed | Not Executed |

### Module 18: Compatibility Testing

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-242 | Verify on different Android versions | Verify on multiple Android versions | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Install on devices with different Android versions<br>3. Run the smoke tests | App should work on supported versions; supported versions: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-243 | Verify on different screen sizes | Verify on small and large screens | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Install on different screen sizes<br>3. Observe layouts | Layout should adapt | Not Executed | Not Executed |
| TC-244 | Verify on different resolutions | Verify different resolutions | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Run on HD/FHD+ devices<br>3. Observe | UI should be sharp and not distorted | Not Executed | Not Executed |
| TC-245 | Verify portrait mode | Verify portrait | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Use the app in portrait | Layout should be correct | Not Executed | Not Executed |
| TC-246 | Verify landscape mode | Verify landscape if supported | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Rotate the device<br>3. Observe | Layout adapts or orientation locked; Requirement Confirmation Required | Not Executed | Not Executed |
| TC-247 | Verify different network conditions | Verify on varied networks | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Test on 4G, Wi-Fi, slow<br>3. Observe | App should work as per network | Not Executed | Not Executed |
| TC-248 | Verify low battery | Verify on low battery/battery saver | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Enable battery saver<br>3. Use tracking | App should work | Not Executed | Not Executed |
| TC-249 | Verify low storage | Verify on low storage | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Reduce free space<br>3. Launch | App should run without crash | Not Executed | Not Executed |
| TC-250 | Verify background/foreground | Verify background/foreground handling | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Switch apps repeatedly | App should resume | Not Executed | Not Executed |
| TC-251 | Verify phone rotation | Verify rotation during use | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Rotate on map/game<br>3. Observe | State should be retained | Not Executed | Not Executed |

### Module 19: Performance Observation (Manual)

| TEST CASE ID | TEST SCENARIO | TEST CASE | TEST STEPS | EXPECTED RESULT | ACTUAL RESULT | STATUS (PASS/FAIL) |
|---|---|---|---|---|---|---|
| TC-252 | Verify app launch time | Measure app launch time on 4G | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Close the app<br>3. Start the stopwatch and tap the icon<br>4. Stop when usable<br>5. Repeat 3 times | Launch time should be within the acceptable benchmark; benchmark: Requirement Confirmation Required | Application took approximately 10 seconds to become usable on 4G. (Observed; no benchmark defined, so not treated as a failure.) | Not Executed |
| TC-253 | Verify screen loading time | Measure screen load time | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Open each main screen<br>3. Time loading | Screens should load reasonably; benchmark: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-254 | Verify map loading time | Measure map load time | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Select a bus<br>3. Time until the map is ready | Map should load in acceptable time; benchmark: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-255 | Verify search response time | Measure search response | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Search a bus<br>3. Time the result | Results should appear promptly; benchmark: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-256 | Verify bus tracking refresh time | Measure tracking refresh | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Observe icon refresh<br>3. Record intervals | Refresh should be regular; interval: Requirement Confirmation Required | Not Executed | Not Executed |
| TC-257 | Verify game loading time | Measure game load | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Start games<br>3. Time loading | Game should load in reasonable time | Not Executed | Not Executed |
| TC-258 | Verify UI responsiveness | Verify responsiveness | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Perform quick taps/scrolls | UI should respond immediately | Not Executed | Not Executed |
| TC-259 | Verify freezing | Verify no freezing in extended use | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Use app 20 minutes<br>3. Observe freezes | No freezing | Not Executed | Not Executed |
| TC-260 | Verify crash in extended session | Verify stability | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Use all modules for 30 minutes<br>3. Note crashes | No crash | Not Executed | Not Executed |
| TC-261 | Verify battery/data usage | Observe battery and data usage | 1. Launch the Aapli Bus VVMT application (4G network, GPS ON unless stated otherwise)<br>2. Use app 15 minutes<br>3. Check usage | Usage should be reasonable; threshold: Requirement Confirmation Required | Not Executed | Not Executed |

## 6. Exploratory Testing Observations

| OBSERVATION ID | MODULE | OBSERVATION | ACTION TAKEN | RESULT | DEFECT? |
|---|---|---|---|---|---|
| OBS-001 | Performance | App launch took approximately 10 seconds on 4G | Measured launch time | ~10 seconds to usable state | Performance Observation (APLI-008) |
| OBS-002 | Announcements | Announcement opens using the eye/view button | Tapped eye/view button | Announcement opened | No |
| OBS-003 | Bus Search | Buses 101-106 were available | Searched buses | Buses found | No |
| OBS-004 | Bus Search | Bus 107 not found | Searched 107 | Not found | Requirement Confirmation Required |
| OBS-005 | Bus Details & Map | Bus 102 opens map | Searched and selected Bus 102 | Map opened | No |
| OBS-006 | Bus Details & Map | Bus icons appear on map | Viewed the route | Icons visible | No |
| OBS-007 | Bus Details & Map | Tapping bus icon displays bus number | Tapped a bus icon | Number/details displayed | No |
| OBS-008 | Live Tracking | Green/yellow bus indicators observed (a yellow bus appeared moving) | Observed map | Colours seen; meaning unconfirmed | Requirement Confirmation Required |
| OBS-009 | Bus Stops | Bus stops can be searched | Searched stops | Stops searchable | No |
| OBS-010 | Location Accuracy | Location name displayed as 'Polhar Highway Rasta' | Compared with expectation | Name possibly inaccurate; unverified | Requirement Confirmation Required (APLI-002) |
| OBS-011 | GPS / Location | Buses remain visible when device location is OFF | Turned OFF location | Buses still visible | Requirement Confirmation Required |
| OBS-012 | Network | Bus information can remain visible when network is OFF | Turned OFF network | Information still visible | Requirement Confirmation Required |
| OBS-013 | Installation & Launch | Internet appears necessary during initial app opening | Opened app without Internet | Internet appears needed at initial open | Requirement Confirmation Required |
| OBS-014 | Localization | UI language changes | Changed language | UI text changed | No |
| OBS-015 | Localization | Announcement content does not appear to change with language | Changed language and viewed announcements | Announcement content unchanged | Potential Defect / Requirement Confirmation Required (APLI-003) |
| OBS-016 | Jobs | Jobs section had no visible jobs | Opened Jobs | No jobs shown | Requirement Confirmation Required |
| OBS-017 | Games | Multiple games are available | Opened Games | Several games listed | No |
| OBS-018 | Games | Multiple/repeated ads can appear | Played games | Ads appeared repeatedly | Requirement Confirmation Required (APLI-007) |
| OBS-019 | Games | Game can become laggy | Played games | Lag noticed | Potential Defect (APLI-006) |
| OBS-020 | Games | Game progress remains after refresh | Refreshed game | Progress remained | Requirement Confirmation Required |
| OBS-021 | Games | Back button displays game exit confirmation | Pressed Back in game | Exit confirmation (Cancel/Exit) shown | No |
| OBS-022 | Bus Stops | Nalasopara Phata opens blank | Opened the stop | Blank screen | Potential Defect (APLI-001) |
| OBS-023 | Bus Stops | 'See All' shows nearby bus stops | Tapped See All | Nearby stops shown | Requirement Confirmation Required (APLI-005) |
| OBS-024 | UI / UX | Map info panel occupies large screen portion | Viewed map | Large portion occupied | Requirement Confirmation Required (APLI-004) |

## 7. Defect Report

> No defect is a *Confirmed Defect* yet. Severity/Priority are **proposed** values for the logged candidates; change after reproduction and requirement confirmation.

| BUG ID | TEST CASE ID | MODULE | DEFECT TITLE | DESCRIPTION | STEPS TO REPRODUCE | EXPECTED RESULT | ACTUAL RESULT | SEVERITY | PRIORITY | ENVIRONMENT | STATUS |
|---|---|---|---|---|---|---|---|---|---|---|---|
| APLI-001 | TC-117 | Bus Stops | Nalasopara Phata bus stop opens to a blank screen | Selecting 'Nalasopara Phata' opens a screen that appears blank without details or message. | 1. Launch the app<br>2. Open bus stop search<br>3. Select 'Nalasopara Phata'<br>4. Observe the screen | Relevant bus stop details should be displayed | Blank screen is displayed (observed during exploratory testing) | Major | High | [DEVICE] / [ANDROID VERSION] / 4G | Potential Defect – to be confirmed during formal execution |
| APLI-002 | TC-111 | Location Accuracy | Possible incorrect location/area name displayed ('Polhar Highway Rasta') | App displayed 'Polhar Highway Rasta'; tester expected a name such as 'Pelhar / Vasai Phata'. Official name not verified. | 1. Enable location<br>2. Open the screen showing the area name<br>3. Note displayed name<br>4. Compare with official source | Displayed area name should match the officially verified name | Displayed 'Polhar Highway Rasta' | Minor | Medium | [DEVICE] / [ANDROID VERSION] / 4G | Requirement Confirmation Required – to be confirmed during formal execution |
| APLI-003 | TC-035 | Localization | Announcement content does not change with selected language | UI/paragraph content changes but announcements appear unchanged. Whether announcements should be localized is unconfirmed. | 1. Open Announcements and note content<br>2. Change language<br>3. Reopen announcements<br>4. Compare | Announcement content should change if localization of announcements is expected | Announcement content did not appear to change | Minor | Medium | [DEVICE] / [ANDROID VERSION] / 4G | Potential Defect – to be confirmed during formal execution |
| APLI-004 | TC-231 | UI / UX | Map UI may provide insufficient map area | Route/bus-stop info (e.g. '202 to Vasai Phata') occupies a large portion of the map screen. | 1. Search a bus (e.g. 202)<br>2. Open the map<br>3. Observe space used by the info panel<br>4. Try pan/zoom | Map should provide sufficient usable area | Info panel occupies a large portion of the screen | Minor | Medium | [DEVICE] / [ANDROID VERSION] / 4G | Requirement Confirmation Required – to be confirmed during formal execution |
| APLI-005 | TC-120 | Bus Stops | 'See All' may display nearby bus stops rather than all bus stops | 'See All' shows nearby stops. Intended meaning unconfirmed. | 1. Open nearby bus stops<br>2. Tap See All<br>3. Observe list | 'See All' should match the defined meaning (all stops or all nearby stops) | Nearby bus stops are shown | Trivial | Low | [DEVICE] / [ANDROID VERSION] / 4G | Requirement Confirmation Required – to be confirmed during formal execution |
| APLI-006 | TC-204 | Games | Game becomes laggy during gameplay | Lag observed during gameplay; conditions to be investigated. | 1. Open Games<br>2. Start a game<br>3. Play for several minutes<br>4. Observe lag | Game should run smoothly | Game became laggy | Minor | Medium | [DEVICE] / [ANDROID VERSION] / 4G | Potential Defect – to be confirmed during formal execution |
| APLI-007 | TC-203 | Games | Repeated advertisements may negatively affect game usability | Another ad can appear after closing one, and ads appear after levels. Ads are not defects by themselves. | 1. Start a game<br>2. Complete levels<br>3. Close an ad<br>4. Observe if another appears | Ad frequency should not disrupt gameplay | Repeated ads observed | Minor | Low | [DEVICE] / [ANDROID VERSION] / 4G | Requirement Confirmation Required – to be confirmed during formal execution |
| APLI-008 | TC-252 | Performance | Application takes approximately 10 seconds to launch on 4G | Launch took ~10 seconds on 4G; no benchmark defined. | 1. Close the app<br>2. Tap icon and start stopwatch<br>3. Stop when usable | Launch within acceptable benchmark (RC) | ~10 seconds to become usable | Minor | Medium | [DEVICE] / [ANDROID VERSION] / 4G | Performance Observation – to be confirmed during formal execution |

## 8. Requirement Traceability Matrix (RTM)

> Requirement text = derived test objectives. 'Needs clarification' = expected behaviour not known.

| REQUIREMENT ID | MODULE | REQUIREMENT | TEST CASE ID | TEST CASE DESCRIPTION | STATUS | DEFECT ID |
|---|---|---|---|---|---|---|
| REQ-001 | Installation & Launch | Application installs and launches successfully to a usable home screen | TC-001 to TC-006 | 6 case(s): application installation; application identity; first launch; ... | Not Executed | - |
| REQ-002 | Installation & Launch | Application remains stable (no crash/freeze) across restart and lifecycle events | TC-009 to TC-016 | 8 case(s): app restart; launch after force stop; background/foreground behaviour; ... | Not Executed | - |
| REQ-003 | Installation & Launch | Application launch behaviour under different Internet/GPS states | TC-007 to TC-008 | 2 case(s): launch without Internet; launch with GPS disabled | Not Executed | - |
| REQ-004 | Navigation | User can navigate between screens; back/forward/exit behave consistently | TC-017 to TC-026 | 10 case(s): home screen; navigation menu; Back button; ... | Not Executed | - |
| REQ-005 | Localization | UI text changes according to selected language | TC-027 to TC-034, TC-038 to TC-039 | 10 case(s): language change; UI translation; buttons translation; ... | Not Executed | - |
| REQ-006 | Localization | Language persistence and localization scope (including announcements) | TC-035 to TC-037 | 3 case(s): announcement localization; language persistence; language after device restart | Not Executed | APLI-003 |
| REQ-007 | Announcements | Announcements can be listed, opened (eye/view button) and closed | TC-040 to TC-050 | 11 case(s): announcement list; announcement loading; eye/view button opens announcement; ... | Partially Executed (1/11 PASS) | - |
| REQ-008 | Bus Search | User can search a bus by number and see matching results | TC-051, TC-053, TC-060, TC-062 | 4 case(s): search by valid bus number; search for bus 107; multiple results; ... | Partially Executed (1/4 PASS) | - |
| REQ-009 | Bus Search | Search handles invalid, empty, partial and special input gracefully | TC-052, TC-054 to TC-059, TC-063 to TC-065 | 10 case(s): search by invalid bus number; empty search; partial bus number; ... | Not Executed | - |
| REQ-010 | Bus Search | User can search bus stops and select a result | TC-061, TC-115 to TC-116 | 3 case(s): bus stop search; bus stop search; bus stop selection | Partially Executed (1/3 PASS) | - |
| REQ-011 | Bus Details & Map | Selecting a bus opens a map with route and bus information | TC-066 to TC-072, TC-080 | 8 case(s): selecting a bus opens map; map loading; bus icon display; ... | Partially Executed (3/8 PASS) | - |
| REQ-012 | Bus Details & Map | Map supports zoom/pan/refresh and shows bus stops and route | TC-073 to TC-079 | 7 case(s): map zoom; map movement; map refresh; ... | Not Executed | - |
| REQ-013 | Live Tracking | Bus location/movement/status is displayed and updated on the map | TC-081 to TC-084, TC-086 to TC-094 | 13 case(s): bus location display; bus movement; bus status; ... | Not Executed | - |
| REQ-014 | Live Tracking | Bus colour indicators correspond to the status defined by the application | TC-085 | 1 case(s): bus colour indicators | Not Executed | - |
| REQ-015 | GPS / Location | Location permission flow (allow/deny/revoke) works correctly | TC-095 to TC-096, TC-099 to TC-101 | 5 case(s): location permission allowed; location permission denied; first permission request; ... | Not Executed | - |
| REQ-016 | GPS / Location | Application behaviour when device location is ON/OFF | TC-097 to TC-098, TC-107 to TC-110 | 6 case(s): location disabled; location enabled; buses visible with location OFF - previously loaded data; ... | Not Executed | - |
| REQ-017 | GPS / Location | Nearby buses/bus stops are shown based on user location | TC-102 to TC-106, TC-119 | 6 case(s): current location; nearby bus stops; nearby buses; ... | Not Executed | - |
| REQ-018 | Location Accuracy | Displayed location/area name is accurate | TC-111 to TC-114 | 4 case(s): accuracy of displayed location/area name; location name against official source; location name consistency across screens; ... | Not Executed | APLI-002 |
| REQ-019 | Bus Stops | Bus stop opens and shows relevant stop details and routes | TC-117 to TC-118, TC-122 to TC-130 | 11 case(s): Nalasopara Phata bus stop opens correctly; bus stop details; bus stop map; ... | Not Executed | APLI-001 |
| REQ-020 | Bus Stops | 'See All' behaviour (all stops vs nearby stops) | TC-120 to TC-121 | 2 case(s): 'See All' meaning; 'See All' list completeness | Not Executed | APLI-005 |
| REQ-021 | Journey Planning | User can plan a journey between source and destination (if feature exists) | TC-131 to TC-147 | 17 case(s): journey planning availability; source selection; destination selection; ... | Not Executed | - |
| REQ-022 | Ticket Booking | User can select and generate a ticket (if feature exists) | TC-148 to TC-160 | 13 case(s): ticket feature availability; ticket selection; source selection; ... | Not Executed | - |
| REQ-023 | Ticket Booking | Ticket history/details/digital ticket display (if feature exists) | TC-161 to TC-164 | 4 case(s): ticket history; ticket details; QR ticket; ... | Not Executed | - |
| REQ-024 | Payment | Payment success/failure/cancel handling (if feature exists) | TC-165 to TC-176 | 12 case(s): payment availability; successful payment; failed payment; ... | Not Executed | - |
| REQ-025 | Jobs | Jobs section shows listings or an appropriate empty state | TC-177 to TC-186 | 10 case(s): Jobs page loading; Jobs empty state; 'No jobs' message; ... | Not Executed | - |
| REQ-026 | Games | Games can be listed, launched and played | TC-187 to TC-193, TC-204 to TC-207 | 11 case(s): games list; game loading; game start; ... | Not Executed | APLI-006 |
| REQ-027 | Games | Game progress persistence and exit confirmation | TC-194 to TC-198 | 5 case(s): progress persistence after refresh; exit confirmation; cancel exit; ... | Partially Executed (1/5 PASS) | - |
| REQ-028 | Games | Advertisement behaviour during gameplay | TC-201 to TC-203 | 3 case(s): advertisement display; advertisement close; repeated advertisements | Not Executed | APLI-007 |
| REQ-029 | Games | Game audio and mute behaviour | TC-199 to TC-200 | 2 case(s): game audio; mute | Not Executed | - |
| REQ-030 | Network | Application behaviour across 4G / Wi-Fi / no Internet / switching | TC-208 to TC-214 | 7 case(s): behaviour on 4G; behaviour on Wi-Fi; behaviour with no Internet; ... | Not Executed | - |
| REQ-031 | Network | Offline behaviour: cached vs static vs live data | TC-215 to TC-223 | 9 case(s): app launch without Internet; search without Internet; map without Internet; ... | Not Executed | - |
| REQ-032 | UI / UX | UI elements are aligned, readable and consistent | TC-224 to TC-230, TC-232 to TC-234, TC-239 to TC-241 | 13 case(s): alignment; buttons; fonts; ... | Not Executed | - |
| REQ-033 | UI / UX | Loading, empty, blank and error states give proper feedback | TC-235 to TC-238 | 4 case(s): empty screens; blank screens; error messages; ... | Not Executed | - |
| REQ-034 | UI / UX | Map screen provides sufficient usable map area | TC-231 | 1 case(s): map layout usable space | Not Executed | APLI-004 |
| REQ-035 | Compatibility | Application works across Android versions, screen sizes and device conditions | TC-242 to TC-251 | 10 case(s): on different Android versions; on different screen sizes; on different resolutions; ... | Not Executed | - |
| REQ-036 | Performance | Manual observation of launch, load, response and stability | TC-252 to TC-261 | 10 case(s): app launch time; screen loading time; map loading time; ... | Not Executed | APLI-008 |

**Coverage analysis**

| Category | Requirements |
|---|---|
| Test cases designed for | All 36 derived requirements (test design coverage 100%; execution coverage is separate) |
| Executed at least partly | REQ-007, REQ-008, REQ-010, REQ-011, REQ-027 |
| Partially/conditionally covered (feature existence unconfirmed) | REQ-021, REQ-022, REQ-023, REQ-024 |
| Needing clarification (expected behaviour unknown) | REQ-003, REQ-006, REQ-013, REQ-014, REQ-016, REQ-017, REQ-018, REQ-020, REQ-021, REQ-022, REQ-023, REQ-024, REQ-025, REQ-028, REQ-031, REQ-034, REQ-036 |
| Linked to defect candidates | REQ-006, REQ-018, REQ-019, REQ-020, REQ-026, REQ-028, REQ-034, REQ-036 |

## 9. Test Execution Summary

| Metric | Value | Percentage |
|---|---|---|
| Total Test Cases | 261 | 100% |
| Executed | 7 | 2.7% of total |
| Passed | 7 | 100.0% of executed |
| Failed | 0 | 0.0% of executed |
| Blocked | 0 | 0.0% of executed |
| Not Executed | 254 | 97.3% of total |
| Not Applicable | 0 | 0.0% of total |

*20 further cases carry an exploratory observation in Actual Result but remain 'Not Executed' because the verdict needs requirement confirmation or formal reproduction.*

## 10. Defect Summary

**Confirmed defects only**

| Severity | Number of Defects |
|---|---|
| Critical | 0 |
| Major | 0 |
| Medium | 0 (not on the project severity scale; kept for the requested format) |
| Minor | 0 |
| Trivial | 0 |

**Potential defects / findings (not counted above)**

| Bug ID | Title | Classification | Proposed Severity | Proposed Priority |
|---|---|---|---|---|
| APLI-001 | Nalasopara Phata bus stop opens to a blank screen | Potential Defect | Major | High |
| APLI-002 | Possible incorrect location/area name displayed ('Polhar Highway Rasta') | Requirement Confirmation Required | Minor | Medium |
| APLI-003 | Announcement content does not change with selected language | Potential Defect | Minor | Medium |
| APLI-004 | Map UI may provide insufficient map area | Requirement Confirmation Required | Minor | Medium |
| APLI-005 | 'See All' may display nearby bus stops rather than all bus stops | Requirement Confirmation Required | Trivial | Low |
| APLI-006 | Game becomes laggy during gameplay | Potential Defect | Minor | Medium |
| APLI-007 | Repeated advertisements may negatively affect game usability | Requirement Confirmation Required | Minor | Low |
| APLI-008 | Application takes approximately 10 seconds to launch on 4G | Performance Observation | Minor | Medium |

## 11. Testing Types Coverage

| TESTING TYPE | COVERED? | EXAMPLES |
|---|---|---|
| Functional Testing | Yes | Bus search, bus stops |
| Smoke Testing | Yes | App launch, navigation |
| Sanity Testing | Yes | Changed features |
| Regression Testing | Planned | Previously tested functionality |
| Exploratory Testing | Yes | Unscripted exploration |
| Negative Testing | Yes | Invalid search, network failure |
| UI Testing | Yes | Map/UI |
| Usability Testing | Yes | Navigation |
| Localization Testing | Yes | Language |
| Compatibility Testing | Planned | Android/device |
| Performance Observation | Yes | App launch/game lag |
| Network Testing | Yes | Offline/online |
| GPS Testing | Yes | Location |

*'Yes' = test cases designed; execution status is in Section 9.*

## 12. Recommendations

| # | Type | Observed Issue | Recommendation / Requirement Confirmation |
|---|---|---|---|
| 1 | Observed Issue | Nalasopara Phata opens blank (APLI-001) | Recommendation: handle blank screens with details or a clear message; reproduce 3 times first |
| 2 | Requirement Confirmation | 'See All' shows nearby stops (APLI-005) | Confirm intended meaning; consider the label 'See All Nearby Stops' if intended |
| 3 | Requirement Confirmation | Area name 'Polhar Highway Rasta' (APLI-002) | Verify official name against Google Maps/VVMT before reporting |
| 4 | Requirement Confirmation | Announcements not localized (APLI-003) | Confirm whether announcements should be localized |
| 5 | Requirement Confirmation | Map info panel size (APLI-004) | Review map space; consider a collapsible panel |
| 6 | Requirement Confirmation | Green/yellow bus indicators | Clarify colour meaning; consider an in-app legend |
| 7 | Observed Issue | Game lag (APLI-006) | Investigate on more devices/networks and note when lag occurs |
| 8 | Requirement Confirmation | Repeated ads (APLI-007) | Review ad frequency after levels; confirm intended ad policy |
| 9 | Requirement Confirmation | Bus info visible when network/location OFF | Clarify cached vs live; consider offline/stale-data messaging |
| 10 | Requirement Confirmation | Jobs section empty | Check for a 'No jobs available' message; add one if missing |
| 11 | Performance Observation | ~10 s launch on 4G (APLI-008) | Compare with a benchmark and repeat measurements before concluding |

## 13. Test Summary Report

**1. Project Overview** – Manual testing of the Aapli Bus VVMT Android application as a personal QA portfolio (lab assignment) project by Sujeet Sahani.

**2. Testing Objective** – Verify core functionality, usability, localization, network/GPS behaviour and observed performance, and document findings professionally.

**3. Scope** – All 19 modules in Section 4 on an Android device over 4G (Wi-Fi/no-Internet for network cases).

**4. Out of Scope** – Load/stress testing, security testing, automation, backend/API testing, iOS, real financial transactions, features not present in the app.

**5. Test Environment** – See Section 2 (device/OS/app version to be filled in).

**6. Testing Types** – See Section 11.

**7. Modules Tested** – Application Installation and Launch; Application Navigation; Language / Localization; Announcements; Bus Search; Bus Details and Map; Live Bus Tracking; GPS / Location; Location / Area Name Accuracy; Bus Stops; Journey Planning; Ticket Booking; Payment; Jobs; Games; Network Testing; UI / UX Testing; Compatibility Testing; Performance Observation (Manual). (Ticket Booking, Payment and Journey Planning apply only if the features exist.)

**8. Test Case Statistics** – Total 261; Executed 7; Passed 7; Failed 0; Blocked 0; Not Executed 254; Not Applicable 0.

**9. Defect Statistics** – Confirmed: 0. Potential/under confirmation: 8 (see Sections 7 and 10).

**10. Major Findings** – Exploratory observations only: a blank bus-stop screen, possible location-name inaccuracy, announcements not changing with language, large map info panel, 'See All' semantics, game lag, repeated ads and ~10 s launch. None is a confirmed defect yet.

**11. Risks** – Expected behaviour is undocumented for many areas; the app is live and data changes; limited device/OS coverage; unverified features (tickets/payments/journey planning).

**12. Limitations** – Formal execution is incomplete, only one device/network profile is planned, no official requirement document is available, performance is a manual observation.

**13. Recommendations** – See Section 12.

**14. Conclusion** – The test repository (261 cases) and traceability are in place. Testing is **not complete**: 2.7% of cases are executed. Findings must be reproduced and confirmed before being reported as defects.

## 14. Final Project Metrics

| METRIC | VALUE |
|---|---|
| Total Test Cases | 261 |
| Executed | 7 |
| Passed | 7 |
| Failed | 0 |
| Blocked | 0 |
| Not Executed | 254 |
| Not Applicable | 0 |
| Confirmed Defects | 0 |
| Potential Defects (logged candidates) | 8 |
| Critical Defects | 0 |
| Major Defects | 0 confirmed (1 proposed: APLI-001) |
| Medium Defects | 0 |
| Minor Defects | 0 |

*Update these values after each execution cycle.*

## 15. Resume-Ready Project Description

**Use the version below now; replace numbers after you execute more tests.**

```
Aapli Bus VVMT – Mobile Application Testing (Personal QA Project)

• Performed manual and exploratory testing of the Aapli Bus VVMT Android application covering app launch, navigation, localization, announcements, bus search, map and live bus tracking, GPS/location, bus stops, games, jobs and network behaviour.
• Designed 261 test cases (with RTM) covering functional, smoke, negative, UI/UX, localization, network, GPS and performance-observation scenarios; executed 7 to date.
• Logged 8 defect candidates with severity, priority, reproduction steps and expected/actual results, pending reproduction and requirement confirmation.
• Tested bus search, route/map functionality, bus tracking, bus stops and location-based functionality.
• Performed network (4G / offline) and GPS (ON/OFF) scenario testing.
• Maintained test cases, execution status, RTM and defect documentation using MS Excel.
• Applied SDLC, STLC and defect life-cycle practices.
```

*Do not change numbers to '200+ test cases' or 'X defects' unless they are real (the case count is already above 200; the executed/defect counts are not).* 

## 16. Interview Questions and Answers

**1. Tell me about your Aapli Bus VVMT testing project.**

It is a personal manual testing project on the Aapli Bus VVMT bus app. I designed test cases, did exploratory testing, recorded observations, built an RTM and logged defect candidates, all documented in Excel.

**2. Why did you select this application?**

It is a real public-transport app I can use. It has searchable data, maps, GPS, languages, games and network-dependent behaviour, so I could practise many types of testing.

**3. What modules did you test?**

Launch, navigation, localization, announcements, bus search, bus details/map, live tracking, GPS, location accuracy, bus stops, journey planning, tickets/payment (if available), jobs, games, network, UI/UX, compatibility and performance observation.

**4. How did you create test cases?**

I broke each module into scenarios, then wrote positive, negative and boundary cases with numbered steps and expected results. Where expected behaviour was unknown, I wrote 'Requirement Confirmation Required'.

**5. How many test cases did you create?**

261 test cases across 19 modules, without padding duplicates.

**6. How many did you execute?**

So far 7 are formally executed. Many more are observed in exploratory testing, and the rest are planned. I only mark Pass/Fail with real evidence.

**7. How many defects did you find?**

No confirmed defects yet. I logged 8 defect candidates that I am confirming through reproduction and requirement checks.

**8. Give me an example of a defect.**

APLI-001: selecting the 'Nalasopara Phata' bus stop opens a blank screen instead of stop details.

**9. What was the severity and priority?**

I proposed Major severity and High priority, because users cannot see stop information. It stays a potential defect until reproduced.

**10. How did you test GPS?**

I checked permission allowed/denied/revoked, location ON/OFF, current location and nearby stops. With location OFF, buses still appeared, so I test whether it is previously loaded data, live data, or independent of GPS, instead of calling it a bug.

**11. How did you test network conditions?**

I tested 4G, Wi-Fi, no Internet, switching, slow network and recovery. I observed that bus info stays visible when the network is off, and I check if it is cached, static or live.

**12. How did you perform negative testing?**

Invalid and empty search, partial numbers, letters, special characters, spaces, long input, no network, GPS off and permission denied.

**13. How did you perform regression testing?**

I planned a regression suite from smoke and high-priority cases to rerun after a fix or app update. I will only report it as done after I execute it.

**14. How did you test localization?**

I changed the language and checked UI text, buttons, menus, errors, search text and persistence after restart. UI text changed but announcements appeared unchanged, so I logged it as a potential defect needing confirmation.

**15. What was the most important defect you found?**

The blank screen on Nalasopara Phata, since it blocks a core function, once confirmed by reproduction.

**16. What challenges did you face?**

No official requirement document, so I could not tell expected behaviour for things like green/yellow bus colours, cached data or 'See All'. I handled this by marking them for requirement confirmation.

**17. How did you decide whether something was a bug?**

I compare actual vs expected behaviour from a requirement or reasonable user expectation. If expected behaviour is unknown, I classify it as a question or potential defect, not a bug.

**18. What is the difference between severity and priority?**

Severity is the technical impact of the defect; priority is how soon it should be fixed. A blank core screen is high severity and high priority; a small spelling issue on a main page can be low severity but high priority.

**19. What is RTM?**

A Requirement Traceability Matrix links requirements to test cases and defects so that every requirement has coverage and every defect can be traced back.

**20. How did you ensure test coverage?**

I mapped 36 derived requirements to test cases through an RTM, covered each module with positive, negative, UI, network and GPS cases, and tracked uncovered or unclear items.
