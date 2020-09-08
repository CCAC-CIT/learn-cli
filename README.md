Intro to the Command Line
=========================

Assumptions: 
1. If you're on Windows, you have downloaded and installed Git Bash (which comes with [Git for Windows](https://gitforwindows.org/)). If you're on a Mac or Linux machine you won't need to bother&mdash;you already have a Linux-style command line interface.
1. You've gone through [this deck](https://docs.google.com/presentation/d/14oisMTEG-O-_DnHSfBRCLsuRq041VnJt9qFOAiVhdpI/edit?usp=sharing), either with an instructor or at least on your own.

## Getting started and finding our bearings
1. **Windows:** open Git Bash.<br />**Mac:** [open Terminal](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)<br />**Linux:** open your terminal, which might work with ctrl-alt-T, or you might have to go searching for it 
1. Usually, the terminal will open up at the home directory for the user who is using it, but let's be really sure:<br />
```> cd ~``` &lt;- this says "change my working directory to my home directory"; **remember not to type the &gt;**
1. Now, let's see where home is:<br />
```> pwd``` &lt;- this stands for "print working directory"<br />
On my CCAC Windows machine, what prints is ```/c/Users/csheldon-hess/```; yours will be different depending upon your username, your operating system, and how you've got things configured. That's fine. But you will need to know where your home directory is (write it down if you think you'll forget) and that ```cd ~``` is the shortcut to get there.
1. Is your username part of your home directory? Let's find out what your username is, shall we?<br />
```> whoami```<br />
For me, the output was ```csheldon-hess```, which is, indeed, part of my home path. 
1. What else is here? <br />
```> ls```  &lt;- this lists the contents of the directory<br />
This should give you a list of all of the files and directories inside your home directory. But we can add flags!< br/> 
```> ls -ahl``` &lt;- this lists them, even the hidden files(!!), with a LOT more details<br />
Fiddle around with the flags until you get a version of ```ls``` that you like. Git Bash is a pretty friendly command line interface, with color-coding for different types of files, so I'm generally pretty happy with ```ls -a``` &mdash; unless I need to know file permissions for some reason, in which case I pop the ```l``` back on.


Now we're going to take a quick break from the command line. Using the browser of your choice, visit [the GitHub page that goes with this lesson]() and click the green button showing a downward-pointing arrow and the word "Code" (top right part of the screen), and then choose "Download ZIP." Go ahead and save it; it doesn't matter too much where the zip file goes, but I want you to **unzip the file into your home directory.** (In my case, I'll save it into C:\\Users\\csheldon-hess\\, and I will let it create its own directory, called "learn-cli.")