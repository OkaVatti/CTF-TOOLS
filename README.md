# CTF TOOLS
tools to use for your hacking endeavors : For educational purposes of course

This is not *EVERY* tool that you will need for your CTF. Finding good tools is one of the basic fundementals of hacking. Understanding how they work and what they have to offer, along with their use cases is how you will truely excell above your peers and, maybe, even just make a name for yourself. That is... if you're good enough

____

To begin, let's start off with what I myself have brought to the table. All the tools below can be found here at [THIS](https://drive.proton.me/urls/4D147VZNBR#gxGDQNv1hBpV) link.

- Malware
	- `mlwr` and `REVENG` are the main folders you'll want to look at if you're into that kind of stuff. Not very useful when it comes to a CTF but I thought I'd include it anyway just for you to test and reverse engineer on your own time
		- **NOTE: I SHOULDN'T HAVE TO SAY THIS BUT PLEASE DO NOT RUN THEM ON YOUR ACTUAL MACHINE. FOR THE LOVE OF GOD TEST THEM IN A VIRTUAL MACHINE.**

- Password Lists
	- Several Password lists provided by the kind folks here on github and some hacker forums, the main one, `yourpasswordsucks.txt` being a combined 16 million in total. The tools you'll be using with this are [Hashcat](https://hashcat.net/wiki/) and [John The Ripper](https://openwall.info/wiki/john)
		- note: I have not checked how many of those passwords are duplicates, I couldn't be bothered to check within the few hours I had to compile the list. 

- Tools
	- Webshells
		- Located in `Tools/SecLists/Web-Shells`. The tools themselves are provided by Kali Linux but aren't installed by default. They are basic ones that you could use on any exploitable application that matches.

- OpenBullet2
	- This One's just a big one, you probably wont have to use it that often. Everything pertaining to this application can be found [here](https://github.com/openbullet/OpenBullet2).

- Responder
	- The most recent github version. Way more up to date than the Kali Linux version. **REMEMBER TO RUN IT WITH PYTHON3**

- HackingTool
	- A suite of more applications meant for things such as Pentesting, Exploitation, Post-Exploitation, Phishing, Payload creation, and many more.

____

That's pretty much it for everything I've provided you. Now let's get onto the tools that will be available you with the OS of your choice, whether it be Kali Linux or ParrotOS.

- OpenVPN
	- A simple tool that will allow you to connect to a VPN provided by the CTF Intructor **OR** one that you've planted yourself within the network.

- nmap
	- A tool that allows you to scan the network for open ports on devices. I.E. Port 21, Port 22, Port 80, etc. If the port is open, chances are it is linked to a neseccary exploit
		- basic Syntax you'll need to know:
			- `nmap -sC -sV {TARGET_IP}` is the command that you'll find yourself using a lot in your carreer. If you are unable to find any ports, don't worry, this happens often due to the target attempting to make it look like their system is down or simply non-existent. Try the `-Pn` modifier, if that *still* doesn't work. Try `-p- --min-rate 5000`. Your full command will look something like this 
			- `nmap -p- --min-rate -sC -sV {TARGET_IP}`

- netcat
	- also known as `nc` within the terminal. It is integrated within the *nmap* package. More information can be found [here](https://www.computerhope.com/unix/nc.htm) and[there](https://www.geeksforgeeks.org/introduction-to-netcat/).

- Python 3.0
	- It's truely your best friend. If you need to quickly prop up an http server instance that reports back when a form of http connection is made. Very useful for when you're trying to confirm whether or not a payload as been successfully uploaded durring your exploitation of a system.
		- Syntax for http.server:
			- `python3 -m http.server {port}`
			- Example of `{port}`: 80 or 8000

and finally, last but not least...

- **METASPLOIT**
	- metasploit is a pentesting and exploitation framework designed for, well, hacking. The framework itself contains hundreds, even thousands of exploits for known vulnerabilities. Those for Windows and Linux alike.
	- I honestly cannot teach you this. It's complex as fuck. Just lookup "metasploit tutorial" or "metasploit exploits". You can also look for exploits on **exploitdb**

