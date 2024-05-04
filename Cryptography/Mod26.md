**Mod26**

This challenge is in the Cryptography section and it is pretty straight forward as well:

<img width="272" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/e2ddc7fe-1633-486f-975f-f5df64dc8da6">

By reading the challenge the first bumped into my mind is one of the simplest algorithms of cipher encryption since the challenge asks wat is ROT13, and in cipher encryption, ROT stands for rotate by, which means that you can look at the A, B, C as if it was place on a wheel and each letter change counts as one ROT. With that in mind, I really didn’t want to do it manually and count 13 letters from each letter of sign so I look up on google a ROT13 decryption and got into the first option I saw.
There, I’ve copied and pasted the encrypted part from the challenge window to the ROT13 decryption website and what I got was the flag:

<img width="272" alt="image" src="https://github.com/yottam205/PicoCTF-Sloutions/assets/117525375/b313c755-0b7e-4145-92d2-eae914824d82">

From there I’ve just copied and pasted the flag into the challenge window and that was it.