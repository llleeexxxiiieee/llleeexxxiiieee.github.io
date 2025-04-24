---
title: "Using Web Pages as a Covert Channel"
excerpt: "Final project for CYBE 4360x: Digital Forensics.<br/><img src='/images/436wireshark.png' style='width:500px;'>"
collection: portfolio
---

## Description
This project aimed to create a digital forensics scenario and a step-by-step walkthrough of how to investigate the scenario, similar to the labs in the class. The areas of digital forensics I decided to focus on in this project are covert channels and network forensics. A covert channel is a method of communication that involves sending data in an unauthorized and unintended manner. The method I chose to utilize for this project is HTTP requests to specific website pages. This is considered a covert channel because the URL of a website is intended for a user to connect to the website, not communicate unrelated data. This relates to network forensics because the investigator looks at packet capture (PCAP) files to discover the covert channel. 

Scenario: The music lyrics from unreleased albums have been getting leaked online. All the albums have one thing in common: their CD covers are printed at the same company, PrettyPrinty. Once that bit of information got out, music labels stopped wanting to work with them. With their business and income on the line, PrettyPrinty hires a group of digital forensics experts to figure out how the data leaked. The company bans the use of phones and cameras on the printing floor, but there are many computers. Looking at packet captures, the investigators find many HTTP requests. They are all to the same simple website with few blank pages and the frequency at which it was visited seems suspicious. Turns out an employee would use the web pages as a covert channel to represent different letters in ASCII. The pages represent 0s and 1s. 

<img src="/images/436diagram.jpg" width="400">
<img src="/images/436wireshark.png" width="400">

## My Role
Project Designer and Lead Developer

This was a solo project and one with a very open-ended description, so I was responsible for coming up with the project idea, deciding what technologies I wanted to use, and determining the scope and complexity all on my own. I chose the scenario by modeling it after some of the assignments in the class were written and inspired by my love for music. I got the idea for the covert channel from the paper _ and modified it. I set up two virtual machines, one to be a web server, the other to be the computer in the factory. I wrote the code that sent requests to the website and captured the traffic using Wireshark. Finally, I put it all together, took screenshots for the step-by-step walkthrough, and wrote a final report.

## Skills or knowledge gained
* Setting up VMs and a network in VMware
* Sending specific HTTP requests using Python
* Capturing web traffic using Wireshark

## Resources used
* Used labs from CPRE 2300 to help understand how to setup a VM
* Johnson, Daryl; Yuan, Bo; Lutz, Peter; and Brown, Erik, "Covert channels in the HTTP network protocol: Channel characterization and detecting man-in-the-middle attacks" (2010). Accessed from [https://repository.rit.edu/other/781](https://repository.rit.edu/other/781/)
    * This paper inspired my covert channel