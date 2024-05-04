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
