# Active Directory: Password Reset Lockout Policy

<h2>Description</h2>
In this Active Directory Home Lab, I created a full domain group policy object to lock an account after 3 password attempts, lock myself out from a user account, then reset the user account's password.   
<br />


<h2>Languages and Utilities Used</h2>

- <b>Windows GUI</b>

<h2>Environments Used </h2>

- <b>Windows Server 22</b> 
- <b>Windows 11 Enterprise</b> 
<br />
<br />
On the Active Directory server go to Tools>Group Polcy Management.

![1) tools GPmanagement](https://github.com/user-attachments/assets/adea21e1-d170-47ca-9ff2-4a1787875f3f)

<br />
<br />
In Group Policy Management, right click the main domain "GothamCity.local", create new GPO named Account Locky Policy.

![2)GPO for whole domain, right click domain](https://github.com/user-attachments/assets/2208e000-d544-4bbd-a43a-87b33f3960b5)

<br />
<br />
Right click Account Lockout Policy, selec Edit.

![3)edit account lockout policy](https://github.com/user-attachments/assets/b3506868-5c6a-476e-822b-f31a2275772c)

<br />
<br />
Navigate to Account Lockout Policy under Security Settings and select Account lockout threshold.

![4) navigate to account lockout policy](https://github.com/user-attachments/assets/9dd0ec0f-0423-46f9-b11d-9b9109b22076)

<br />
<br />
Check "define this policy setting" and I set the threshold to 3 attempts before lockout. 

![5) lock account after 3 attemps](https://github.com/user-attachments/assets/aab293c8-82d9-46c0-b36a-ea024f8a0b16)

<br />
<br />
I used the suggested lockout duration and reset counter and clicked ok.

![7) use reccomended values](https://github.com/user-attachments/assets/b4da424e-438d-4862-8307-8e83e98bbbe8)

<br />
<br />
Right click Account Lockout Policy and select "Enforced".

![6) click enforced in GPM](https://github.com/user-attachments/assets/1c764d4e-36ff-4761-8c82-a364f5eca7e9)

<br />
<br />
Switched to User account and locked myself out.

![8) locked out of user account](https://github.com/user-attachments/assets/5f32e64c-296e-4dbf-b039-10b023f4ad5c)

<br />
<br />
On Active Directory, select Tools>Active Directory Users and Computers.

![9)tools AD users and computers](https://github.com/user-attachments/assets/478245a9-4c91-445d-be60-9c880af94f0d)

<br />
<br />
USed the search tool to find Bruce Wayne in the "Entire Directory", right clicked user, and select reset password.

![10) search tool, find users, right click reset password](https://github.com/user-attachments/assets/324238d2-14b4-4e0d-b84d-521c3359940e)

<br />
<br />
Entered a password to give to the user to log back in and select "User must change password at next logon", and select "Unlock the user's account".

![11) new password and change pswd at enxt logon](https://github.com/user-attachments/assets/2b140f49-1277-415b-b9ee-bbcb8ddd6a5f)

<br />
<br />
Entered Domain Controller provided password and set a new password for the User account.    

![12) entering new pswd](https://github.com/user-attachments/assets/25bfcd9d-10d0-423f-9dc6-8e2840a57f07)

<br />
<br />
Logged back in. Success.

![13) success](https://github.com/user-attachments/assets/7f50a9e5-1d90-4ca7-83f5-7b03a77acc46)

<br />
<br />
