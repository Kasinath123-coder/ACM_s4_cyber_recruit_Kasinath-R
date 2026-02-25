MISC Challenge 2 :  This is for you know who 

Description : 

We are given a MISC challenge containing a downloadable archive. We have to identify the hidden flag. 

Approach :  

First step was examining contents.Then extracted archives. Analyse receiver.txt . Analyse top secret.png . Binwalk scan the file , extract embedded data . And then I explored zip payload and got a file important.txt and read the contents inside it. Then investigated a hidden directory and found a jpg file . Did strings analysis on that file and got a key. Then decoded it and got the flag. 

Tools / Commands used : 

1.  zipinfo 
2. unzip 
3. file 
4. strings 
5. binwalk 
6. base64 
7. echo 

Final flag : potter{7h15_15_D010r35_Um8r1dg3} 
