Forensics Challenge 5 : I need to Hack Potter 

      
Description: 


The task is about network forensics / packet analysis. PCAP file was given we have to inspect that file and extract hidden flag from it. 


Approach :  

At first I opened the pcap file and checked packet count , duration and protocol. Next I checked what protocol existed. I found that TCP was the protocol. Then I checked the TCP Streams if TCP existed. Then I got the streams of TCP protocol. I reconstructed it each stream and checked the ascii contents in it. While checking the ascii contents in stream 3 I found a human readable text and gave it as password. Then I noticed that there is one more hidden password so I checked the file for another human readable form and got another human readable text which is the password. 


Tools / Commands Used :  


1. file challenge.pcap 

2. tshark -r challenge.pcap -Y "tcp" | wc -l 

3. tshark -r challenge.pcap -T fields -e tcp.stream | sort -n | uniq 

4. tshark -r challenge.pcap -q -z follow,tcp,ascii,3 

5. strings challenge.pcap | less
   
6. zipinfo → Inspect archive 

7. unzip → Extract ZIP 

8. file → Identify real file types 

9. strings → Extract printable data 

10. binwalk → Detect embedded payloads 

11. base64 → Decode encoded data 

Final Flag : ACM{w3_4r3_cyb3r} 

 
