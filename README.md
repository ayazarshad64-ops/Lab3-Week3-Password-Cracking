<p align="center">
  <img src="screenshots/week3-banner.png" alt="Week 3 - Password Cracking" width="100%">
</p>

<h1 align="center">🔓 WEEK 3 | Password Cracking Techniques</h1>

<br>

<!-- Colorful Author & Instructor Box -->
<div style="background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%); border-radius: 12px; padding: 20px; color: white; box-shadow: 0 4px 8px rgba(0,0,0,0.3); margin-bottom: 25px;">
  <h3 style="margin-top: 0; color: #ecf0f1; border-bottom: 2px solid rgba(255,255,255,0.2); padding-bottom: 10px;">👨‍💻 Lab Details</h3>
  <p style="margin: 8px 0;"><b>Student Name:</b> Muhammad Ayaz</p>
  <p style="margin: 8px 0;"><b>Program/Batch:</b> Cyber Security | Batch B084H</p>
  <p style="margin: 8px 0;"><b>Instructor:</b> Mr. Waqas Karim (CCIE)</p>
  <p style="margin: 8px 0;"><b>Institute:</b> Network Walks</p>
</div>

---

# 📌 MODULE 1: Password Cracking with JTR (John The Ripper)

**Task:** Crack the password of an attached PDF file (`My Locked PDF1.pdf`) using **John the Ripper (JTR)** and **Johnny GUI** on a Windows PC.

### ⚙️ Step-by-Step Execution

**Step 1 & 2: Install John the Ripper & Johnny GUI**
Downloaded John the Ripper from the official Openwall website and installed the Johnny GUI. Configured the settings to point to the `john.exe` file located in the `run` folder.

**Step 3: Extract PDF Hash**
Downloaded the encrypted PDF file. Opened the online hash extractor tool (`onlinehashcrack.com`) to extract the hash from the locked PDF.

**Evidence (Hash Extractor Tool):**
<img src="screenshots/w3-jtr-hash-extractor.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 4: Save the Hash**
Copied the extracted PDF hash code, opened **Notepad**, pasted the code, and saved the file as **`hash.txt`**.

**Evidence (Saving hash.txt file):**
<img src="screenshots/w3-jtr-file-hash.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 5: Crack the Password in Johnny GUI**
Opened Johnny GUI, loaded the `hash.txt` file, and started the attack. The tool successfully cracked the password, which was displayed as `password1`.

**Evidence (Johnny GUI Password Cracked):**
<img src="screenshots/w3-jtr-johnny.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 6: Open the PDF File**
Used the cracked password (`password1`) to successfully open the first PDF file and captured the flag.

**Evidence (Flag Captured):**
<img src="screenshots/w3-jtr-success.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

<br>

---

# 📌 MODULE 2: Password Cracking with Networkwalks Tools

**Task:** Crack the password of the attached PDF file (`My Locked PDF1.pdf`) using the Networkwalks Hash Calculator and Password Cracker tools.

### ⚙️ Step-by-Step Execution

**Step 1 & 2: Extract the Hash**
Opened the Networkwalks Hash Calculator and uploaded the locked PDF file to extract the hash value starting with `$pdf$...`.

**Evidence (Uploading PDF):**
<img src="screenshots/w3-pdf-upload.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Evidence (Hash Calculator Tool):**
<img src="screenshots/w3-hash-calculator.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 3: Prepare the Password Cracker**
Copied the full `$pdf$` hash and opened the Networkwalks Password Cracker in the browser. Pasted the hash into the input field and selected the built-in 100-word list.

**Evidence (Password Cracker Interface):**
<img src="screenshots/w3-cracker-start.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 4: Run the Dictionary Attack**
Started the cracking process. The tool tried different passwords from the wordlist. After trying 91 out of 100 words, it successfully found the match.

*   **Cracked Password:** `password1`

**Evidence (Dictionary Attack in Progress & Match Found):**
<img src="screenshots/w3-cracker-match.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 5: Capture the Flag**
Used the cracked password to open the PDF and capture the flag using Networkwalks tools.

**Evidence (Flag Captured):**
<img src="screenshots/w3-success.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

---

## 🔍 Key Takeaways
*   **JTR vs Online Tools:** John the Ripper provides powerful offline cracking capabilities, while online tools like Networkwalks offer a quick, browser-based alternative for simple dictionary attacks.
*   **Hash Extraction:** Extracting the hash is the most critical step. Once the `$pdf$` hash is extracted, the original file is no longer needed for the cracking process.
*   **Weak Passwords:** The password `password1` is a classic example of a weak, dictionary-based password that can be cracked in seconds.

---

<div style="background-color: #f8f9fa; border-left: 6px solid #28a745; border-radius: 8px; padding: 15px; margin-bottom: 25px; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
  <h3 style="margin-top: 0; color: #218838;">✅ Week 3 Status: Both Modules Completed</h3>
  <p style="margin-bottom: 0; color: #2c3e50;">Successfully executed Dictionary Attacks using both John the Ripper (JTR) and Networkwalks web tools.</p>
</div>
