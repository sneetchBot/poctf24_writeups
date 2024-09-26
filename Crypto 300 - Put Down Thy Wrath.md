## UWSPpoctf2024- Put Down Thy Wrath

:::info
:bulb: This is a writeup for the 'Put Down Thy Wrath' challenge in poctf.
:::

### :eight_spoked_asterisk: The Challenge

In this challenge, you are given a public key and an encrypted message that was encrypted using a flawed implementation of homomorphic encryption. Your task is to analyze the encryption algorithm, identify its weaknesses, and use them to decrypt the message and reveal the flag. The provided file contains the encryption implementation, and here is the public key and the encrypted message. Good luck!

C:
79,74,3f,0f,5a,27,21,3a,36,48,64,51,64,0f,79,7e,1a,64,64,03,33,0f,64,64,57,21,27,3f,0f,2c,4a,3a,3f,24,27,3f,0f,7e,64,79,1a,64,2c

Public Key:
3233

[Homomorphic Function](https://pointeroverflowctf.com/static/Crypto300-3_homomorphic_encryption.py)

### :mag_right: Solution
The solution ended up being in the code file due to an error while posting the challenge >>

An error in the deployment of Crypto 300 - Put Down Thy Wrath causes the challenge to be much easier than intended due to the linking of a script form testing instead of the final version. 

### :triangular_flag_on_post: The Flag!!

:::spoiler
poctf{uwsp_T3mp357_4nd_7urnm01l}
:::
        