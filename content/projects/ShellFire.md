---
title: ShellFire
subtitle: A red vs blue team cyber battleground
date: 2026-01-27
tags: [projects, docker, current]
#bigimg: [{src: "/img/leetnessBanner.png", desc: "1337ness Logo"}]
---
``` THIS IS A WORK IN PROGRESS, CHECK BACK FOR UPDATES ```

Before I became the TA for the Intro to Cybersecurity Course at Utah State, I helped out in the class as much as I could. Towards the end of the semester, the class was doing a Red vs Blue team tabletop simulation. It was pretty fun, and I found it to be a great learning tool for the students. However, it was done on pen and paper, and I thought it would be cool to automate it. 
<!--more-->
Check out the current progress on [my GitHub](https://github.com/BrohdeXC/ShellFire)

## End-Goal Requirements ##
* Students able to connect to their game machine through their browser
* Teams of 7v7, each player with different roles and tools
* Enterprise environment, equipped with databases, login pages, DMZ, logging, and more
* Point system for files obtained / defended at the end of the time limit
* Can run on a small raspberry pi cluster

## Settling on a Framework - Docker ##
I needed something reusable, easy to set up on any computer, and easy for the students to use. Eventually, I settled on using Docker. I've never used it before this project, but it's a great opportunity for me to learn about it.

## Student Connection - VNC ##
The first thing that I wanted to get working was a way for the students to connect to the browser. I remembered back to when I was using Proxmox, all of the VMs I would use VNC. Although there were alternatives such as ttyd or wetty, I opted for VNC because it would allow students to have access to GUI tools such as Wireshark and Ghidra if they wanted.

## Networking - Traefik ##
As easy as it would be for me to just set up one docker compose and have a flat network, I want management for the admin and some routing to simulate a real network. Right now, Traefik looks like the tool for the job.

## To Be Continued... ##
