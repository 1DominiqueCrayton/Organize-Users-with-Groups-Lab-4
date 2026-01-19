# Organize Users with Groups — Lab 4  
## Use the Okta Expression Language in a Group Rule

## Objective
Create a group and automatically assign users to it using a rule that leverages the **Okta Expression Language**.

---

## Scenario
You will create a **Finance and Accounting – Employees Only** group.  
Users will be automatically added to this group based on their **department** and **user type**.

---

## Create a Group

### Step 1
From the Admin Console, go to **Directory > Groups**.

---

### Step 2
Create the **Finance and Accounting – Employees Only** group.

<p align="center">
  <img width="1030" height="453" alt="image" src="https://github.com/user-attachments/assets/69a945d4-3482-425e-ad1a-66559de86193" />
</p>

---

### Step 3
Refresh the browser page.

---

## Add a Group Rule

### Step 1
From the **Groups** page, select the **Rules** tab.

---

### Step 2
Add a rule to assign employees in the **Finance** or **Accounting** departments to the **Finance and Accounting – Employees Only** group:

a. Add a rule named **Finance and Accounting Employees**  
b. For the **IF** condition, select **Use Okta Expression Language**  
c. In the expression field, enter the following: (user.department=="Finance" || user.department=="Accounting")
&& user.userType=="Employee"

d. For the **THEN** condition, assign users to the  
**Finance and Accounting – Employees Only** group  

<p align="center">
  <img width="1081" height="507" alt="image" src="https://github.com/user-attachments/assets/c4654ebc-7368-4b0c-a140-4303460b840f" />
</p>

e. Save the rule  
f. Activate the **Finance and Accounting Employees** rule  

<p align="center">
  <img width="1304" height="545" alt="image" src="https://github.com/user-attachments/assets/536564cf-ed07-4058-80f5-a1d9798fb0fe" />
</p>

g. Verify that the **Finance and Accounting – Employees Only** group includes:
- **2 employees** from the Finance department  
- **1 employee** from the Accounting department  

<p align="center">
  <img width="1315" height="626" alt="image" src="https://github.com/user-attachments/assets/26505a80-c53f-4257-b08a-a6b89a6855cc" />
</p>

