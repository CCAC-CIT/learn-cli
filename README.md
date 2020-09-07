Intro to the Command Line
=========================

Assumptions: If you're on Windows you have downloaded and installed Git Bash (which comes with [Git for Windows](https://gitforwindows.org/)). If you're on a Mac or Linux machine you won't need to bother&mdash;you already have a Linux-style command line interface.

Steps:
1. **Windows:** open Git Bash.<br />**Mac:** [open Terminal](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)<br />**Linux:** open your terminal, which might work with ctrl-alt-T, or you might have to go searching for it 
2. Usually, the terminal will open up at the home directory for the user who is using it, but let's be really sure:
```cd ~``` &lt;- this says "change directory to my home directory"
3. Now, let's see where home is:
```pwd``` &lt;- this stands for "print working directory"
On my CCAC Windows machine, what prints is ```/c/Users/csheldon-hess/```; yours will be different depending upon your username, your operating system, and how you've got things configured.
4. Is your username part of your home directory? Let's find out what your username is, shall we?
```whoami```
