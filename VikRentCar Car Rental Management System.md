* Exploit Title: VikRentCar Car Rental Management System - SQLi
* Software Link: (https://wordpress.org/plugins/vikrentcar/)
* Version: 1.4.4
* Vulnerability proof：  
Access by users with low privileges：http://127.0.0.3/wp-admin/admin.php?option=com_vikrentcar&task=overv
![image](https://github.com/BigTiger2020/2025/blob/main/SQL-3.png)
As shown in the image, select Overview from the drop-down menu and click Apply. Use Burp to capture packets and insert an SQL injection statement into the month parameter. You will find an injection with a 5-second delay and a database error.
![image](https://github.com/BigTiger2020/2025/blob/main/SQL-1.png)  
An injection attack was successfully performed using the sqlmap tool. The command used was "python sqlmap.py -r 2.txt --dbms=mysql -p month --current-db".
![image](https://github.com/BigTiger2020/2025/blob/main/SQL-2.png)


