### Test Case ID: MAN-WEB-FORM-001
**Title:** Create Dynamic Form with Maximum Fields
**Priority:** High 
**Type:** Positive Test

**Preconditions:**
- User is logged into WeMineOffice
- User has permissions to create forms
- Form Builder feature is accessible

**Test Data:**
- Form Name: Heavy Equipment Daily Inspection
- Total Fields: 50 (maximum allowed)
- Field Distribution:
 15 Input Text fields
 10 Date Picker fields
 10 Select fields
 10 Radio fields (each with 4 options)
 5 Image Picker fields

**Steps:**
1. Go to Form Builder
2. Click "Create New Form"
3. Enter form's Name field "Heavy Equipment Daily Inspection"
4. Add 15 "Input Text" fields with labels
5. Add 10 "Date Picker" fields
6. Add 10 "Select" fields with dropdown options
7. Add 10 "Radio" fields with 4 options
8. Add 5 "Image Picker" fields
9. Verify total field count 
10. Click "Save Form" 
11. Assign form code: HEDI-001
12. Change status to Published

**Expected Result:**
- All 50 fields are created successfully
- Form is saved and published successfully
- Form code is properly assigned
