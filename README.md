# PicoCTF-Sloutions
# Introduction
I am new to cybersecurity and recently learned about CTF (Capture the Flag), a type of technical challenge. In this document, I will share my approach to solving these challenges. Although PicoCTF is designed for middle and high school students, I find it valuable as a beginner. I started solving these challenges while working on the Google Cyber Security certification and after completing the "Introduction to Computer Science" (CS50) and "Introduction to Programming with Python" (CS50P) courses from EdX and Harvard University. I will continue to add content as I delve deeper into the world of cybersecurity and as I take and complete additional courses.

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

 

## 4. Wave a Flag

To be honest, I initially solved this challenge incorrectly, so I'll post both the incorrect and correct methods here.

### My Way:
I started by creating a new directory and downloading the relevant file into it. After that, I tried to open the file using the `cat` command but was overwhelmed by some unreadable text (I'll show only the beginning since that's what's relevant):

![Initial Attempt](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/e455b461-ae02-4d1c-a789-161798e5d1df)

Upon closer inspection, I noticed a hint in the text and simply copied the flag from there. However, it felt like I missed something, so I went back to the challenge window and looked at the hints.

### The Correct Way:
After downloading the file into the folder, the third hint recommended running `./warm`, which is a way to execute a script or program. However, running the command resulted in a "permission denied" error:

![Permission Denied](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/2fdc8f6e-29d9-486f-a28a-e7f4840f8155)

To resolve this, I checked the file's permissions using `ls -l` and then changed the file permissions to be executable by all users with `chmod +x warm`:

![Change Permissions](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/d616ebb0-4b8c-4323-b0fa-5ffe143fb092)

Then, I tried running the script again by executing `./warm`. After it prompted me to use `-h` for help, I finally got the flag correctly:

![Correct Method Flag](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/1895c0ce-f159-43a7-b0fd-0d9c67270409)

---

Stay tuned for more updates as I continue to explore and complete additional PicoCTF challenges!



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
