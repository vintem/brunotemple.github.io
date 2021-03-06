---
layout: post
title: Why and how to install Jeykll (Windows 10)
categories: jekyll
tags: [jekyll]
---

### What is Jekyll?

Jekyll is a static site generator. In simple words, it provides a way for users to have a website without the need of storing its contents in a database. It is a tool to build sites and blogs, like this one.

### Why Jekyll?

Although Jekyll is simple to use, it is powerful and with some creativity, gives you the opportunity to create a great website. It is open sourced and can be hosted on GitHub. I’ll talk about GitHub later, but for now, you have to know that GitHub allows users to host their websites for free.

### How to install Jekyll on Windows 10?

Yes, I know what some people might think. Why I need a tutorial to install a simple program. The answer is: Windows isn’t officially supported by Jekyll. However, Jekyll can run on windows.

1 – Install a package manager called Chocolatey, [Chocolatey link][link to Chocolatey]

2 – Install Ruby via Chocolatey, open a prompt as administrator and type it:

    choco install ruby -y

3 – Download the Ruby development kit windows, [link to download][ruby download] choose the right version for your system, 32 or 64 bits. Extract it in a folder, here's my suggestion: C:\tools\DevKit2

Close the prompt and reopen it. Navigate to the folder where you extracted, in my case: C:\tools\DevKit2; And type: 

    ruby dk.rb init

4 – Still in the same folder edit the file “config.yml”, include the path where Ruby was installed. Ex: -C:/tools/ruby22 (don’t forget the dash before the path)

5 - Execute the command:

    ruby dk.rb install

Close the command prompt and reopen (as administrator) and install Jekyll, must be the 2.4.0 version:

    gem install jekyll:2.4.0
    
6 – Close the command prompt and reopen (as administrator) and install Bundler.

    Gem install bundler
    
    Bundle install
    
7 - Close the command prompt and reopen (as administrator) and install Python.

    Choco install python2

8 -  Check the installation (creating a site):

Close the command prompt and reopen in a folder that you want to (ex: c:\test\):

Execute the commands

    Jekyll new myblog

    cd c:\test\myblog

    jekyll serve

Open your browser in: http://localhost:4000/

Voila: This is your blog.

[link to Chocolatey]: https://chocolatey.org/install
[ruby download]:      http://rubyinstaller.org/downloads/
