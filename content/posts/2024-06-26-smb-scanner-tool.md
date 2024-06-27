---
title: "Creating My Own SMB Scanner"
date: 2024-06-26
draft: false
description: "A proof of concept that enables a better of understanding of more popular tools and how they work to find open shares on a target host."
tags: ["nmap", "smb", "smb enumeration"]
series: ["Building an SMB Scanner"]
series_order: 1
---

A proof of concept that enables a better of understanding of more popular tools and how they work to find open shares on a target host.
<!--truncate-->

One of the things I am consistently learning while embarking on this career pivot to cybersecurity is how much of a leg up building your own tools, blogging, and networking can get you when trying to enter the field with no prior (cybersecurity) experience.

I have software development experience which makes building my own tooling super fun for me. I've already built a DDoS Script and an DNS Enumeration tool, but those are no where near the projects I want to build and showcase.

{{< github repo="twhite96/ddos-script" >}}
<br>
{{< github repo="twhite96/simple-dns-enum-tool" >}}

The DDoS script was the most challenging and most rewarding of the two because of how much I struggled to build it, to get my head around Python, a language I hadn't used in 9 years. The DNS enumeration tool was built as part of a YouTube video I watched from a guy that works at TryHackMe now and I put little though into it.

Now, I feel I am ready to build my own tools. I've [written some thorough notes](https://notes.0x8c.org/Scripting-Notes/SMB-Scanner-Tool) about the design of this tool, but here are the basics:

1. What should the script do?
2. What does it accomplish that `nmap` and `rustcan` do not?
3. How will you utilize the goals of other, more established scripts to build your own?

{{< alert icon="lightbulb" cardColor="#B7FF96" iconColor="nearblack" textColor="nearblack">}}
I've answered these questions with the following:
{{< /alert >}}

### The script should only do ***four*** things

* List server shares
* Find null authentication
* Enumerate shares
* List permissions on each shared directory

That seems like a fair amount of tasks for the script to accomplish for now.

## Building

I've started building it already. You can find it on my GitHub account.

{{< github repo="twhite96/smb-scanner" >}}