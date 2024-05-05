# PicoCTF-Sloutions
#### Below are my attempts to solve the PicoCTF challenges
#### Please note that here are all of my solutions, but, I also made a file for each challenge so it might be easier for you to look them up by their subject or name.

**PicoCTF – How I’ve done things:**

I am just getting into the world of cyber security and one of the million things I’ve heard in the past few weeks is CTF or Capture the Flag. Which is a kind of a technical challenge you need to complete. Here I’m trying to show my ways of making these challenges. It is well worth to note that PicoCTF is a middle/high school aimed platform, meaning they aim for that age. But, as a beginner in Cyber Security I believe I can get great value from these challenges and then, move on to others.
It is worth noting that I have started solving these challenges during on doing the Google Cyber Security certification and after studying both introduction to computer science (CS50) and introduction to programming with Python (CS50P) from EdX and Harvard Uni.

**Questions**

<details>

<summary>General Skills</summary>

|Question|Points|
|--------|------|
|[Obedient Cat](General%20Skills/Obedient%20Cat.md)|5|
|[Python Wrangling](General%20Skills/Python%20Wrangling.md)|10|
|[Wave a Flag](General%20Skills/Wave%20a%20Flag.md)|10|

</details>

<details>

<summary>Cryptography</summary>

|Question|Points|
|--------|------|
|[Mod26](Cryptography/Mod26.md)|10|

</details>

<details>

<summary>Forensics</summary>

|Question|Points|
|--------|------|
|[Information](Forensics/information.md)|10|

</details>

# All Questions

**Obedient Cat**

After signing up, that’s the first challenge I saw:

<img width="198" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/f4f166e2-4e74-4127-afe1-2ec3ba17ea54">

I started by entering the Webshell. There you need to enter your username and password to start using the platform. 
I’ve made a new directory with the name of the challenge so it’ll be organized and navigated to that directory.

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/5fdfe624-d9a1-4702-a527-58a4a76611f0">

Then I went back to the challenge and right clicked on the link so I can get the download link in to the shell: 

<img width="221" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/ef19a951-0d38-4ecd-b79f-ef894e0752c2">

In the shell I’ve downloaded the file using the ‘wget’ command and pasting the url I’ve copied:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/f32623b2-ea51-4c00-982f-27edc32e2332">

As you can see in the picture, there was only one file named “flag”, not specifying what kind of file it is.
I tried to open the file using the ‘cat’ command and inside the file was the flag:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/792c05fb-162f-472c-9818-7f865d184463">


I didn’t feel it was necessary to take pictures of pasting the flag back in the challenge window.
The challenge was super easy and required almost no previous skills to figure out what is going on in it. Please note I didn’t use the hints although it is important to feel free and comfortable to use them, because at the end of the day, what we’re trying to do is to learn.

 
**Mod 26**

This challenge is in the Cryptography section and it is pretty straight forward as well:

<img width="272" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/e2ddc7fe-1633-486f-975f-f5df64dc8da6">

By reading the challenge the first bumped into my mind is one of the simplest algorithms of cipher encryption since the challenge asks wat is ROT13, and in cipher encryption, ROT stands for rotate by, which means that you can look at the A, B, C as if it was place on a wheel and each letter change counts as one ROT. With that in mind, I really didn’t want to do it manually and count 13 letters from each letter of sign so I look up on google a ROT13 decryption and got into the first option I saw.
There, I’ve copied and pasted the encrypted part from the challenge window to the ROT13 decryption website and what I got was the flag:

<img width="272" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/b313c755-0b7e-4145-92d2-eae914824d82">

From there I’ve just copied and pasted the flag into the challenge window and that was it.

 
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


**Wave a flag**

To be honest, I found out that how I solved this challenge was wrong, so ill post here the way I’ve done it and the way it should be.
My way:
So I started with making a new directory and getting the relevant file in it. After that I tried to open the file using the ‘cat’ command and got overwhelmed with some weird text I didn’t knew what to do with (I won’t be posting the whole file, just the begging because that is what’s relevant):

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/e455b461-ae02-4d1c-a789-161798e5d1df">

Looking closer I saw what’s written with the help thing that I’ve marked in the picture, so I just copied the flag and that was it, but it felt like I’ve missed something so I went back to the challenge window and tried to look in the hints.
That’s the way it should be solved:
After downloading the file into the folder, hint number three recommended on entering ‘./warm’ which is a way of running a script or a program.
After running that, it said permission denied:

<img width="416" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/2fdc8f6e-29d9-486f-a28a-e7f4840f8155">	

So I guess what I need to do is to change the files permission. Before that I checked what is the files permission by executing ‘ls -l’. after that, I changed the file permission to all the users by executing ‘chmod +x warm’:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/d616ebb0-4b8c-4323-b0fa-5ffe143fb092">

Then I tried running the script once again by executing ‘./warm’. And after it asked me to use ‘-h’ for help I got the flag but in the right way this time:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/1895c0ce-f159-43a7-b0fd-0d9c67270409">


**Information – Forensics – 10 Points**
This challenge was a little more challenging for me then the others. 
I started as usual, by downloading the relevant file. After reading the instructions, that says that “Files can always be changed in a secret way”, I thought that the file might have been changed and that I need to figure out what file type it should be. So first I tried to open the file, which I had not permission to, then I tried to look on the file’s info using ‘file’ and stat’ command and see if it is a jpg file:

![information 1](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/b75ded8e-be7f-4fda-ad6c-4c8daebddaa8)


The only clue I got from using these commands is that the file is a picture and that it should be a picture. At that point I was completely lost. I tried to open the file in different ways, I tried to change the file type, just because of the instructions, but no fruits came out of it either. So, I tried see a hint and see what I can get from it. The first hint says “look at the details of the file”, which probably mean that the flag is somewhere in the file’s details and that there is got to be another way to view those details so I started looking for that way. One of the ways I found Is using ‘more’ and ‘less’. 
The ‘less’ command gave no fruits either, but, using the ‘more’ command, I saw something which I thought is suspicious in the file’s license line so I decided to see how I can view it in a different way. I thought it is suspicious because it looks like the resource of the license is encoded or encrypted:

![information 2](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/43fc5c39-885e-4c73-b832-20b25a6f43d3)

From searching other ways to see the file’s data or information to check if the license is what I saw I bumped into the ‘exiftool’ command that shows the file’s meta information, and the lincese was the same there, so now I only had to figure out if it is encoded or encrypted and how I can know how it had been encoded or encrypted so I’ll be able to decode or decrypt it:

![information 3](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/03978642-b62e-473d-b05b-57feffe36fa2)

My feeling was that the odds are the string is encoded, because there is no data transmission here and if it had been encrypted, to decrypt it will demand harder work finding the kind of encryption and the key etc., and that felt like it is not the kind of things they came to do here, so I decided on trying to decode the string and see what I get. From what I found on forums, odds are the string encoded using Base64 so I decided to try to encode it with ‘base64’ command and it did work and I found the flag in it! (The command I used to decode is ‘echo “the string” | base64 -d’):

![information 4](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/9d183d55-47d0-4e47-a000-2ad6357637cd)
