# Security & Analysis Presentations

## Overview
This repository contains two PowerPoint presentations that cover:
1. **Software Code & Threat Analysis**  
   An in-depth look at common static-analysis tools, known vulnerable libraries/frameworks, and practical mitigation measures.
2. **Secure Data Storage and Encryption using GnuPG**  
   A guide to setting up secure data storage with MySQL and implementing GPG encryption keys for protecting sensitive information.

Each slide deck is designed for developers, security professionals, and IT students to gain practical knowledge on discovering software weaknesses, addressing them, and securely storing/encrypting data.

---

## Contents
- **Presentation Files**
  - `Software Code & Threat Analysis.pptx`  
    Explores tools, libraries, CVEs, and mitigation strategies for:
    - Flawfinder  
    - ImageMagick v7.1.0-27  
    - FFmpeg v4.4.3  
    - OWASP Dependency-Check  
    - Apache Struts v2.2.3.1  
    - OpenSSL v1.0.1 (including CVE-2022-28463)
  - `Secure Data Storage and Encryption using GnuPG.pptx`  
    Covers:
    - Introduction to databases and MySQL (creating databases, tables, and users)  
    - GPG key generation and management (public/private key export, passphrase protection)  
    - Encryption & decryption workflows to safeguard backups, files, and communication  

- **README.md**  
  This file, which explains the purpose, structure, and usage instructions for the repository.

---

## Slide Deck Breakdowns

### 1. Software Code & Threat Analysis
1. **Title Slide**  
   - “Software Code & Threat Analysis Presentation” – Objectives and scope.

2. **Flawfinder**  
   - Overview of Flawfinder for scanning C/C++ source code against CWE listings.

3. **ImageMagick v7.1.0-27**  
   - History of ImageMagick (October 2021 release) and associated security risks when processing untrusted images.

4. **Detail/Discover Software Threats**  
   - General guidance on identifying weaknesses in software dependencies and image libraries.

5. **CVE-2022-28463 Mitigation**  
   - Explanation of the ImageMagick-related vulnerability CVE-2022-28463 and recommended patch/workaround steps.

6. **FFmpeg v4.4.3**  
   - Overview of FFmpeg 4.4.3 (released August 26, 2021), typical use cases, and multimedia processing vulnerabilities.

7. **Threat Discovery for FFmpeg**  
   - Spotting unsafe library usage, untrusted codecs, and malicious media streams.

8. **FFmpeg Mitigations**  
   - Best practices: updating to a secure FFmpeg version, sandboxing, and safe configuration.

9. **OWASP Dependency-Check**  
   - Introduction to OWASP Dependency-Check as a software composition analysis (SCA) tool for Java, .NET, Ruby, Python, and Node.js.

10. **Apache Struts v2.2.3.1**  
    - Historical context (released 2011), common exploit vectors, and notable security incidents.

11. **Threat Discovery in Struts**  
    - Auditing Struts-based applications, identifying outdated components, and risk assessment.

12. **Struts Mitigations**  
    - Upgrading to secure Struts versions, applying vendor patches, and using runtime protections (e.g., WAF rules).

13. **OpenSSL v1.0.1**  
    - Overview (released 2012), significant vulnerabilities (e.g., Heartbleed), and cryptography-related risks.

14. **Threat Discovery in OpenSSL**  
    - Identifying insecure API usage, weak cipher configurations, and out-of-date libraries.

15. **OpenSSL Mitigations**  
    - Best practices: updating OpenSSL, enforcing strong cipher suites, and regular cryptographic audits.

---

### 2. Secure Data Storage and Encryption using GnuPG
1. **Title Slide & Group Credits**  
   - “Secure Data Storage and Encryption using GnuPG”  
   - Contributors: Bhargava Reddy Kikkura, Bharath Kumar Uppala, Hari Kiran Gaddam, Bharath Viswa Teja, Vidya Charan Maddala, Rajaabinandhan Periyagoundanoor Gopa.

2. **Introduction to Database & MySQL**  
   - Definition of a database.  
   - Overview of MySQL as an open-source RDBMS (speed, reliability, ease of use).

3. **Logging into MySQL & Creating a Database**  
   - Steps to log in as `root`.  
   - Command examples to create a new database.

4. **Creating Tables in the Database**  
   - SQL statements for defining tables (columns, data types, primary keys).

5. **Inserting Data**  
   - `INSERT` commands demonstrating how to populate tables with sample records.

6. **Creating a User for the Database**  
   - SQL commands to create a dedicated MySQL user and grant appropriate privileges.

7. **GPG Encryption Keys Overview**  
   - Importance of GPG for private digital communication: public/private key pairs, digital signatures, encrypted email, and secure file sharing.

8. **Setting up GPG**  
   - Installation and configuration steps.  
   - Choosing key type and key size, entering user data, passphrase creation.

9. **Exporting Keys to ASCII Files**  
   - Command to export the public key in ASCII-armored format:  
     ```bash
     gpg --export --armor > public_key.asc
     ```  
   - Command to list and export the secret (private) key securely.

10. **Encryption & Decryption Implementation**  
    - Role of encryption: protecting database backups, files, and preventing unauthorized access.  
    - Role of decryption: allowing only authorized users (with correct private key/passphrase) to read protected data.  
    - Example GPG commands for encrypting a file:  
      ```bash
      gpg --encrypt --recipient <recipient-email> <file-to-encrypt>
      ```  
      And for decrypting:  
      ```bash
      gpg --decrypt <encrypted-file>
      ```

11. **Use Cases & Best Practices**  
    - Encrypting MySQL backups before archiving or transferring off-site.  
    - Secure file sharing workflows:  
      - Generating a new keypair per user.  
      - Keeping private keys offline.  
      - Rotating keys periodically.  

---

## How to View the Slide Decks
1. **Clone or Download**  
   ```bash
   git clone https://github.com/<your-username>/<repository-name>.git
   cd <repository-name>
