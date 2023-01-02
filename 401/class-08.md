## Access Control (ACL)

### 5 Steps to RBAC

1. What is Role Based Access Control (RBAC) and why do we care?
- RBAC involves assigning system access to users based on their role within an organization.
- Access is assigned to each person based strictly on their role assignment. 
- With tight adherence to access requirements established for each role, access management becomes easier. 
- It is much easier to audit user rights and to correct any issues identified. It allows systems to be more secure. 

2. Describe a Role/Permission heirarchy that you might implement using RBAC.
- Office Manager and Dentist will have access to employee payroll and being able to edit clock in/out times. They will have access to patient balances and setting treatment costs.
- Other dental providers will have access to what is necessary for their appointments with patients. 

3. What approach might you take to implement RBAC?
- Figure out what resources you have for which you need to control access. Examples include email system, customer database, contact management system, etc. 
- Group workforce members into roles with common access needs. Keep them as simple and stratified as possible. 
- Assign people to roles and set their access. 
- Resist temptation to make a one-off change for an employee with unusual needs. 
- Periodically review your roles, the employees assigned to them, and the access permitted for each. 

### RBAC

1. If Authentication is “you are who you say you are,” what is Authorization?
- Lets see what you have permission to access based on your specific role. 

2. Name three primary rules defined for RBAC.
- Role Assignment: A subject can exercise a permission only if the subject has selected or been assigned a role.
- Role Authorization: A subject's active role must be authorized for the subject. With rule 1 above, this rule ensures that users can take on only roles for which they are authorized.
- Permission Authorization: A subject can exercise a permission only if the permission is authorized for the subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which they are authorized. 

3. Describe RBAC to a non-technical friend.
- An approach in computer systems security to restricting system access to authorized users based on their role. 

### RBAC Tutorial 
1. What Are access rights Associated with? The User? or The Role? Explain.
- The role, meaning what you do and your function. Based on this, it will determine what files you can access in the organization. 

2. Access Rights, or Authorization, is activated after a user successfully does what?
- Users authenticate themselves into the system and can take on some roles, accessing authorization to resources. 

3. Explain how RBAC might benefit a business.
- Policy is associated with roles and does not need to change when a person leaves the organization. 
- New employees should be able to activate the desired role. 