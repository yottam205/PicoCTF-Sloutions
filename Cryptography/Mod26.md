**Mod 26**

This challenge is in the Cryptography section and is quite straightforward:

<img width="272" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/e2ddc7fe-1633-486f-975f-f5df64dc8da6">

When I read the challenge, the first thing that came to mind was one of the simplest cipher algorithms, ROT13. In cryptography, ROT stands for "rotate by," meaning that each letter in the alphabet is shifted by a fixed number of positions. For ROT13, each letter is shifted by 13 positions.

Instead of manually shifting each letter, I searched for a ROT13 decryption tool online and used the first option I found. I copied and pasted the encrypted part from the challenge window into the ROT13 decryption website, which revealed the flag:

<img width="272" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/b313c755-0b7e-4145-92d2-eae914824d82">

From there, I copied and pasted the flag into the challenge window to complete it.
