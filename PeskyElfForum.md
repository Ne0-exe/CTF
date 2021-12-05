**Pesky Elf Forum Writeup by Vintage.exe 05.12.2021**
**TryHackMe Advent of Cyber Day 5**


XSS types:

- DOM: Document Object MOdel represents the page as  a programming interface for HTML and XML documents.

- Reflected: supplying data in a HTTP request.

- Stored: being stored on the web application and then gets run when other users visit the site or web page.

- Blind: similar to stored XSS, the only difference is you can't see the payload working or be able to test it against yourself first.

![forum1](https://user-images.githubusercontent.com/64281657/144761612-59adb505-32e1-439c-a5d7-402e8682a62e.png)

![login2](https://user-images.githubusercontent.com/64281657/144761618-996dc716-5ff4-478e-9d94-b1d8792c9946.png)



    By changing password I can see that URL has something interesting to say...
    
    

![change3](https://user-images.githubusercontent.com/64281657/144761624-1529ca5b-8138-4951-91cb-af2117a9a077.png)


![comment4](https://user-images.githubusercontent.com/64281657/144761629-4778186c-55dd-42ee-a38b-6db83bb4967f.png)

    Leaving a comment like this: <script>fetch('/settings?new_password=pass123');</script> has left a mark in source page...


![comment5](https://user-images.githubusercontent.com/64281657/144761635-5f3a0b30-d9f5-4801-a8e3-0fe1959bbf60.png)


    Thanks to that anyone logging to their account will automatically have their pass changed to "pass123"


![grinch6](https://user-images.githubusercontent.com/64281657/144761643-2eb79829-8730-4bdf-8670-eb3deb12b932.png)

    Trap for Grinch has been succesful, let's own the flag.

![grinch7](https://user-images.githubusercontent.com/64281657/144761652-6b11772f-560d-4421-9883-d7012973607a.png)





1.  What flag did you get when you disabled the plugin? 

		-> THM{NO_MORE_BUTTMAS}
    
    
    
_As always see ya tommorow! HO HO HO_
