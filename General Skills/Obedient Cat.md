**Obedient Cat**

After signing up, the first challenge I encountered was "Obedient Cat."

<img width="198" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/f4f166e2-4e74-4127-afe1-2ec3ba17ea54">

I started by entering the Webshell, where I needed to enter my username and password to access the platform. To keep things organized, I created a new directory named after the challenge and navigated into it.

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/5fdfe624-d9a1-4702-a527-58a4a76611f0">

Next, I returned to the challenge description and right-clicked on the link to copy the download URL.

<img width="221" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/ef19a951-0d38-4ecd-b79f-ef894e0752c2">

In the shell, I downloaded the file using the `wget` command by pasting the copied URL:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/f32623b2-ea51-4c00-982f-27edc32e2332">

As shown in the picture, the downloaded file was named "flag" without specifying its file type. I opened the file using the `cat` command and found the flag inside:

<img width="468" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/792c05fb-162f-472c-9818-7f865d184463">


I didn't include pictures of pasting the flag back into the challenge window as it seemed unnecessary. This challenge was very straightforward and required almost no prior skills to solve. Although I didn't use the hints, it's important to feel comfortable using them when needed because the main goal is to learn.
