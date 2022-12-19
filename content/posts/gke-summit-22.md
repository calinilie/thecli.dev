---
title: "Gke Summit 22"
date: 2022-12-19T23:39:13+01:00
tags: ["blog", "conference", "google cloud"]
description: "An few personal key takeaways from Google Kubernetes Summit 2022"
image: /images/gke-summit-22.jpg
---

Together with the two great gentlemen and colleagues of mine I had the pleasure of visiting Google’s HQ 
in SunnyVale, California. Google had arranged a 2 day session centered around Google Kubernetes Engine. 
We talked to senior PMs, directors of PM and principal engineers all working on GKE and adjacent 
products. We gained insight into upcoming product releases as well as into how they see the evolution of GKE.

Here are some of my personal key takeaways from the event.

## Adoption of kubernetes
Or rather lack of adoption of kubernetes. What is standing in the way of succeeding with kubernetes?

Culture. Running workloads on k8s is not the same as running pet VMs. 
Why do some (most?) people who’ve been running data centers, massive IT setups, or have been writing code,
for the past 20 years, struggle when having to operate kubernetes workloads? Because running 
ephemeral pods requires a different ethos than running software on a pizza box, or a VM.

## Please run stateful workloads
While running stateful workloads on GKE was a venture for the brave a few years back, it is no longer
 the case. The tooling built into GKE makes it significantly easier to run stateful workloads or 
 even migrate them between clusters with no downtime. It seems like Google is quite invested in assisting 
 its customers with running stateful workloads on GKE.

## Running Windows containers is kinda OK
While they admit that there is limited adoption of Windows containers [relative to Linux containers], 
there is adoption! The licensing model might be a good motivator. One only has to pay a Windows license 
per node. Systems which run many small Windows machines, can significantly reduce the license cost.

## Multi-cloud setup is not a thing
“Ofcourse Google would say that!”. However, this was just an observation. Most customers who run multiple 
clouds are in a transitory phase. They are moving from one cloud to another. 

## Fleets
Running 5 clusters is significantly easier than running 100. Google is heavily investing in tooling 
to make fleet management easy. Anthos is a large component in this endeavor, allowing one to even run 
GKE outside of Google Cloud Platform. 

## Autopilot everything
In almost every session, Autopilot mode was mentioned. This is a great step towards simplifying cluster 
management. They also made it clear that Autopilot would be a fit for power users as well, and their 
intention was not to significantly change the experience of running kubernetes.


There were many more sessions with loads of focus on networking and security. There’s plenty of things 
that I learned and look forward to tinkering with.
