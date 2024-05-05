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
