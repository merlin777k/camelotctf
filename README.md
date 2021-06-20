# camelotctf
A Home-Based CTF event using CTFd and NGROK (LINUX BASED MACHINE)
This repo provides a recommended step-by-step procedure on how to 
setup your Home-based or School-based CTF event.
Thanks to CTFd and NGROK

DISCLAIMER: 
This repository and its information is for Educational Purpose Only in light 
of using Capture The Flag (CTF's) events to enhance some Cybersecurity skills.
You are responsible for the consequences of using some tools in non-ethical way.
Support ethical hacking.

=====================================================================
Part1: Setting up your CTFd SERVER (Desktop)
OS: Linux Mint
https://linuxmint.com/

1. Open Terminal and go to downloads directory;
2. Make directory ctf
3. Change directory to ctf and do the following:
$sudo git clone https://github.com/CTFd/CTFd.git
(source: https://github.com/CTFd/CTFd)
4. Change directory to /CTFd. Follow the instructions at CTFd github
5. Finally if successful at same Terminal Window and you used $flask run
hit ctrl-c to stop CTFd. Use the syntax below to bind your IP
(Be sure you know your IP, using ifconfig)
$gunicorn --bind 192.168.254.100:8000 -w 4 "CTFd:create_app()"

Part2: Setting up your machine for ONLINE access using NGROK Tunnel
1. Visit NGROK website : https://ngrok.com/
2. Signup for Free Plan
3. Download your ngrok executatble and be sure to follow instructions.
4. Lets start port forwarding your IP to the world:
$./ngrok http 192.168.254.108:8000
5. If successful you should have your successsful tunnel with a URL.
6. Copy the https url
7. Visit URL shorter: https://bitly.com/
8. paste your ngrok url and click shorten. Share your URL to fellow ethical hackers
or in your community at FB. Have fun in solving challenges !!
----- visit us at our camelotCTF website for updates
https://sites.google.com/view/camelotctf/
