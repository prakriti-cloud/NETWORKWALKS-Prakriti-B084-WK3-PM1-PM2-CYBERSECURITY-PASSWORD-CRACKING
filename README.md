**Objectives**  
To recover the forgotten password of an encrypted PDF file (128-bit RC4 encryption) by extracting its cryptographic hash ($pdf$...) and running a dictionary attack using a password recovery tool.

**Problems Faced**  
I chose the wrong locked file to crack password of. While I should have chosen My Locked PDF2, I input My Locked PDF1 instead. The password for the PDF1 had already been cracked and the hash was also created. Therefore, I got access denied error.
However, that was fixed quickly after I input My Locked PDF2.

**Cracked Password**  
<img width="439" height="447" alt="Screenshot 2026-11-20 203817" src="https://github.com/user-attachments/assets/eee01cee-ffae-41ce-be3f-5a916d0613e4" />  

**What I Learned**  
- A dictionary attack requires a .txt file of plaintext candidate passwords (one per line) rather than the hash file itself.  
- Small, generic wordlists only catch the most common passwords; recovering stronger or customized passwords requires a larger or more targeted wordlist.
- Browser-based cracking tools process passwords at a slower rate (around 10 passwords per second in this test), making smaller, targeted wordlists much more practical than massive files.

**Conclusion**  
While the hash extraction and dictionary attack workflow were executed properly, the PDF remained locked because the password was not present in the basic 100-word list. Successfully recovering the password requires supplying a larger or custom-tailored wordlist containing likely password variations.
