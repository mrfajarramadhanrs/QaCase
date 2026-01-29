### Test Case ID: MAN-MOB-AUTH-001
**Title:** Login with valid credentials on WeMine/WeMineOffice
**Priority:** High


**Preconditions:**
- User has valid credentials registered in the system
- User's tenant is properly configured in Tenant Service
- Backend services (User Service, Tenant Service) are operational
- Microsoft authentication service is available

**Steps:**
1. Open Application WeMine
2. Enter valid username
3. Click Continue
4. Verify hit to API /user/who
5. Verify Miscrosoft's screen is displayed
6. Enter valid password
7. Verify hit to API /user/me
8. Verify hit to API /tenant/master
9. Observe Progress bar
10. Wait until progress is 100%
11. Observe restart prompt
12. Click "Restart" text
13. Verify state after restart app


**Expected Result:**
- User successfully authenticates via Microsoft login
- All API calls complete without errors
- Master data syncs with visible progress indication
- Restart prompt appears after first-time master data update
- App functions properly after restart with master data cached locally

### Test Case ID: MAN-MOB-AUTH-002
**Title:** Login WeMine with offline connection
**Priority:** High  

**Preconditions:**
- User has successfully logged in at least once
- Master data has been synced to local storage
- Device has no internet connection

**Steps:**
1. Open Application WeMine
2. Turn off Internet connection
3. Enter valid username and password synced data before
4. Verify the transition is smooth
5. Verify functionality availability

**Expected Result:**
- App operates with cached master data
- No error messages about network connectivity for cached data access