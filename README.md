# PDF Password Recovery using john the Ripper (CLI & johnny GUI)

## Project Overview
This project demonstrates password auditing and recovery on a password-protected PDF file (`My Locked PDF1.pdf`) using **John the Ripper (JTR)** via the command line Interface (CLI) and **Johnny** (the official GUI frontend for John the Ripper).

> **Disclaimer:** This project was completed strictly for educational and authorized security auditing purposes.

 ---

 ## Tools Used
 * **Operating Systems:** Windows11 & Kali Linux (Oracle VirtualBox)
 * **CLI Tool:** John the Ripper (`pdf2john` & `john`)
 * **GUI Tool:** Johnny (JTR Frontend)
 * **Web Tools:** Networkwalks Hash Calculator & Networkwalks Password Cracker

   ---

 ## Methodology & Execution

 ### Method 1: John the Ripper (CLI)
1. **Extract the PDF Hash:** 
      Used `pdf2john` to extract the password hash from the locked PDF:
      ```bash
      pdf2john My-Locked-PDF1.pdf > hash.txt
      ```
2. **Crack the Hash via Dictionary Attack:**
   Executed John the Ripper using the wordlist:
   ```bash
   john --wordlist=/usr/share/wordlists/JTR_default_password.txt hash.txt
   ```
3. **Verify Recovery Password:**
   ```bash
   john --show hash.txt
   ```

---

### Method 2: Johnny (GUI)
1. Opened **Johnny** and loaded the extracted `hash.txt` file via *Open Password File**.
2. Configured the dictionary attack using the target wordlist.
3. Started the attack and confirmed the cracked password in the results table.

   ---

   ### Method 3: Networkwalks Hash Calculator & Password Cracker
   1. **Calculate / Extract Hash:**
      opened the **Networkwalks Hash Calculator** in a web browser, uploaded/input the target file details to generate the corresponding hash.
   2.**Crack the Password:**
      Opened the **Networkwalks Password Cracker** web tool, pasted the extracted hash, and ran the cracking process to recover the plaintext password.

      ---

      ## Summary of Results
      * **Targeted File:** `My-Locked-PDF1.pdf`
      * **Recoverd Password:** `<password1>`
      * **Verification:** Successfully unlocked `My-Locked-PDF1.pdf` using the recovered password across all three methods.

