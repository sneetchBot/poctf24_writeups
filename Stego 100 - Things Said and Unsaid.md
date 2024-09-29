## UWSPpoctf2024- Things Said and Unsaid

> [!NOTE]
> This is a writeup for the 'Things Said and Unsaid' challenge in poctf.

### :eight_spoked_asterisk: The Challenge

![Challege-Image](pictures/Stego100-3.jpeg)

### :mag_right: Solution
This is a pretty simple stegonography challenge. I obtained the flag through the following steps:
1. Download the image: https://pointeroverflowctf.com/static/Stego100-3.jpeg
2. Put the image through a hexeditor and at the end of the hexedit file you will see the following text: probably_improbable alternatively run the Strings command on the jpeg to get the same results
3. Extract the image using the command binwalk -e Stego100-3.jpeg
4. Cd into the extracted file '_Stego100-3.jpeg.extracted' to find a zip file
5. Using an unzipper (e.g. 7z x) unzip the file using the password: probably_improbable to obtain the flag!

### :triangular_flag_on_post: The Flag!!
Plugging into the flag format, we get poctf{uwsp_w3_4r3_such_57uff}
        
