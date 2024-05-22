**Python Wrangling**

First, I created a new directory in the Webshell called `Python Wrangling`. Then, I downloaded the files from the challenge window, similar to how I did in the first challenge.

After downloading all three files, the challenge directory looked like this:

<img width="442" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/f32c94a2-8293-40bb-9a0e-569b624b0860">

Unsure of where to start, I began by opening each file using the `cat` command. The two text files contained the following:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/99539815-a6f1-4019-bcac-e78e372bdb6d">

It appeared that `pw.txt` contained a password and `flag.txt.en` contained something encrypted. Next, I opened the `ende.py` file, which initially seemed overwhelming:

1- <img width="254" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/99bca11e-dc09-4381-a05d-03f2c56a1a50">
2- <img width="278" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/f844edff-1827-4129-b7ed-a1847a5d2737">

However, by reading between the lines, I understood its purpose. The first line, `import sys`, indicated the use of the sys library, often for command line interaction. The help message provided insight into how to use the script:

<img width="430" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/4fc4cd3c-c049-41c4-8f05-f8bb22da71fe">

The `help_msg` argument suggested that we need to decrypt a file named `pole.txt`, which was not present. After reviewing the script again, I realized it had four conditions using `if`.

The first condition checked the number of arguments in the command line, requiring 3 or 4 arguments:

<img width="322" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/8c3180bd-c027-48db-bc1f-57b591c28743">

The second condition used `-e` for encryption, as indicated in the help message:

<img width="254" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/760551e7-1af2-4319-a0db-836c0fc1239a">

The third condition used `-d` for decryption, which matched the help message:

<img width="455" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/05b9d611-37cb-42a3-9edc-7bee0f1560f9">

The last condition was for displaying the help message, which was already clear.

At this point, I understood that the script could encrypt and decrypt files. I decided to try decrypting `flag.txt.en` using the following command:

```bash
python ende.py -d flag.txt.en 
```

After executing the command, the program prompted me for a password. I used the password from pw.txt:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/94cca9c9-a73d-4be1-a0e4-e0364624de8e">

This revealed the flag. I was pleasantly surprised it worked:
	
<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/52ef9b2e-abfd-4a54-976e-cca4709f60c3">
