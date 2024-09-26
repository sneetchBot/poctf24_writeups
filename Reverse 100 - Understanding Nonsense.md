## UWSPpoctf2024- Understanding Nonsense

:::info
:bulb: This is a writeup for the 'Understanding Nonense' challenge in poctf.
:::

### :eight_spoked_asterisk: The Challenge

Oh, boy... Only Wave 2 and I'm already exhausted. Whatever the issue, I just can't be bothered to finish putting this challenge together. Here, this what I have so far. Started working on the decode function and gave up. You go ahead and do the rest and the flag is yours! And if Prof. Johnson asks, tell him this was really well done or I'll get in trouble.

Right Click, Save As... [Reverse100-3](https://pointeroverflowctf.com/static/Reverse100-3)
Right Click, Save As... [Reverse100-3 Source Code](https://pointeroverflowctf.com/static/Reverse100-3.c)

### :mag_right: Solution
I actually didn't end up looking at the Reverse100-3 file since the problem was solvable just by looking at the source code

Looking inside the main function we see: 

```
int main() {
    unsigned char encoded_flag[] = { 0x8e, 0x79, 0xa9, 0x9c, 0xac, 0xd5, 0xc5, 0xc7, 0x91, 0x7a, 0xa5, 0x8a, 0xb8, 0x8d, 0xc6, 0x81, 0x55, 0x83, 0xa5, 0x59, 0x7b, 0xb9, 0x87, 0xb8, 0x51, 0x69, 0x7b, 0x58, 0xbb, 0x8b, 0xcd};

    unsigned int seed = 88974713;
    int length = sizeof(encoded_flag);

    printf("Encoded flag: ");
    print_flag_hex(encoded_flag, length, 0);

    // Reverse the modifications 10 times (finish this!)
    printf("\nDecode function not added yet!");

    printf("\nDecoded flag (plaintext in hex): ");
    print_flag_hex(encoded_flag, length, 0);  // Print final decoded flag in hex

    return 0;
}
```

Looking at the function declarations above, I saw a function called reverse_modify_flag which reversed the modification of the flag bytes based on the seed. The comment in main() seems to indicate that this function must be called 10 times. I added the following code below the comment to reverse modification 10 times and ran the file.
    
    for(int i = 0; i < 10; i++){
        reverse_modify_flag(encoded_flag, seed);
    }
    
I got 706f6374667b757773705f627233763137795f31355f3768335f353075317d which is the flag in Hex
### :triangular_flag_on_post: The Flag!!

Translating with CyberChef 
:::spoiler
poctf{uwsp_br3v17y_15_7h3_50u1}
:::
        