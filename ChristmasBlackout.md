**Christmas Blackout Writeup by Vintage.exe 03.12.2021**
**TryHackMe Advent of Cyber Day 3**



1.  Using a common wordlist for discovering content, enumerate http://10.10.76.199 to find the location of the administrator dashboard. What is the name of the folder? 

![gobuster](https://user-images.githubusercontent.com/64281657/144651673-d1644c0a-761b-4cd8-9287-5a25a2889f83.png)

	
    So basically they reccomend using dirbuster but I'm gonna use gobuster (cuz why not?). -> admin


![loginpage](https://user-images.githubusercontent.com/64281657/144651724-5855c00b-7f36-4e26-b6a4-fb7eb7018ede.png)

2. In your web browser, try some default credentials on the newly discovered login form for the "administrator" user. What is the password?

![success](https://user-images.githubusercontent.com/64281657/144651736-b65e0a5e-597c-473a-8b05-27bdf2a8cfde.png)


		Enetering default credentials -> administrator/administrator


3. Access the admin panel. What is the value of the flag?

![adminpanel](https://user-images.githubusercontent.com/64281657/144651740-df2000a0-1cba-488c-9a44-0d3fa63c6afa.png)


		-> THM{ADM1N_AC3SS} 
		
    
Still there is no problem with solving those CTFs. See ya tomorrow!
