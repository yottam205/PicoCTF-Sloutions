**Python Wrangling**

First things first, I’ve made a new directory in the Webshell called Python Wrangling.
After that I’ve downloaded the files from the challenge’s window, same as I’ve done in the first challenge. (Don’t feel like there’s a need to picture how I’ve done it after the first one)
After downloading all three files, the challenge directory looks like this:

<img width="442" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/f32c94a2-8293-40bb-9a0e-569b624b0860">

I was not really sure how to get started so I just started by opening each file using the ‘cat’ command.
The two text files look like this:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/99539815-a6f1-4019-bcac-e78e372bdb6d">

It seems like the pw.txt file contains a password and the flag.txt.en contains something encrypted or unknown. 
The next this I’ve done was opening the ende.py file using the same command and it looked like this:

1- <img width="254" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/99bca11e-dc09-4381-a05d-03f2c56a1a50">
2- <img width="278" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/f844edff-1827-4129-b7ed-a1847a5d2737">

From a first look it looks overwhelming, but, if you know a little python and start reading between the lines you can get a sense of what is going on. The first line in the file is ‘import sys’ which means that there is a use of the sys library. In most of the cases I’ve seen (and there are not that much of them) it means that the project interacts with the command line, and that every argument in the command line has a role here (I won’t be getting much more then that into the sys library or python explanations). 
Next, you can see the help message that there is in the project, just because it’s the first thing they wrote:

<img width="430" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/4fc4cd3c-c049-41c4-8f05-f8bb22da71fe">

From the help_msg argument you can understand that we need to decrypt the filename pole.txt using this code. Unfortunately, there is no file in that name so I was kind of lost at this moment and went back to the challenge window looking for answers. The hints did not help me at all so I decided to look closer and read through the file again. What I realized is that there are four conditions using ‘if’.
The first one is the condition on how many commands should be written in the command line while using the program. According to that condition, there needs to be 3 or 4 arguments.

<img width="322" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/8c3180bd-c027-48db-bc1f-57b591c28743">

The second one is using -e in the command line, and that is in case you want to encrypt a message. You can see in the help message that you need to write -d or -e before the pole.txt:

<img width="254" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/760551e7-1af2-4319-a0db-836c0fc1239a">

The third condition is using -d and my guess was that it is to decrypt a file, and that is why in the help message it is written with -d:

<img width="455" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/05b9d611-37cb-42a3-9edc-7bee0f1560f9">

and the last one was the help condition, but it is not necessary to post it here since we already know what the help message is.
So at that moment my understanding is that that is an encryption program, and that it can encrypt messages, so what I can do is just try to decrypt the flag.txt.en file and see if that works. So to try and encrypt it, I should write the following in the command line:
‘python ende.py -d flag.txt.en’
After executing it, the program asked me for a password. My guess is that the password is what’s written in the pw.txt file, so I’ve just copied it:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/94cca9c9-a73d-4be1-a0e4-e0364624de8e">

The result is actually the flag. I was a little surprised it worked, but good for me:
	
<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/52ef9b2e-abfd-4a54-976e-cca4709f60c3">