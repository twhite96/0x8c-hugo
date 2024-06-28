---
title: "OWASP Juice Shop and WordPress Setup"
date: 2024-06-28
draft: false
description: "Setting up personal labs outside of HackTheBox and TryHackMe is something I've wanted to do for a while."
tags: ["owasp juice shop", "wordpress"]
---

Setting up personal labs outside of HackTheBox and TryHackMe is something I've wanted to do for a while.
<!--truncate-->

This very early early Friday night/morning, I decided to spin up an LXC of WordPress to pen test (LXCs in this case are very easy to deploy on Proxmox with [Proxmox Scripts Turnkey Appliances](https://tteck.github.io/Proxmox/#turnkey-lxc-appliances)) and [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) in a Docker container.

With the WordPress instance, I plan on playing around with it for brute force password attacks, SQL Injection, and all of that good stuff.

But with the Juice Shop, *that* is where the real test begins.

## Config

I put both the apps on the same subnet as the switch my one old mini PC is that is running a full instance of Kali Linux which will make accessing the IPs of these apps easy.