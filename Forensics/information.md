## 5. Information – Forensics – 10 Points

This challenge was a bit more challenging for me than the others. I started, as usual, by downloading the relevant file. After reading the instructions, which said "Files can always be changed in a secret way," I suspected that the file might have been altered and that I needed to figure out its correct file type. First, I tried to open the file but lacked permission. Then, I used the `file` and `stat` commands to see if it was a jpg file:

![Information 1](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/b75ded8e-be7f-4fda-ad6c-4c8daebddaa8)

The only clue from these commands was that the file was indeed a picture. At this point, I was completely lost. I tried opening the file in different ways and changing the file type based on the instructions, but to no avail. I then decided to check the hints. The first hint suggested, "look at the details of the file," indicating that the flag might be in the file’s details.

To view the file's details, I tried using the `more` and `less` commands. The `less` command did not provide any useful information, but with the `more` command, I noticed something suspicious in the file’s license line. It looked like the license resource was encoded or encrypted:

![Information 2](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/43fc5c39-885e-4c73-b832-20b25a6f43d3)

Searching for other ways to view the file’s data, I found the `exiftool` command, which shows the file’s meta-information. The license information looked the same, confirming my suspicion. My next step was to determine if it was encoded or encrypted and how to decode or decrypt it:

![Information 3](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/03978642-b62e-473d-b05b-57feffe36fa2)

I felt that the string was likely encoded, as encryption would require a more complex process to decrypt, involving finding the encryption type and key, which seemed beyond the scope of this challenge. I decided to try decoding the string with Base64, a common encoding method. Using the `base64` command, I decoded the string and found the flag! The command I used was:

```bash
echo "the string" | base64 -d
```

![information 4](https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/9d183d55-47d0-4e47-a000-2ad6357637cd)
