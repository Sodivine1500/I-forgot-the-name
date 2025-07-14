**MALWARE ANALYSIS WITH FLAREVM**

I created this virtual lab to get a better understanding on how Malware moves, spreads, and works.

The Lab is isolated from my comptuer so it wouldn't spread out my computer, this is the safest way to do this.

So I first download VMware for virtualization, then I downloaded FlareVm on my computer for all of the cyber forenics tools. 

Then I downloaded high serverity sample malware (15 samples, I got them all from Malware Bazaar), after I downloaded all of them I unzipped the files, That is where it started. Soon as it happened the malware took effect and I starting analyzing the actions.

I started with HxD for data analysis. I then found the SHA-256 for about 8 of them, the rest I found later in the analysis. for now I copy and pasted what I did find in NotePad++.

Next I used PeStudio to analyze the Malware files for any signs that something is rapidly trying to force a command.

I navgiated to the strings and I found information that was valuable and I found the SHA-256 encryptions (Unpacked & Packed)

Curiously, Went to the process tree to see if any malware .exe were opening and were running. I ended up actually find a malware .exe which was a Malware but turned into a DLL.

Now that I found that I wanted to find the Ip that was given to me and where they actually were. Their country code was 22 so I knew that it was coming from a different country (Senegal).

I followed that up to the process monitor to see if there was any malware actively trying to take a command over. I ended up actaully finding a DLL that was brute-forcing actively the security file name was **\Windows\SysWOW64\msasn1.dll**



