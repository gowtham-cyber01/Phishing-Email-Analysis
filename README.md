Phishing Email Analysis

- This project analyzes a real-world phishing email sample to identify common phishing traits and highlight red flags based on technical and content inspection.

Sample Email: `sample_email.txt`

A full raw phishing email with headers and body is saved in `sample_email.txt`.

---

## 🧪 Step-by-Step Analysis

### 1. **Sender Email Spoofing**
- **From:** `MBran@aol.com`
- **Return-Path:** `<MBran@aol.com>`
- Despite appearing to come from AOL, there's no verification of authenticity (e.g., no SPF/DKIM/DMARC info). This is commonly used in spoofing attacks.

---

### 2. **Header Discrepancies**
- Headers reveal a long chain of relays.
- The email originated from `imo14.mx.aol.com`, but the sender is not validated.
- No SPF, DKIM, or DMARC records were present in the headers.
- The use of `Received:` headers shows multiple hops that may be used to mask the original source.

👉 **Tool used:** [Google Admin Toolbox - Message Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/)

---

### 3. **Suspicious Links**
Several links are listed in the email that:
- Use free hosting sites like `freeyellow.com`, often abused in scams.
- Contain suspicious tracking codes and promotion for making money.
- The visible text does not always match the URL (common phishing technique).

---

### 4. **Urgent or Manipulative Language**
- Phrases like:
  - “*You’ll definitely be hearing from me again soon!*”
  - “*Reach up to 3 Million… FREE*”
  - “*Earn big income… JUST BIG WEEKLY CHECKS*”
- These push urgency, opportunity, and FOMO — all classic signs of phishing.

---

### 5. **Mismatched URLs**
- Example:  
  - **Text:** "A HREF=..."  
  - **Actual URL:** `http://www.freeyellow.com/members2/drivevehicle/index.html`
- The `A HREF` tag was malformed and hidden, another tactic used to deceive recipients.

---

### 6. **Spelling & Grammar Errors**
- Words like "**definately**" instead of "definitely".
- Overuse of **capitalization**, inconsistent punctuation.
- Poor formatting and sentence structure throughout.

---

## 🧾 Summary: Phishing Traits Identified

| Trait | Present |
|-------|---------|
| Sender spoofing | ✅ |
| Missing SPF/DKIM/DMARC | ✅ |
| Suspicious/mismatched URLs | ✅ |
| Urgent/scam language | ✅ |
| Poor grammar/spelling | ✅ |
| Malicious intent (chain letter scheme) | ✅ |
| Unverified sender identity | ✅ |

---

## ✅ Conclusion

This email exhibits **multiple red flags** of phishing, including spoofed sender identity, suspicious links, manipulative language, and poor formatting. It is a textbook example of spam and phishing scams meant to trick users into spreading a chain mail ad disguised as a "business opportunity."

---

## 📁 Files Included
- `sample_email.txt`: Raw phishing email with full headers and body
- `README.md`: This analysis
