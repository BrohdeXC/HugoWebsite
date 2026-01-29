---
title: Learning Linux Mini-CTF
date: 2026-01-28
tags: [Club]
draft: false
---

The Intro to Cybersecurity Class this week is learning how to use Linux. Since it's still the beginning of the semester, it would be a good idea to have the club review their Linux commands as well. We put together a mini-CTF for the club meeting for students to hone in on their terminal knowledge. From changing directory to steganography, we hid 20 flags for the students to find in a zip file full of red herrings.
<!--more-->

The flags follow this format:
`ClubCTF{5f4dcc3b5aa765d61d8327deb882cf99}`. 

What the students don't know is that the hexadecimal values are MD5 hashes for the final secret password.

## SPOILERS: Where To Find The Flags ##
```
flag01.txt - ls/cat - root directory
.flag02.txt - ls -la - hidden file in root directory
flag03.txt - ls -la - hidden directory in root directory
.flag04.txt - tree -a - LONG directory traversal
flag 0 5.txt - escape chars - careful-naming
flag06.jpg - file/mv - rename files with wrong filetype
flag07.txt - 7z x nested.7z - Unzip a 7z archive
flag08.txt - grep - grep for the flag in loreum ipsum
flag09.part* - cat / > / >> - cat out all parts of the file and paste into new file
flag10.txt - base64 - encodes the flag in base64
flag11.py - grep - hidden in a code comment
flag12.bin - strings - hidden in the strings of the binary
flag13.txt - rev - reversed base64 text
flag14.txt* - unicode - zero width chars
flag15.json - jq - json parsing
flag16.zip - unzip / john - password protected zip files
corrupt17.zip - 7z x - Fix a corrupted zip file. 7zip is pretty good about extracting anyways
flag18.png - steghide - Hidden file using steganography **hiddenmessage** 
flag19.txt - hexadecimal - Which one is actually valid hex?
flag20.jpg - finale - Steghide, password protected zips, zip2john, 1337haxorz, sheer awesomeness, !!!secret!!!
```
