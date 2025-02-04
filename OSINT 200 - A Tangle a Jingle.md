## UWSPpoctf2024- A Tangle a Jingle

> [!NOTE]
> This is a writeup for the 'A Tangle a Jingle' challenge in poctf.

### :eight_spoked_asterisk: The Challenge

Sometimes I like to try to find the exact location where a photo was taken. A little OSINT exercise I do sometimes to keep my skills sharp. This image was posted to a social media platform last year. I was able to find where it was taken, and if you can too then you will see that there is a business just out of frame, across the street from the building on the corner, to the left of the bollards. The phone number on their sign is the password to the archive (no spaces or special characters.)
![Street in the morning with shopfronts to the left](pictures/upload_935153b42d772c196351a146de935a62.png)

### :mag_right: Solution
I couldn't actually save the image so I dispayed a screenshot of it. Doing a Google Image Search, I found a [Reddit post](https://www.reddit.com/r/pics/comments/1avt0nk/some_sky_pictures_from_my_paper_round/?rdt=50323) from 7 months ago with the exact image. Reddit reduces image quality unless you have an account so I created an account. The improved image quality helped us read the phone number on the red storefront.
Looking up the phone number, we found the business address in the UK. From Google Street View, the phone number on the shopfront to the left is:
![Telephone# on left shopfront](https://github.com/sneetchBot/poctf24_writeups/blob/812992c2ccfab92f546fd677425126bab78c7664/pictures/upload_d52678cc6ba40a13156320ccb9f61a2d.png)

### :triangular_flag_on_post: The Flag!!
<details> 
        <summary>Using the phone # as the password to the zip file we get</summary> 
         poctf{uwsp_1_h4v3_4_dr34m}
</details>    
        
