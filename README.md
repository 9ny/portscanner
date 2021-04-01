# portscanner
My port scan project. I made with python and nmap. I will update in the coming days. I'll add more scan parameter for penetration.

#!/usr/bin/env/python
# -*- coding: utf-8 -*-


import os
os.system("apt-get install figlet")
os.system("clear")

os.system("figlet portscanner")

print(""" 
made by devilin9

Welcome to Portscanner.

1) Fast port scan
2) Attempts to determine the version of the service running on port
3) OS detection 
4) Open port scan
""")

islemno = raw_input("Choose an option: ")


if(islemno=="1"):
	hedefip = raw_input("Target IP: ")
	os.system("nmap" + hedefip)
elif(islemno=="2"):
	hedefip = raw_input("Target IP: ")
	os.system("nmap -sS -sV" + hedefip)
elif(islemno=="3"):
	hedefip = raw_input("Target IP: ")
	os.system("nmap -O" + hedefip)
elif(islemno=="4"):
	hedefip = raw_input("Target IP: ")
	os.system("nmap  --open" + hedefip)
		
else:
	print("Unrecognized option. Portscanner has been closed")
