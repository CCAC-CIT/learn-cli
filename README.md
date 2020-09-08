Intro to the Command Line
=========================

##Assumptions: 
1. If you're on Windows, you have downloaded and installed Git Bash (which comes with [Git for Windows](https://gitforwindows.org/)). If you're on a Mac or Linux machine you won't need to bother&mdash;you already have a Linux-style command line interface.
1. You've gone through [this deck](https://docs.google.com/presentation/d/14oisMTEG-O-_DnHSfBRCLsuRq041VnJt9qFOAiVhdpI/edit?usp=sharing), ideally with an instructor or at least on your own.

##Reminder:
* Don't type the &gt; that appears before commands. That just indicates the existence of the command prompt.

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

## Getting some files we'll need
Now we're going to take a quick break from the command line. Using the browser of your choice, visit [the GitHub page that goes with this lesson](https://github.com/ccac-data-analytics/learn-cli) and **click the green button on the right hand side of the screen (it shows a downward-pointing arrow and the word "Code"), and then choose "Download ZIP."** Go ahead and save it; it doesn't matter too much where the zip file goes, but I want you to **unzip the file into your home directory.** (In my case, I'll save it into C:\\Users\\csheldon-hess\\, and I will let it create its own directory, called "learn-cli.")

What you want to happen is that, when you go back into your terminal and type ```ls``` from your home directory, there is a new directory there called "learn-cli" &mdash; if this isn't what happens, hit me up on Slack, and we'll talk through it. 

Assuming that happened, let's explore the ```learn-cli``` directory!

## Exploring, moving around, and making new things
1. You're still probably hanging out in your home directory. Cool, let's say you want to stay there, but you also want to see what's in ```learn-cli``` &mdash; not a problem!<br />
```> ls learn-cli``` &lt;- that's right, you can ```ls``` a different directory than you're currently working in<br />
(Note: you used a ***relative path*** for that. You could do exactly the same thing with an absolute path: ```ls ~/learn-cli``` )
1. ```learn-cli``` has another directory inside it, called ```text_files``` &mdash; to look at that, you can just tack the subdirectory onto the previous command. **But don't type the whole command! Hit the up arrow on your keyboard.** That will bring up your previous command, and you can add ```/text_files``` to the end of it (the full command, then, will be ```ls learn-cli/text_files``` or, if you tried that absolute path up there, ```ls ~/learn-cli/text_files``` )<br />
The up and down arrows let you scroll through your command history. This saves a lot of typing!
1. While we're talking about saving time and typing, do yourself a favor: type the following **but don't hit enter yet:**<br />
```> cd lear``` **now hit tab**<br />
It should have autocompleted to ```cd learn-cli/``` and you can hit enter now. Your working directory is now ```~/learn-cli``` &mdash; if you try ```ls``` in here, you'll see the same things as you did when you listed the contents of this directory from outside of it.<br />
That trick is called **tab completion,** and it serves two purposes:
	1. It saves typing, of course. Really handy when you're dealing with long filenames.
	1. It also serves as an error check. Type the following:<br />
	```> cd lea``` and then hit "tab" - it honks at you and doesn't auto-complete, right? That's because there is no ```learn-cli``` directory inside the ```learn-cli``` directory! <br />
	Go ahead and delete that command.
1. Now, let's say we want a new file in this directory. Not a problem. We'll use the command ```touch``` to create the file. (There are other ways.)<br />
```> touch birds_rock.txt```<br />
```> ls``` <br />
Notice that there is now a file called "birds_rock.txt" in this directory.
1. If we wanted to create an entire new directory, also not a problem. We'll call it "temp_dir":<br />
```> mkdir temp_dir```<br />
```> ls```<br />
Now we have our new file, "birds_rock.txt" and our new directory, "temp_dir"

## TODO:
cd ..
cp
mv
rm
rmdir
*
warning about -rf
less
cat
head
tail
ctrl-c
>
|