# Odoo 18 User Initialization from CSV Guide

Based on the Odoo documentation, here are the main ways to initialize users in Odoo 18 from a CSV file of employees:

## Method 1: Direct CSV Import via Odoo UI

**Step 1: Prepare your CSV file**
Create a CSV file with the required user fields. Essential columns include:
- `External ID` (for updates/unique identification)
- `Name` 
- `Login` (username)
- `Email`
- `Password` (optional - users can reset later)
- `Groups` (to assign permissions)

Example CSV format:
```csv
External ID,Name,Login,Email,Groups
user_emp_001,John Doe,john.doe,john.doe@company.com,base.group_user
user_emp_002,Jane Smith,jane.smith,jane.smith@company.com,base.group_user
```

**Step 2: Import via Odoo Interface**
1. Go to **Settings → Users & Companies → Users**
2. Click the **Actions** button (cog icon)
3. Select **Import**
4. Upload your CSV file
5. Map the columns to corresponding Odoo fields
6. Test the import and then confirm

## Method 2: Using res.users Model Import

For the `res.users` model, key fields to include:
- `name`: Full name
- `login`: Username (must be unique)
- `email`: Email address
- `password`: Initial password
- `groups_id`: User groups (comma-separated for multiple)

## Method 3: Employee + User Creation

If you want to create both employee records and user accounts:

**First import employees (`hr.employee`):**
```csv
External ID,Name,Work Email,Department,Job Title
emp_001,John Doe,john.doe@company.com,Sales,Sales Manager
emp_002,Jane Smith,jane.smith@company.com,HR,HR Specialist
```

**Then create users linking to employees:**
```csv
External ID,Name,Login,Email,Employee/External ID
user_001,John Doe,john.doe,john.doe@company.com,emp_001
user_002,Jane Smith,jane.smith,jane.smith@company.com,emp_002
```

## Important Considerations:

1. **Import Order**: Import related records first (employees, then users)
2. **External IDs**: Use unique External IDs for updating existing records
3. **Password Reset**: Enable password reset from login page in Settings → Permissions
4. **User Groups**: Assign appropriate groups like `base.group_user` for basic access
5. **Data Validation**: Test with a small batch first to ensure field mapping is correct

The CSV import method is the most straightforward approach for bulk user creation from your existing employee list.

## Security Notes

- Change default passwords in production
- Assign appropriate user groups based on roles
- Enable password reset functionality for users
- Consider using External IDs for better data management

## Troubleshooting

- If import fails, check field mappings
- Ensure External IDs are unique
- Verify CSV formatting (UTF-8 encoding recommended)
- Test with small batches first