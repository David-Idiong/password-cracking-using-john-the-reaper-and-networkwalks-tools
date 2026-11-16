# password-cracking-using-john-the-reaper-and-networkwalks-tools

<img width="955" height="473" alt="jh1" src="https://github.com/user-attachments/assets/ec1a66d9-2e83-404c-a5cf-f28118c5cac4" />


**Step 1: Open the PDF hash extractor**
Navigated to OnlineHashCrack's PDF Hash Extractor tool, which converts an encrypted PDF into the hash format used by pdf2john / pdf2hashcat.

<img width="959" height="503" alt="jh2" src="https://github.com/user-attachments/assets/9b7e8552-ad7b-4081-a992-3bc32082a12f" />




**Step 2: Select the locked PDF**
Chose the location of the password-protected file (My Locked PDF1.pdf) from my local folder.


<img width="959" height="469" alt="jh3" src="https://github.com/user-attachments/assets/f608b8d8-0bc0-411c-96a0-99547bf2b5bf" />




**Step 3: Extract the hash**
Uploaded the file and let the tool process it. Extraction completed and returned the PDF's hash value in $pdf$... format.



<img width="703" height="350" alt="jh4" src="https://github.com/user-attachments/assets/e0a49996-6647-4a24-ace9-83f232292ba4" />

**Step 4: Save the hash**
Copied the extracted hash into Notepad and saved it as hash1.txt so it could be easily identified and loaded later.



<img width="957" height="502" alt="jh5" src="https://github.com/user-attachments/assets/7e9daba5-36dd-40ef-917e-45e2fdaf1f66" />


**Step 5: Configure John the Ripper (Johnny)**
Opened Johnny, the GUI for John the Ripper, and pointed it to the John the Ripper executable to confirm the installation was detected and working correctly.



<img width="959" height="482" alt="jh6" src="https://github.com/user-attachments/assets/e17896c8-8ac5-4856-8b83-9177b1652fb3" />


**Step 6: Load the hash file**
Used "Open password file" in Johnny and navigated to the saved hash1.txt file containing the extracted PDF hash.



<img width="959" height="507" alt="jh7" src="https://github.com/user-attachments/assets/c84f637c-3487-42f4-bbff-347ffd022308" />


**Step 7: Run the attack**
Started the attack in Johnny. John the Ripper processed the hash and successfully cracked the password, shown as 100% (1/1: 1 cracked, 0 left).


<img width="518" height="273" alt="jh8" src="https://github.com/user-attachments/assets/675f5c6a-fa55-4922-b706-d4c7e2990f67" />


**Step 8: Verify - wrong password first**
Before entering the cracked password, I deliberately typed an incorrect one into the PDF's password prompt to confirm the file was genuinely locked and I didn't already know the password.



<img width="959" height="506" alt="jh9" src="https://github.com/user-attachments/assets/7fc2d1cf-41d8-4399-b455-3b6c9b59a071" />


**Step 9: Unlock the PDF**
Entered the password recovered by John the Ripper, and the PDF opened successfully - confirming the crack worked and capturing the lab's flag.




Using networkwalks tools

<img width="943" height="468" alt="nw1" src="https://github.com/user-attachments/assets/7adbf622-25fa-49b8-bd8a-17a87d6bfeff" />


**Step 1: Open the Hash Calculator tool**
Navigated to Networkwalks' own Hash Calculator (networkwalks.com/hash-calculator/), a free tool that can generate common hashes or extract a crackable hash directly from a password-protected PDF.



<img width="947" height="477" alt="nw2" src="https://github.com/user-attachments/assets/240581c4-14a3-4a33-b2fa-af62db4f91e9" />


**Step 2: Upload the locked PDF**
Switched to the PDF tab and selected "My Locked PDF1 (for NW Tools Lab WK3-PM2).pdf" to check if it's password protected and extract its hash — all parsed locally in the browser, nothing uploaded.





**Step 3: Extract the hash**
The tool confirmed the PDF is encrypted and generated a crackable hash in pdf2john / hashcat-compatible format ($pdf$...), along with the PDF's Revision, Version, and Key length details.




<img width="955" height="476" alt="nw4" src="https://github.com/user-attachments/assets/84051f37-abad-4824-af58-7e4abe6c29d2" />

**Step 4: Open the Password Cracker tool**
Moved to Networkwalks' Password Cracker (Dictionary Attack Lab), which hashes every word in a wordlist and matches it against a PDF password hash — the same concept John the Ripper uses.


<img width="956" height="436" alt="nw5" src="https://github.com/user-attachments/assets/cffa25ea-0416-4aaf-92c0-22b4046bab02" />


**Step 5: Paste the hash**
Pasted the extracted $pdf$ hash into the Password Cracker tool and kept the built-in wordlist (100 passwords) active before starting the attack.



<img width="956" height="462" alt="nw6" src="https://github.com/user-attachments/assets/8f1b032e-442f-4ed7-875f-da0e634f3503" />


**Step 6: Run the attack**
The tool tried each password in the wordlist and found a match at 91/100 attempts, cracking the password as "password1".




<img width="552" height="286" alt="nw7" src="https://github.com/user-attachments/assets/ae6f312a-75bc-490c-8f8c-60c08295ead6" />


**Step 7: Verify - wrong password first**
Before entering the cracked password, I deliberately typed an incorrect one into the PDF's password prompt to confirm the file was genuinely locked and I didn't already know the password.



<img width="959" height="503" alt="nw8" src="https://github.com/user-attachments/assets/c3051004-e102-40be-bf2a-54656f8b2dd3" />


**Step 8: Unlock the PDF and capture the flag**
Entered the cracked password ("password1"), and the PDF opened successfully — confirming the crack worked and revealing the lab's flag.



## 👤 Author

**David Idiong**

Cybersecurity Professional 

Networkwalks Internship [B084]

LinkedIn: https://www.linkedin.com/in/david-idiong-71476a326


## 📋 Project Information

**Program Name:** Cybersecurity program at Networkwalks | **Week:** 03 | **Repository:** GitHub
