# Getting started with XAMPP 
The following explains how to install XAMPP (Cross-platform(X), Apache(A),Mysql/MariaDB(M), PHP\(P\), Perl\(P\))

## If you are using a USB Stick

Installing and getting up and running with XAMPP is fairly easy but you need to make sure you download the correct version. You need to make sure you are using a PHP version that is 8.2 or greater. **MAKE SURE YOU DOWNLOAD THE ZIP AND NOT THE .EXE**.

Open a browser and [download this XAMPP version](https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/8.2.12/xampp-portable-windows-x64-8.2.12-0-VS16.zip/download)

Unzip the resulting file into the **root** of your USB drive. It might take a bit of time.

> What do I mean by the root of the USB? When you view the files on the USB there should be a folder called XAMPP. You shouldn't have to click into any other folders first. When you go into the XAMPP folder there should be a file called xampp-control.exe. So the following would be correct **D:\xampp\xampp-control.exe**, and this would be incorrect **D:\xampp-portable-windows-x64-8.2.12-0-VS16.zip\xampp\xampp-control.exe**.

* Navigate to this folder and click on *xampp-control.exe*.
* You might need to select a language
* A control panel should open
* Start the Apache web server
* Start MySQL
* Open a web browser and point it at http://localhost. You should see your xampp homepage.
* Click on phpMyAdmin to check this is also working.

When you've finished working:-
* You have to remember to stop Apache and MySQL before ejecting the USB.
* It's also worth checking on the taskbar under hidden items to make sure you haven't got multiple instances of XAMPP running.

### What to do if XAMPP doesn't work
First double check the following:
1. You have downloaded the correct version. MAKE SURE YOU USE THE .zip. DON'T USE THE .exe.
2. You have unzipped XAMPP into the root of you USB drive. Do not put it in a sub-folder!

This should fix nearly all problems.

### What can else can go wrong?

#### Apache/MySQL won't start
The most likely explanatation is that you have multiple instances of XAMP running which then come into conflict with each other.
- Stop Apache and MySQL
- Close down the control panel.
- Check on the taskbar under hidden items to make sure you haven't got multiple instances of XAMPP running. If you have, right-click and shut them down.
- Use task manager (CTRL+ALT+DEL). Under background process look for *Httpd*, or *Apache* or *mysql*. If any of these processes are running right-click to end the process.
- Restart XAMPP, hopefully everything will now work okay.

#### Apache still won't start
- By default Apache uses port 80. It could be that there is another service running on port 80.
- From the control panel, next to Apache select config, a configuration file will open. On about Line 60 it will say ```Listen 80```.
- Change this to ```Listen 81```
- Save the *httpd.conf* file.
- Try and start the server agin.
  
#### MySQL still won't start
- If when you start MySQL it starts and them almost imediately shuts down, you can try the following fix - https://stackoverflow.com/questions/18022809/how-can-i-solve-error-mysql-shutdown-unexpectedly. Follow the instruction for the highest ranked answer. The ones that start 'Important: do not delete the ibdata1 file. You could destroy all your databases.' Essentially these instructions get you to use the back-up data to fix your database.


#### Important
* It is your responsibility to look after your USB stick. You will probably 
* Back-up your work regularly. It's very easy to leave it in a machine by accident, lose it, damage it, so make sure you back-up reguarly. 


## If you are using your PC/Laptop/Macbook

Go to [https://www.apachefriends.org/](https://www.apachefriends.org/). Select the correct XAMPP version for your platform. Down and run the .exe. file. 

## Where do I put my HTML, CSS and PHP files?
Your web applications are run from the *htdocs* folder.
* Navigate to the *htdocs* folder
* Create a new folder e.g. CHT2520
* Create a simple php page e.g. *test.php* and save it in the *CHT2520* folder
* Navigate to http://localhost/CHT2520/test.php to check it works.


