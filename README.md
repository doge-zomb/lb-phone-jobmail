# Description
This simple and customizable script enables the use of the LB-Phone SendMail exports to send email to players when they are Promoted/Demoted/Hired/Fired from their jobs in a qb-core server. This script is compatible only with qb-core and qb-management, however, it can be quickly changed to support other resources by the server developers.

# Dependencies
  lb-phone
 <br> qb-core 
 <br> qb-management

# Installation

Step 1: Download the resource from the releases page.
<br>Step 2: Extract the files and place them in your server resources directory
<br>Step 3: Add the following code to your qb-management\sv_main.lua:

  <br>Find the ```qb-bossmenu:server:GradeUpdate``` event around line 76
    <br>Add this block of code to the ```if Employee.PlayerData.source then``` statement
   <br> ```TriggerEvent('doge_jobmail:server:gradeUpdateMail', src, Player, Employee, type, initialPosition, data)```

<br>  Find the ```qb-bossmenu:server:FireEmployee``` event around line 132
   <br> Add this block of code to the ```if Employee.PlayerData.source then``` statement
   <br> ```TriggerEvent('doge_jobmail:server:fireMail', src, Player, Employee, type, target)```

<br> Step 4: ensure doge_jobmail at the end of your server.cfg after lb-phone and your qb

# Preview
  Hiring Email:
  
  <img width="333" height="660" alt="image" src="https://github.com/user-attachments/assets/8f94bdb1-3208-41e0-b79a-5cb83672f235" />

  Promotion Email:

  <img width="295" height="660" alt="image" src="https://github.com/user-attachments/assets/fc5767c8-7479-4a69-86de-1157bd7cbabd" />

  Demotion Email:

  <img width="332" height="655" alt="image" src="https://github.com/user-attachments/assets/01fe3181-df10-4f1d-8701-f5b0e4528f73" />

  Termination Email:

  <img width="321" height="670" alt="image" src="https://github.com/user-attachments/assets/87d52322-202d-4591-b312-9670fc21698f" />

  Extra Image to show that the email subject and other factors change based on the hiring persons job and rank

  <img width="342" height="657" alt="image" src="https://github.com/user-attachments/assets/47facbc5-f3a0-49a0-931e-f5f834ceb746" />

  <img width="338" height="644" alt="image" src="https://github.com/user-attachments/assets/f44f4875-a944-4b3f-83c0-1b5d525376ba" />

  # Customization:

You can customize the messages by editing the message variables in the server.lua, a config file is soon to come for convenience.


