**Elf HR Problems Writeup by Vintage.exe 01.12.2021**
**TryHackMe Advent of Cyber Day 2**


_It was all about modyfying cookies!_

![login](https://user-images.githubusercontent.com/64281657/144502021-efcb24e4-d1fb-4898-af60-56af661dcf9d.png)

![warning](https://user-images.githubusercontent.com/64281657/144502095-2633aa6b-a9cb-41ca-a1fb-0141516b5fe7.png)

1. Register an account, and verify the cookies using the Developer Tools 	in your browser. What is the name of the new cookie that was created 	for your account?

![cookie](https://user-images.githubusercontent.com/64281657/144502153-3017e95d-b8fa-4a4c-bd7a-b2c866e357a2.png)



        name of the cookie -> user-auth
  

2. What encoding type was used for the cookie value?

        using first seen site with cipher recognizer -> hexadecimal


3. What object format is the data of the cookie stored in?


	![cyberchef](https://user-images.githubusercontent.com/64281657/144502556-f2321310-9c1a-4219-af41-92595d243510.png)


	      simply looking around for object notation -> json (javascript object notation)


4. Manipulate the cookie and bypass the login portal. What is the value of the administrator cookie? (username = admin)


  ![cyberchef2](https://user-images.githubusercontent.com/64281657/144502707-8db758f3-f9b3-4232-b314-786b18ab3b69.png)

      after cyberchef meeting -> 7b636f6d70616e793a2022546865204265737420466573746976616c20436f6d70616e79222c206973726567697374657265643a2254727565222c20757365726e616d653a2261646d696e227d


5. What team environment is not responding?

	    no surprise -> HR


6. What team environment has a network warning?

       simply -> Application


**Second day and still no much effort to handle, but be patience, there is still 22 more days to go...**
