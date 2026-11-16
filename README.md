<p align="center">
  <img src="screenshots/week3-banner.png" alt="Week 3 - Password Cracking" width="100%">
</p>

<h1 align="center">🔓 WEEK 3 | Password Cracking with Networkwalks Tools</h1>

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

## 🎯 Objective
To understand the mechanics of a Dictionary Attack by extracting the `$pdf$` hash from a locked PDF file and cracking it using the Networkwalks Hash Calculator and Password Cracker tools.

---

## 📝 Task 1: Crack the Locked PDF

**Target File:** `My Locked PDF1.pdf`
**Tools Used:** [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/) & [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/)

### ⚙️ Step-by-Step Execution

**Step 1: Download the Target File**
Downloaded the encrypted PDF file (`My Locked PDF1.pdf`) to the laptop from the lab portal.

**Evidence (Locked PDF Files):**
<img src="screenshots/w3-locked-files.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 2 & 3: Extract the Hash**
Opened the Networkwalks Hash Calculator and uploaded the locked PDF file to extract the hash value starting with `$pdf$...`.

**Evidence (Uploading PDF):**
<img src="screenshots/w3-pdf-upload.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Evidence (Hash Calculator Tool):**
<img src="screenshots/w3-hash-calculator.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 4 & 5: Prepare the Password Cracker**
Copied the full `$pdf$` hash and opened the Networkwalks Password Cracker in the browser. Pasted the hash into the input field and selected the built-in 100-word list.

**Evidence (Password Cracker Interface):**
<img src="screenshots/w3-cracker-start.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 6 & 7: Run the Dictionary Attack**
Started the cracking process. The tool tried different passwords from the wordlist. After trying 91 out of 100 words, it successfully found the match.

*   **Cracked Password:** `password1`

**Evidence (Dictionary Attack in Progress & Match Found):**
<img src="screenshots/w3-cracker-match.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

**Step 8 & 9: Open the PDF**
Used the cracked password (`password1`) to successfully open the locked PDF file and capture the flag.

**Evidence (Flag Captured):**
<img src="screenshots/w3-success.png" width="600" style="border: 1px solid #ccc; border-radius: 5px; box-shadow: 2px 2px 8px rgba(0,0,0,0.2);">

---

## 🔍 Key Findings & Takeaways
*   **Dictionary Attacks are Effective:** If a password is a common word (like `password1`), a dictionary attack can crack it in seconds.
*   **Hashing is One-Way:** We cannot reverse a hash, but we can generate hashes of known words and compare them to the target hash to find a match.
*   **Password Security:** This lab proves why we must use complex, long, and unpredictable passwords (or passphrases) instead of common dictionary words to prevent such attacks.

---

<div style="background-color: #f8f9fa; border-left: 6px solid #28a745; border-radius: 8px; padding: 15px; margin-bottom: 25px; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
  <h3 style="margin-top: 0; color: #218838;">✅ Lab Status: Completed</h3>
  <p style="margin-bottom: 0; color: #2c3e50;">Successfully extracted the hash and cracked the PDF password using Networkwalks tools.</p>
</div>
