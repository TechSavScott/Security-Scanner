## ***Python Vulnerability Scanner***

**Author:** Jadon Scott  
**Date:** 06/27/26

---

# **Project Overview**

### **Project Summary**

In this project, I'm going to be building an AI Powered Vulnerability Scanner for Python. This will help me learn the advantages of utilizing AI along with how to code & configure. I'm interested in walking through this project because it will serve as my first guide for future cybersecurity related tasks.

**Initial Questioning**

* What is the project called? \- Python Vulnerability Scanner

* What was the primary objective? \- To engineer a python terminal scanner capable of detecting vulnerabilities within a file.

* Why did you choose this project? \- I did this project to showcase my growing understanding of coding and ability to implement cybersecurity related tools & measures. 





---

# **Requirements**

### **Business Requirements**

* What did the user or client need? \- Google Gemini API Key, Cursor, and Python.  
* What constraints existed? \- No constraints existed.

### **Technical Requirements**

* Operating system \- Windows 11  
* Network requirements \- Stable Connection  
* Software dependencies \- Cursor

---

# **Project Scope**

**Questions to Answer**

* What features were included? \- A feature in which vulnerabilities and their types are graded & color coded based on threat level.  
* What assumptions were made? \- That the project would take days to complete.  
* What limitations existed? \- No limitations existed. 

---

# **Pre \- Download Requirements & Configurations**

- Download Latest [Python 3](https://www.python.org/downloads/release/python-3146/)  
- Download Terminal Software “[Cursor](https://cursor.com/download)”  
- Open your settings \> Type “For Developers” in Settings \> Scroll down & extend “PowerShell” under Terminal \> Switch on “Change execution policy to allow local PowerShell scripts to run without signing. Require signing for remove scripts”.

---

# Phase \#1 \- Connecting Gemini API 

Start by setting up your project folder and opening it in your text editor.

* Open **Cursor**.

Create a new folder on your Desktop called security-scanner.

In your Cursor Editor Window, click “Open Project” and select the security scanner.

* Select security-scanner.  
* Click **Open Folder**.

Now, before installing packages, let's create a virtual environment to keep the project's dependencies separated. First, you need to open a terminal window in Cursor to run commands.

* In Cursor, click **Terminal** → **New Terminal** from the top men

First, check if Python is installed on your machine.

* Type this command in the terminal and press **Enter**. { *python \--version* }  
* You should get a response back similar to something like “*Python* \**Downloaded Version*\*” 

Now that we’re set, let's create a virtual environment.

* In your terminal, type this command and press **Enter**. { *python \-m venv venv* }

Activate the virtual environment.

* In your terminal, type this command and press **Enter**. { *venv\\Scripts\\activate* }  
* You should see (venv) appear at the beginning of your terminal prompt. This tells us your virtual environment is active.

Now you’ll install the SDK that allows Python to talk to Gemini.

* In your terminal, type this command and press **Enter**. { *pip install google-generativeai* }  
* This may take a minute, but when complete, you should get an output response of “*Successfully installed google-generativeai*”

Before writing code, you need to install a package to securely manage your API key. Instead of hardcoding your key directly in your code, you'll use environment variables.

* In your terminal, type this command and press **Enter**. { *pip install python-dotenv* }

Your packages are installed. Now let's create your (.env) file with a placeholder. You'll add your actual API key to this file in just a moment.

* In Cursor, create a new file in the left hand space under (venv) called (.env) within the security scanner folder. When finished, click “file” in the top left corner and click “save”.

Now that your environment is set up, let's get your API key from Google AI Studio.

* Open your web browser n’ go to [Google’s AI Studio](https://aistudio.google.com/api-keys?project=gen-lang-client-0478062455), sign in or make an account, and your dashboard should look like the photo below.  
  ![][image1]  
<img width="1906" height="894" alt="re - api key dashbaord" src="https://github.com/user-attachments/assets/04db883f-7535-4caf-aa69-f4d59b2dbbd2" /> (re \- api key dashboard screenshot)  

* Above your profile picture n’ email in the bottom right, click the key symbol.  
    
* Once in, your dashboard should look like the image below. Click “Create API Key” in the top right corner.  
  ![][image2]  

<img width="1905" height="901" alt="api key dashboard" src="https://github.com/user-attachments/assets/a9d7bde4-85fc-452d-8f99-e1f325cdb962" /> (api key dashboard screenshot)

A dialog will appear to create your API key.

* In the name field, enter My API Key (you can name this whatever you want).  
* Click on the **Choose an imported project** dropdown.  
* Select **Create project**.  
* In the project name field, enter My New Project (you can call it whatever you want).  
* Click **Create project**.  
* Click **Create key**.  
* Click the **Copy** icon next to your key to copy it.

Now your API key is set up & ready to go.

Now add your actual API key to the .env file you created earlier.

* Go back to Cursor.  
* Open your .env file and paste the following text seen below along with your key in the space above the terminal. 

GOOGLE\_API\_KEY=\*your\_key\_here\*

* When finished save your work.

Now, it’s time to create the main script file.

* In Cursor, create a new file under (.env) called (scanner.py) and add the following code meant to test Gemini’s connectivity.   
  ![][image3]  
<img width="702" height="633" alt="CodeSet #0" src="https://github.com/user-attachments/assets/53c9a746-49fa-4f7c-82c3-971ee6d76a19" /> 
(codeset \#0 screenshot)  
* When finished save your work.

* In your terminal, type this command and press **Enter**. { python scanner.py }  
* The correct response output should say “Hello, security scanner\!” or something similar.

![][image4]

<img width="1919" height="1030" alt="ResponsiveScanner" src="https://github.com/user-attachments/assets/ee2df2cb-3f66-40c8-a792-6604a1e76463" /> (responsive scanner screenshot)

* When you run python scanner.py, Python executes your code line by line which loads your API key from .env, connecting to Gemini's servers, sending the users prompt, and printing the response via the terminal.

Now that the connection between the key and Gemini is functioning it’s time to test with a security-focused prompt to see how Gemini responds.

* In your (scanner.py) tab, find the section between \# YOUR CODE GOES BELOW HERE and \# YOUR CODE GOES ABOVE HERE.

* Replace everything in that section with the following code below:

![][image5]

<img width="513" height="270" alt="CodeSet #1" src="https://github.com/user-attachments/assets/dbe1da59-5112-4176-8e14-ea76b8b726e4" /> (codeset \#1 screenshot)

* When finished save your work.  
* In your terminal, type this command and press **Enter**. { *python scanner.py* }  
* The correct response output should be Gemini identifying the hardcoded password as a security vulnerability while explaining why storing passwords directly in a codeset is dangerous.

![][image6]

<img width="1919" height="1078" alt="ConnectedToGemini" src="https://github.com/user-attachments/assets/18edc351-642b-4072-9b17-497e9ffcd503" /> (connected to gemini screenshot)

---

#    Phase \#2 \- Building a Scanner

Now is time to create some intentionally vulnerable code to test your scanner. This’ll help verify Gemini can identify real security issues like hardcoded secrets.

* In your (scanner.py) tab, add these vulnerable code examples after the model initialization seen below. (right before the \# YOUR CODE GOES BELOW HERE section):

![][image7]

<img width="560" height="632" alt="CodeSet #2" src="https://github.com/user-attachments/assets/7e12953d-e205-44f7-8821-dd5bfb3490b3" /> (codeset \#2 screenshot)

Create a detailed prompt that tells Gemini exactly how to analyze code for security vulnerabilities.

* In your (scanner.py) tab, add this security prompt above the YOUR CODE section (after the model initialization):

![][image8]

<img width="533" height="316" alt="CodeSet #3" src="https://github.com/user-attachments/assets/85d87d54-d074-44c5-becd-a1d27171e724" /> (codeset \#3 screenshot)

 Now test the scanner against your vulnerable code examples.

* In your (scanner.py) tab, update the YOUR CODE section with the testing code seen below:![][image9]  
  <img width="653" height="547" alt="CodeSet #4" src="https://github.com/user-attachments/assets/065775bd-90bd-43ac-b119-0c0763cee410" /> (codeset \#4 screenshot)  
* When finished save your work.  
* In your terminal, type this command and press **Enter**. { *python scanner.py* }

You should get a response of Gemini identifying vulnerabilities in each code example; see example photo below:

![][image10]

 <img width="1917" height="1030" alt="ColorCodedMagic" src="https://github.com/user-attachments/assets/449f1017-8977-4fd9-98f4-dde1cbdc238c" /> (color coded magic screenshot)

---

#    Phase \#3 \- Add Color & Severity Level

First, it’s important you add colors to make the output more readable.

* In your terminal, type this command and press **Enter**. { *pip install colorama* }  
* You should see "Successfully installed colorama" in your terminal.


Now that colors are installed it’s time to modify the prompt Gemini can rate the severity of each vulnerability.

* Update your security prompt by replacing it with the following code seen below:  
  ![][image11]  
 <img width="478" height="370" alt="CodeSet #5" src="https://github.com/user-attachments/assets/c7f8272d-e295-487f-a5d5-c2b0be854210" /> (codeset \#5 screenshot)  
* When finished save your work.

Next, we’ll add colors to make severity levels stand out.

* At the top of your (scanner.py) tab, add the following colorama import below:

![][image12]

  <img width="331" height="106" alt="CodeSet #6" src="https://github.com/user-attachments/assets/154814ab-4d74-485e-8fbc-06ffaf0fc396" /> (codeset \#6 screenshot)

Just above the YOUR CODE section, add the following code below:![][image13]

<img width="865" height="185" alt="CodeSet #7" src="https://github.com/user-attachments/assets/a56078bf-41b2-4c12-ae56-daf0a1d1fd88" /> (codeset \#7 screenshot)

Finally, update your YOUR CODE section to use colors with the following code below:

![][image14]

<img width="665" height="603" alt="CodeSet #8" src="https://github.com/user-attachments/assets/1eab0837-08e5-4d8e-90fe-66d5d5cfe6bb" /> (codeset \#8 screenshot)

* When finished save your work.  
* In your terminal, type this command and press **Enter**. { *python scanner.py* }

You should now see a security report with colored severity levels \- red for critical, yellow for high, blue for medium, and green for low\!

![][image15]

<img width="1919" height="1032" alt="LiveFileTesting" src="https://github.com/user-attachments/assets/0324635b-4c50-4177-b071-7cf8aded9b0a" />(live file testing screenshot)

