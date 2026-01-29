### Test Case ID: MAN-WEB-AUTH-001
**Title:** Login with valid credentials on WeMine/WeMineOffice
**Priority:** High
**Type:** Positive Test


**Preconditions:**
- User has valid credentials registered in the system
- User's tenant is properly configured in Tenant Service
- Backend services (User Service, Tenant Service) are operational
- Microsoft authentication service is available

**Steps:**
1. Open Application WeMineOffice
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


### Test Case ID: MAN-WEB-AUTH-002
**Title:** Login with valid credentials on WeMine/WeMineOffice
**Priority:** High
**Type:** Negative Test


**Preconditions:**
- User has valid credentials registered in the system
- User's tenant is properly configured in Tenant Service
- Backend services (User Service, Tenant Service) are operational
- Microsoft authentication service is available

**Steps:**
1. Open Application WeMineOffice
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


