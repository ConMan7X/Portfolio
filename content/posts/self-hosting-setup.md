---
author: "Connor Schicht"
date: 2025-12-21
linktitle: Self Hosting Setup
menu:
  main:
    parent: self-host
title: Self Hosting Setup
weight: 10
---

## Introduction

Recently, I have been inspired to use my own hardware and storage to self-host my own private information, private entertainment,
and any other private services I may want to host. This project has been greatly inspired by the sheer number of services that
require subscriptions, the pricing of those subscriptions, and finally, the desire to be in control of my own data.

## Step One: Acquiring the Hardware

Hardware, being the first step in a project like this, can definitely be very daunting, as it often requires quite a large investment
for something that you haven't even experimented with yet. Luckily, I had gotten a taste of self-hosting some very basic services
on my old MacBook Pro, which was sitting covered in dust, forgotten from my high school days. This small bit of experience had
given me the confidence and the desire to make a bigger investment.

My plan has always been to purchase a small mini computer that would be low in power consumption but has expandability
for future requirements, especially storage. This idea ruled out a Raspberry Pi for my needs as, any expandability would
increase connections or complexity of the machine. The price of Raspberry Pis was also a major factor, with even older
generations costing more than $150 in Australia. I settled on finding a small Dell or Lenovo mini PC, preferably used
on eBay for extra savings.

After many weeks of looking around at the different options on eBay or refurbished sites, I finally started placing bids
on a 7th Gen Intel Lenovo Mini PC with 8GB of RAM. In the end, I managed to snag a used one for $150AUD. I landed on
this specific PC as the 7th Gen Intel chips are capable of hardware transcoding H.265/HEVC, which I figured would be worth
the extra $30 while I'm setting up my whole operation.

## Step Two: Deciding on an Operating System

On the other side of the server is the software, and the decision that had to be made about the operating system and how I
would host my services. I had heard a lot of good things about Proxmox, a bare-metal operating system that allows you to
easily run many different virtual machines on your computer. Instead, I chose to keep it simple with software I already
have experience in and that I thought would be a bit more hands-on and fun.

I ended up going with a bare-metal install of Debian Linux, running in headless mode, but I did also set up a VNC server
if I needed to have a GUI. For the services, I will choose to go with Docker containers using Docker Compose to allow
for some YAML files that I can backup, as well as an easy way to update the services in the containers.

## Step Three: Starting the Servers

The final step in the setup phase was to start doing some self-hosting! I chose to take it slow with this
and ended up starting with [Mealie](https://mealie.io), a recipe manager. This was nice and easy to set up using the Docker
Compose documentation, which would end up being a common theme with all of these open source services; the documentation
is always very good. I also decided to set up a dashboard for my home server, for which my choice of software was
[Homepage](https://gethomepage.dev/). I thought this was a very simple but very nice-looking dashboard. I particularly
like how easy it is to customise, as well as all of the widget integrations with different services that are possible.
