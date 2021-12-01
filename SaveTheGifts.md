**Save the Gifts Writeup by Vintage.exe 01.12.2021**
**TryHackMe Advent of Cyber Day 1**

The whole idea of this ctf is to see how IDOR (Insecure Direct Object Reference) works in practice. We can simply apply numbers from 1 to 20 applied to user_id in URL.

![url](https://user-images.githubusercontent.com/64281657/144307882-daf7acfc-6324-41cd-b22a-91955c3667b7.png)

1. _After finding Santa's account, what is their position in the company?_

	Santa's account is hidden under number 1 of user_id. His position -> The Boss!


2. _After finding McStocker's account, what is their position in the company?_

	McStoker's id is no. 3 and his position -> Build Manager


3. _After finding the account responsible for tampering, what is their position in the company?_


	Well, well, well...surpise, surprise. Person(?) standing behind the tampering is Grinch and his position is -> Mischief Manager (*badum* *tsss*)


4. _What is the received flag when McSkidy fixes the Inventory Management System?_

	All I had to do is to click 'Revert' button few times. After that window with flag appears -> THM{AOC_IDOR_2B34BHI3}
