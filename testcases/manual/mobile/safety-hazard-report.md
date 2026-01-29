### Test Case ID: MAN-MOB-INSPC-001
**Title:** Submit Inspection on WeMine with internet
**Priority:** High
**Type:** Positive Test

**Preconditions:**
- User is logged into WeMine Mobile
- Form HEDI-001 (Heavy Equipment Daily Inspection) exists and is published
- Master data is synced to mobile device
- Device has internet connection

**Steps:**
1. Open WeMine Mobile appApp home screen displays
2. Tap "Equipment Inspection" menu
3. Tap "New Inspection" buttonForm selection screen appears
4. Select form code: HEDI-001 
5. Fill all 15 text input fields 
6. Select dates in all 10 date picker 
7. Choose options in all 10 select fields
8. Select options in all 10 radio fields
9. Capture/select images for all 5 image picker fields
10. Review completed form
11. Tap "Submit"
12. Verify API call to backend
13. Check submission confirmation 
14. Return to Equipment Inspection list

**Expected Result:**
- Form loads with all 50 dynamically created fields
- All backend API shows success
- All field types function correctly
- Form submits successfully with online connection
- Submission appears in previous submissions list

### Test Case ID: MAN-MOB-INSPC-002
**Title:** Submit Inspection on WeMine with internet
**Priority:** High
**Type:** Positive Test

**Preconditions:**
- User is logged into WeMine Mobile
- Form HEDI-001 is synced to device
- Master data is synced to mobile device
- Device has no internet connection 

**Steps:**
1. Disable internet connection
2. Open Equipment Inspection feature
3. Tap "New Inspection"
4. Select form code: HEDI-001
5. Fill all form fields (50 fields total)
6. Capture images using camera
7. Tap "Submit"
8. Check submission list
9. Enable internet connection
10. Observe automatic sync
11. Verify backend submission
12. Check submission status update

**Expected Result:**
- Form functions fully in offline mode
- Data is queued locally when offline
- Auto-sync occurs when connection is restored
- No data loss during offline-to-online transition

### Test Case ID: MAN-MOB-INSPC-003
**Title:** Submit New Hazard with Notifications
**Priority:** High
**Type:** Positive Test

**Preconditions:**
- Reporter is logged into WeMine Mobile
- Master data (locations, sublocations, areas, employees) is synced
- Device has internet connection
- Notification Service is operational

**Test Data:**
- Reporter: X (Employee ID: EMP001)
- Location: North Mining Site
- Sublocation: Sector A
- Area: Excavation Zone 3
- Area Description: Near the main conveyor belt
- PIC: A (Employee ID: EMP002, Supervisor)
- Other employees in area: B,C (EMP003, EMP004)

**Steps:**
1. Open WeMine Mobile app
2. Tap "Hazard" menu
3. Tap "Report Hazard" button
4. Tap "Location" field
5. Select "North Mining Site"
6. Tap "Sublocation" field
7. Select "Sector A"
8. Tap "Area" field
9. Select "Excavation Zone 3"
10. Enter "Near the main conveyor belt" in Area Description
11. Tap "Evidence" image picker
12. Capture/select hazard photo
13. Verify PIC field
14. Tap "PIC" field to change
15. Select "A" as PIC
16. Review all mandatory fields
17. Tap "Submit"
18. Confirm submission API hit 
19. Verify hazard entry creation
20. Verify followup task creation
21. Check PIC notification
22. Check area staff notifications
23. Verify notification content for PIC
24. Verify notification content for area staff

**Expected Result:**
- Hazard report form validates mandatory fields
- PIC field pre-selects to reporter by default
- Form submits successfully with all data
- Hazard entry and followup task are created in backend
- PIC receives followup task notification
- All employees in the affected area receive hazard notification
- Notifications are delivered via Notification Service

### Test Case ID: MAN-MOB-INSPC-004
**Title:** Complete Followup Task with Multiple Co-Observers
**Priority:** Critical
**Type:** Positive Test

**Preconditions:**
- Hazard report exists with follow up task assigned to A
- A is logged into WeMine Mobile
- Device has internet connection

**Test Data:**
- PIC: A (EMP002)
- Direct Supervisor: D (EMP005, Area Supervisor)
- Co-Observers: E (EMP006), F (EMP007), G (EMP008)
- Resolution Date: 2026-01-29 14:30

**Steps:**
1. Login as A
2. Check notifications
3. Tap notification
4. View hazard details
5. Tap "Complete Followup" button
6. Tap "Evidence" image picker
7. Capture resolution photo showing fixed hazard
8. Tap "Resolution Date" field
9. Select date: 2026-01-29 and time: 14:30
10. View "Co Observer" field
11. Tap first co-observer select field
12. Select "E" (EMP006)
13. Tap (+) button to add another co-observer
14. Select "F" (EMP007)
15. Tap (+) button again
16. Select "G" (EMP008)
17. Verify all mandatory fields 
18. Tap "Submit Followup"
19. Confirm submission
20. Verify followup task status is Completed
21. Verify notification to supervisor
22. Check supervisor notification content
23. Login as Supervisor 
24. View completed followup task
25. Verify co-observers list

**Expected Result:**
- PIC can access followup task from notification
- Evidence photo upload works correctly
- DateTime picker functions properly for resolution date
- Co-observer functionality allows multiple additions via (+) button
- Form validates mandatory fields (Evidence, Resolution Date)
- Followup task completes successfully
- Direct supervisor receives notification
- All followup data (photo, date, co-observers) is saved correctly
- Workflow Service properly processes task completion

### Test Case ID: MAN-MOB-INSPC-005
**Title:** Offline Hazard Submission and Sync
**Priority:** Medium
**Type:** Positive Test

**Preconditions:**
- User is logged into WeMine Mobile
- Master data is synced locally
- Device has NO internet connection

**Steps:**
1. Disable internet connection
2. Open "Hazard" menu
3. Tap "Report Hazard"
4. Fill all mandatory fields with test data
5. Capture hazard photo using camera 
6. Tap "Submit"
7. Check hazard list
8. Enable internet connection
9. Observe automatic sync
10. Verify backend processing
11. Verify notifications sent
12. Check hazard status

**Expected Result:**
- Hazard reporting works fully offline
- Photos are captured and stored locally
- Data queues for sync when offline
- Auto-sync occurs upon reconnection
- Notifications are triggered after successful sync
- No data loss during offline operation