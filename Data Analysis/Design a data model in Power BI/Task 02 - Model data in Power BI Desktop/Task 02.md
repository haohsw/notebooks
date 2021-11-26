# Model data in Power BI Desktop
## Exercise 1: Create a many-to-many relationship
### Task 1: Get started
### Task 2: Create a many-to-many relationship
- The table displays sales made by each salesperson. However, there is another relationship between salespeople and sales. Some salespeople belong to one, two, or possibly more sales regions. In addition, sales regions can have multiple salespeople assigned to them.
- From a performance management perspective, a salesperson's sales (based on their assigned territories) need to be analyzed and compared with sales targets. In the next exercise, you'll create relationships to support this analysis.
#### Targets
- Create new single relationship
1. Method 01: Drag KEY from TABLE 1 to KEY TABLE 2
2. Method 02: Modeling -> Manage relationships -> New -> Choose TABLE 1 -> Choose TABLE 2 -> Make this relationship active -> Single -> OK
- Create new many to many relationship
1. Method 01: Modeling -> Manage relationships -> New -> Choose TABLE 1 -> Choose TABLE 2 -> Make this relationship active -> Both -> Apply security filter in both directions -> OK
2. Method 02: Drag KEY from TABLE 1 to KEY TABLE 2 -> Double-click the relationship -> Both -> Apply security filter in both directions -> OK
- Edit Relationship
1. Double-click the relationship -> edit -> OK

### Task 3: Relate the Targets table
- Create a relationship from the Salesperson (Performance) | EmployeeID column and the Targets | EmployeeID column.
## Exercise 2: Enforce row-level security

### Task 1: Enforce row-level security
1. On the Modeling ribbon tab, from inside the Security group, select Manage Roles.
2. In the Manage Roles window, select Create.
3. In the Roles box, replace the selected text with the name of the role: Salespeople, and then press Enter.
4. To assign a filter for the Salesperson (Performance) table, select the ellipsis icon (…), and then select Add Filter | `[UPN]`.
5. In the Table Filter DAX Expression box, modify the expression by replacing Value with USERPRINCIPALNAME().
6. Select Save.
7. To test the security role, on the Modeling ribbon tab, from inside the Security group, select View As.
8. In the View as roles window, select the Other User item, and then in the corresponding box, enter: michael-blythe@adventureworks.com
9. Select the Salespeople role.
10. Select OK