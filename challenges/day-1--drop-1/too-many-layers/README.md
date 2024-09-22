# Too many Layers

## Description

gkkab://bgrsktsq.vk/NWPVF

Hey there, fellow code-cracker!
Today, my brother, who’s fond of ciphers and steganography, sent me a mysterious link to a file filled with secrets! 🕵️‍♂️🗝️ He hinted that I need to use an algorithm but was delierious from all the attempts. I couldn't tell what code to use but it sounded like cAFFINE and the magical code word is “today.”

Can you help me unravel this enigma and uncover the elusive flag hidden within? Let’s put our detective hats on and decrypt this together! 🔍✨



## Solution

The first step is to decode the Affine encoded URL as the description hints to. I used decode.fr to bruteforce it. 

![](/images/Layers.png)



This reveals the URL:

```
https://shorturl.at/CDIAE
```

This URL leads to a google drive with a photo of Lord Voldemort.

![](/images/Stego.png)



When we download this file, it is a .io file. This doesn't match the what is being displayed. When I run the file command on it, we can see that it is a PNG file.

![](/images/png.png)



We can change the file type to match what we know it to be. We can use our standard PNG stego tools to see what can be found within the file. 

![](/images/zsteg.png)



In our output from zsteg, we notice a sentence that is of interest. 

![](/images/data.png)



Using this sentence and the hint in the description of the "magical code word" it made me think of the enigma and the man who solved it saving many lives, Alan Turing.



```
flag{Alan Turing}
```


