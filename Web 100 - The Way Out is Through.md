## UWSPpoctf2024- The Way Out is Through

> [!NOTE]
> This is a writeup for the 'The Way Out is Through' challenge in poctf.

### :eight_spoked_asterisk: The Challenge

The first Web challenge of the contest and I am so excited to reveal this one! In this challenge you'll run through a simulated web-based cybersecurity training course a la the DoD Cyber Exchange Awareness Challenge. There's just one problem... The cybersecurity training is... Vulnerable??! Oh, the irony! Can YOU handle the HACK OF THE CENTURY??? Head here to find out!
https://nvstgt.com/TTiOT/index.html

### :mag_right: Breakdown

<p>
Clicking on the instance link, we are redirected to a website displaying a Not Found error.
</p>

![Screenshot]([https://hackmd.io/_uploads/r132sfGC0.png](https://github.com/sneetchBot/poctf24_writeups/blob/442463993c9758a0f28acabf5175264fb37ffc95/pictures/upload_c38e8954d5123144ed51c9a0cd384381.png))


<p>
I wasn't seeing anything standout so I decided to view source where I found something interesting in the script tags.
</p>

### :mag_right: The code enclosed in the script tags

<p>
    
    <script>
        let part_1 = [112, 111, 99, 116].map(x => String.fromCharCode(x)).join('');
        let part_2 = atob("Znt1d3NwXw==");
        let part_3 = "document.cookie";
        let part_4 = "XzdydTdoXw==";
        let part_5_hex = [0x31, 0x35, 0x5f, 0x30, 0x75, 0x37, 0x5f, 0x37, 0x68, 0x33, 0x72, 0x33, 0x7d];

        console.log("The Tooth is Over There.");
        document.cookie = "\u0037\u0068\u0033";
    </script>

</p>

### :mag_right: Solution
To solve parts 1 and 2, I copied both lines into a js web editor and printed into the console. Part 3 refered to the document.cookie variable. When coverted from hex, the variable becomes 7h3 which is the same as the value of the cookie when viewed in inspect element. For parts 4 and 5, I coverted from Base64 and Hex respectively. Combining all 5 parts, I got the flag.

### :triangular_flag_on_post: The Flag!!
<details>
    <summary>Running the shell command, we get the flag</summary>
    poctf{uwsp_7h3_7ru7h_15_0u7_7h3r3}

</details>
