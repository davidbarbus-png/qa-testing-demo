# Test Cases

## Login Functionality

### TC001 - Valid Login
Steps:
1. Open https://www.saucedemo.com/
2. Enter valid username and password
3. Click login

Expected result:
User is successfully logged in

---

### TC002 - Invalid Password
Steps:
1. Enter valid username
2. Enter wrong password
3. Click login

Expected result:
Error message is displayed

---

### TC003 - Empty Fields
Steps:
1. Click login without entering data

Expected result:
Validation message appears
## Advanced Test Cases

### TC004 - Empty Username
Steps:
1. Open https://www.saucedemo.com/
2. Leave username empty
3. Enter valid password
4. Click login

Expected result:
Validation message "Username is required" is displayed

---

### TC005 - Empty Password
Steps:
1. Enter valid username
2. Leave password empty
3. Click login

Expected result:
Validation message "Password is required" is displayed

---

### TC006 - SQL Injection Attempt
Steps:
1. Enter username: ' OR 1=1 --
2. Enter any password
3. Click login

Expected result:
Login should fail and system should prevent injection

---

### TC007 - Very Long Input
Steps:
1. Enter extremely long text (e.g. 500+ characters) into username field
2. Enter password
3. Click login

Expected result:
System should handle input properly and not crash

---

### TC008 - Special Characters Input
Steps:
1. Enter username with special characters (!@#$%^&*)
2. Enter password
3. Click login

Expected result:
System should handle input safely and return proper validation message
