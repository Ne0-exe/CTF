**Santa's Running Behind Writeup by Vintage.exe 04.12.2021**
**TryHackMe Advent of Cyber Day 4**



- Authorisation =/= Authentication. The first one is a term for the rules defining what an authenticated user can or cannot acces!

- Fuzzing- is an automated means of testing an element of a web application until the application gives a vulnerability or valuable information. Do something 'till you find something useful with much faster rate _(self-interpretation)_ .


All I had to do in this task is to configure BurpSuite to fuzz vulnerable site and retrieve Santa's password. 

![login2](https://user-images.githubusercontent.com/64281657/144722683-4580ed37-b95d-451a-943a-a1e30c838896.png)

![burp1](https://user-images.githubusercontent.com/64281657/144722633-d9261020-7782-4077-a535-f95705de97e5.png)

![burp2](https://user-images.githubusercontent.com/64281657/144722638-e671ac1f-fd2f-45b3-9697-9715c2a6d2a3.png)

![burp3](https://user-images.githubusercontent.com/64281657/144722643-5f6f036c-d7d2-4371-af34-7f979c55801b.png)


***Eventually I used list posted on THM exercise because it was modified list for this ctf, use it!***


1. What valid password can you use to access the "santa" account?

![burp4](https://user-images.githubusercontent.com/64281657/144722645-cbf699e3-73dd-4085-8ec2-1704cff2ff9f.png)


		-> cookie





2. What is the flag in Santa's itinerary?

![burp5](https://user-images.githubusercontent.com/64281657/144722653-2d4936e4-75a5-4e5a-8688-41046a549aa7.png)

	
		-> THM{SANTA_DELIVERS}
    
    
_See ya tommorow_
