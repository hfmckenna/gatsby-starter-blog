---
title: Things I Learned On My First Side Project
date: "2018-03-12T22:40:32.169Z"
description: Taking a little inspiration from my past life as a sound engineer when working on my first side project.
---

> Beginners’ Luck is fine for beginners. Beginners don’t know what they can’t do, so the impossible is available. This is also a characteristic of mastery: the assumption of innocence within a field of  experience.

I’d been flying down the side of Mount Codelympus for a while. Blasting through Free Code Camp algorithms and stroking my beard like a wizened guru on zipline challenges.

Getting my head around the intricacies and abstractions of Javascript was really rather enjoyable. While making small front end applications helped put those principles into practice. Or so I thought…

I knew about the importance of taking on side projects from posts on Medium or Code Newbie podcasts. But I’d always found an excuse to avoid starting my own. That was until someone came to me with a fairly simple request at work.

> Colleague: “Alright Hugh, you know a bit about computer stuff don’t you? We’ve got this CSV spreadsheet uploaded to an FTP every day, we just some automation to filter it then sent to a Google Sheet.”

> My Internal Dialogue: “Too easy”, “I’ll be done in a day”, “Not. A. Problem”

Those cock sure responses came quickly to mind. Already being handy with Google Docs I was confident it just needed a little script tinkering and my nascent Javascript skills would see me through. How wrong I was…

This simple task took me into the worlds of Node, Vim, Linux and VPS hosting. My study notes and knowledge of for loops one small part of a bigger goal, getting something to damn well work.

What follows is a documentation of my first fumbled lessons in actually making something and hopefully encourages some other folks taking their first steps outside of tutorials.

## Performance Matters, Even For noobs

My first thought was to simply use a script to download the CSV every time someone opened the Sheet. What could be easier? Just Google around for the right script, modify a few variables to get the columns I need and away we go. There might even be an app on the marketplace!

Little did I consider that the sheer size and formatting of the file in question. With a single cell containing 1000+ word descriptions including HTML. Any automated CSV to sheets transfer was messy and so slow that it precluded any trial and error to get things working properly.

So I already had to consider the potential performance of my solution and getting it to run on a remote server of some kind. Of course from my time spent with FCC I figured the answer had to lie in a nice efficient JSON file, surely? After all countless streams of information are whizzing around the internet every second through APIs.

## Sometimes The Hardest Solution Is The Simplest

Now that I knew I wasn’t getting away with a single step solution I started to look at other higher level applications. Google App Engine has an automated data import that might then be filtered and stored in Big Query. After a bit of time I realised even this would need some server side code to deal with authorisations.

Less high level but still beginner friendly I looked at Heroku and followed the steps to create my first basic app there. While it was great fun noodling around in a terminal for the first time I was heading in a direction that was pretty far off my real objective. Plus when it came to adding extra services I found the nature of a managed environment abstracted things and was often more confusing than helpful.

It was time to stop twiddling around with basic managed web servers and environments; to face up to something that had haunted my dreams since I started to learn to code.

## The Command Line

I’d already rather pretentiously installed the Bash command line interface on Windows 10 and added it to my Start bar, then rarely used it.

Now there was no avoiding it. I needed to get Node JS up and running for this CSV to JSON conversion, plus I knew cron jobs were a good way of automating tasks on Linux servers.

Indeed cron jobs are a great example of the ‘hard is simple’ point as well. While initially opaque, cron jobs are considerably more straightforward and effective than Windows Task Scheduling ever has been for me.

I’d dabbled with Linux before, running a lightweight Ubuntu distro on my ageing laptop. Excel and image editors had always dragged me back to Windows however. My experience with Javascript actually gave me some confidence in navigating the CLI and I’d bought a simple Dell desktop to use as a secondary Ubuntu machine. The WSL terminal on Windows 10 is great but has definite drawbacks and using a Linux machine for coding will increase my familiarity with server side commands, daemons and of course applications like…

## Vim, Ugly Is Beautiful

I’d read about Vim and it’s notoriety for confusing first time users. Partly through a perverse inclination and partly having enjoyed getting to grips with the command line I decided to ignore Nano and give it a go.

It’s great! Certainly not the most intuitive piece of software in the world but navigating the editor in terms of lines, words and bracketed statements makes a lot of sense. Having studied Audio Engineering at university I was very much reminded of Pro Tools or Final Cut, watching people who could navigate and chop audio with minimal mouse swishing.

Similarly as I used Vim and the command line I was reminded of something Robert Fripp of King Crimson said.

> The musician has three disciplines: of the hands, the head, and the heart. Taken together, these form one discipline.

Essentially being in the zone, but where GUI interfaces encourage creative responses they don’t always help you focus and problem solve on multiple levels at once. Certainly in contrast to Windows, where I’ve tried an embarrasing number of text editors, Vim feels great.

## When Stack Overflow Is Not Enough, Take One Step At A Time

For my front end projects and challenges resources like MDN, Stack Overflow and the FCC forum was all I’d really needed to troubleshoot problems. Now I’d stepped into the wilderness of Side Project Land working through my problems linearly was rather overwhelming. Further the early challenges on FCC seem built around solving typical programming conundrums.

It’s rather humbling going from finding a clever recursive function in a self contained problem to a much wider world of making sure you’re even reading the right documentation for your version of MongoDB.

However fundamentally the principle is always the same, just keeping going, breaking things down and moving forward one baby step at a time.

Persevering through my initial problems got me there in the end. From one simple automated file conversion problem I learned a hell of a lot about Node and server side programming.