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

