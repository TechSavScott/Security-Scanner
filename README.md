# Security-Scanner
In this project, I'm building an AI Powered Vulnerability Scanner for Python.
[README.md](https://github.com/user-attachments/files/29429489/README.md)


# AI Security Scanner for Python

**Project Link:** [View Project](http://nextwork.ai/projects/ai-security-audit)

**Author:** Scotty  
**Email:** scottjadon@gmail.com

---


---

## Introducing Today's Project!

In this project, I'm going to be building an AI Powered Vulnerability Scanner for Python. This will help me learn the advantages of utilizing AI along with how to code & configure. I'm interested in this project because it will serve as my first guide for future cybersecurity related task.

### Key tools and concepts

Tools I used were Cursor, Python, and Gemini AI. Key concepts I learnt included installing python, granting scipting access, engineering a scanner, and connecting an AI sourcer to that scanner. The most important skill was being able to understand the coding that went into this project and documenting it.

### Challenges and wins

This project took me approximately 1 day. The most challenging part was fixing error codes. It was most rewarding to inevitably see the outcome of the final test to know the tool works properly.

### Why I did this project

I did this project today to showcase my growing understanding of coding and ability to implement cybersecurity realted tools & measures. This project met my goals by being able to successfully scan vulnerabilities in Python files.

---

## Connecting to Gemini API

In this step, I'm setting up the Gemini API connection. This involves creating a python enviorment, obtaining & setting up an enviorment with an AI API Key, and testing connection to Gemini.

![Image](http://nextwork.ai/thrilled_azure_noble_elephant/uploads/ai-security-audit_sec2c3d4)

I verified the connection by running the entry command "python scanner.py"
Gemini responded with "Hello Security Scanner!", which indicates that Gemini API is connected and properly responding. 

![Image](http://nextwork.ai/thrilled_azure_noble_elephant/uploads/ai-security-audit_sec4e5f6)

My scanner.py file works by resolving any prompted issues with an Gemini source AI responses. When I ran it, Gemini identified that the password "admin123" was weak and insufficient to be used as a secure and reliable password. 

---

## Building the Vulnerability Scanner

In this step, I'm putting the scanner to the test by putting it up against vulnerable code to gaugeit's accuracy, a detailed security prompt to gauge it's attnetion to detail, and a test on it's detection of SQL injections, hardcodede secrets, and weak passwords. 

![Image](http://nextwork.ai/thrilled_azure_noble_elephant/uploads/ai-security-audit_sec7h8i9)

The vulnerabilities Gemini detected was an SQL Injection. The security prompt I crafted asked for... This structured output helps you get consistent & actionable output instead of vague responses.

---

## Adding Severity Ratings

In this step, I'm adding severity ratings, (CRITICAL, HIGH, MEDIUM, LOW), which will tell users the severity of the detected threat. I'm also installing colorama to assist in telling the difference visually.

![Image](http://nextwork.ai/thrilled_azure_noble_elephant/uploads/ai-security-audit_sec0k1l2)

I updated the security prompt to include colors to make severity levels stand out. The add_colors_to_output function works by taking text as input, adds color codes to severity levels, and returns the colorized text. This keeps your code organized and makes it easier to test and maintain. For example, when I see CRITICAL in red, it tells me theres an exploitation that needs immediate attention.

---

## Scanning Real Python Files



![Image](http://nextwork.ai/thrilled_azure_noble_elephant/uploads/ai-security-audit_sec3n4o5)

I scanned vulnerable.py by running files with vulnerabilities. The vulnerabilities detected were Hardcoded Credentials (HIGH), SQL Injection (CRITICAL), Weak Hashing Algorithim (HIGH), Common Injection (CRITICAL),

---

## Wrap-up

---

---
