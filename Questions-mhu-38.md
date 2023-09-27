# Lab03-Mhu-38

###  List the corresponding pages in your text book (Module 3) with the vulnerabilities in this lab. Explain your reasoning in your own words.





### Referenced from CompTIA Security+ Module 3:

####  Page 78-79
#### Vulnerability type: SQL Injection
In the SQL Injection portion of the exercise, I entered the text `' or 1=1 or '` in the email address field. This can give potential attackers unauthorized access by manipulating the SQL query. SQL injetions can be used to manipulate company's database. One can imagine the potential damage that can be done.

The unauthorized access of sensitive data can be used as an internal reference for further attacks on other parts of the business operations. This data can be modified and corrupted, disrupting the business operations both financially and in a reputational sense.

----

#### Page 80 - 81 
#### Vulnerability type: Improper Error/Exception Handling
In the Reconnaissance portion of the exercise, I was able to click on the magnifying glass icon from the "Quick search" link. This prompted the return of an error message that gave me information on the database table being used. Firstly, a potential attacker has gained sensitive information from the internal database structure. Attackers can use this disclosed information to plan out future attacks, and can target further sensitive data by using crafted SQL queries. 

Secondly, the types of sensitive information compromised can be that of customer/employee data, financial information, and propriety details. In the case that this knowledge becomes public, stakeholders can feel that their information has been exploited. To a lesser extend, the business involved will have their reputation take a hit, and on a greater scale, be involved with compliance violations and legal consequences. 

To prevent this, security engineers must have in place proper error handling mechanisms. Error handling should at the least not present any sentitive information.

----
#### Page 78
#### Vulnerability type: Cross Site Scripting 
In the Modifying Source code portion of the exercise, I was able to access and modify the source of the the registration form. This change was able to manipulate the user's access level from "user" (U) to "administrator" (A). I also updated the form's ACTION value to communicate with the server. 

At a glance, it is obvious that this type of data exposure and manipulation allows attackers to gain access to sensitive data as an administrator role. Very similar to the previous types of vulnerability, the attack can use this information to pre-plan and launch further attacks, as well as the compromised status of all stakeholders involved. 

This access, as well as the latter portion of the exercise that manipulates the URL to access the "admin" page, are all part of privilege escalation being done by the attacker. It is important for the security engineer to ensure that no external users can have access to higher-privileged areas within the application, especially without having proper authentication being done. 

----

Overall, it is important for security engineers to have proper access control mechanisms in their applications. One's that enforces privilege management, secure coding practice and regular reviews on its vulnerabilities, and checking input validations to prevent form field vulnerabilities. 