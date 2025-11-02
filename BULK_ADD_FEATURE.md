# Bulk Student Addition Feature

## Overview
This feature allows administrators to add multiple students at once through the Admin Dashboard, making it easy to quickly populate the system with student records.

## How to Use

### Accessing the Bulk Add Feature
1. Login to the system as an administrator
2. Navigate to **User Management** panel
3. Select the **"Without Account"** tab
4. Click the **"📋 Bulk Add"** button

### Adding Multiple Students
1. In the Bulk Add Students window, you'll see a data grid with the following columns:
   - **First Name** * (Required)
   - **Last Name** * (Required)
   - **Student Number** * (Required)
   - **Email** * (Required)
   - **Department** * (Required) - Select from dropdown
   - **Course** * (Required) - Select from dropdown (populated based on department)
   - **Year Level** * (Required) - Select from dropdown

2. Enter student information directly into the grid:
   - Click on a cell to edit it
   - For dropdown columns, click to select from available options
   - You can paste data from Excel or other spreadsheet applications

3. Add multiple rows by:
   - Pressing **Tab** to move to the next cell
   - Pressing **Enter** at the end of a row to create a new row
   - Using arrow keys to navigate the grid

### Department and Course Selection
- First, select a **Department** from the dropdown
- The **Course** dropdown will automatically populate with courses for that department
- Available departments include:
  - College of Arts and Sciences
  - College of Business Management Education
  - College of Criminal Justice
  - College of Computer Studies
  - College of Education
  - College of Engineering
  - College of Law
  - College of Real Estate Management
  - College of Tourism and Hospitality Management

### Saving Students
1. Click **"💾 Save All Students"** when you're done entering data
2. The system will validate all entries:
   - Checks that all required fields are filled
   - Validates email format
   - Checks for duplicate student numbers
3. If there are validation errors:
   - You'll see a detailed list of errors
   - You can choose to save only the valid entries
4. Successfully added students will be saved to the database
5. The student list will automatically refresh

### Additional Features
- **Clear All** button: Clears all entries in the grid (confirmation required)
- **Cancel** button: Closes the window without saving
- **X button**: Same as Cancel

## Validation Rules
- All fields marked with * are required
- Email must be in valid format (e.g., student@example.com)
- Student numbers must be unique (cannot already exist in database)
- Department must be selected before Course can be selected
- Year Level must be one of: 1st Year, 2nd Year, 3rd Year, 4th Year, or Irregular

## Tips
- You can copy and paste data from Excel or CSV files
- Invalid rows will be skipped, but valid rows will still be saved
- The system shows a summary of successful and failed additions
- After successful save, the main student list automatically refreshes

## Error Handling
- **Duplicate Student Number**: If a student number already exists, that entry will be skipped
- **Invalid Email**: Entries with invalid email addresses will not be saved
- **Missing Required Fields**: Rows with missing required information will be skipped
- **Partial Success**: If some students are saved successfully and others fail, you'll see a detailed report

## Technical Notes
- Uses the same database methods as single student addition
- Maintains data consistency with existing student records
- Thread-safe operations prevent UI freezing during save
- Supports transaction rollback for database errors
