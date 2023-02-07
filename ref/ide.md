---
layout: home
title: Install Python and its IDE
parent: References
nav_order: 5
py_version: 3.11.1
seo:
  type: Reference
  name: A guide for how to install Python Interpreter and use IDE/IDLE
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## General Instructions to Install Python

1. Go to <https://www.python.org/>
1. Roll over the **Downloads** link on the top blue bar. You should get a button to download the version for your operating system.
1. Be sure to choose the latest Python version that starts with **`3.`**
   - The last time these instructions were updated, the most recent version was {{page.python_version}}
   - By the time you read this, the current version may be different.
3. Double-click the downloaded file to install. **Follow all instructions.**

### Mac users NOTE
At the end of the install, click on **Install Certificates** to install a set of current SSL root certificates. ([See screenshots.](https://docs.google.com/presentation/d/1Abq0U0BFuMygqpWpsek4q_3JKRC_fbQZRLKXTA_gvhk/edit#slide=id.g110b681bc66_0_9))

Mac users: You can click _yes_ when it asks to move the installer to the Trash.

### Windows users: 
Look carefully for any option to **“add Python to PATH”** - You DO want to do this — so if a box needs to be checked, **check it**.

If you need the step-by-step instructions on how to install your very first Python interpreter on a Windows machine, then read on. 

Skip to ["How to use IDLE with files?"](#how-to-use-idle-with-files) below if you are ready to get started with IDLE.

---

## How to install the Python Interpreter on a Windows machine?

If you have other types of OS (e.g., Linux, Mac), your process can slightly differ from these instructions. Feel free to look it up online or ask us for help during the office hours.


### Step 1. Go to python.org

Open your browser and go to <https://www.python.org/download>

### Step 2. Download the latest version

Click on the button "Download Python {{page.python_version}}" - the specific version can change, so do not worry about it, as long as it is greater than 3.7.

Pressing the “Python {{page.python_version}}” button will initiate the downloading process for the python installer (python installer `!=` python interpreter).

If your browser asks you if you want to download this .exe file - choose “yes”.

If the browser asks you for the place to save this file - choose any folder, it is not important. (We suggest the "Downloads" folder)

Check that you see the process in your browser.

!['A screenshot of showing the python exe file downloading in the browser.']({{ site.baseurl }}/assets/images/ide/downloading-python.png)

Wait until the file finishes downloading - it might take a few minutes.

### Step 3. Find and run the installer

Find it on your computer or in your browser (see the previous picture) and double-click on it to run it.

You should have the result, similar to the picture below.
Click "Run".
!['A screenshot of showing the screen of running python installer.']({{ site.baseurl }}/assets/images/ide/run-installer.png)


### Step 4. IMPORTANT! 
#### Add Python to the PATH
**IMPORTANT!** If you are on a Windows system - <span style="color:red"> make sure that the last checkbox is marked!</span>

!['A screenshot of showing the checked box to add Python to PATH.']({{ site.baseurl }}/assets/images/ide/python-3.11.1-windows-click-add-python.exe_to_path.gif)


### Step 5. Install

Press the “Install Now” line.
!['A screenshot of the setup progress.']({{ site.baseurl }}/assets/images/ide/python-3-11-1-windows-install-click-install-now.gif)

Wait until the installation process is finished.


### Step 6. Celebrate

You should now see the “Setup was Successful” line as shown in the animation above. 

Congratulations! You’ve successfully done the installation. Now we learn how to check that the Python interpreter works.

If something went wrong, please seek out help during lab or office hours.

---

## How to use IDLE with files?

Open IDLE on your computer. If you have installed Python - IDLE goes with it in one package.

!['A screenshot of the menu showing IDLE.']({{ site.baseurl }}/assets/images/ide/find-menu-idle.png)


### Warning!
⚠️  **IMPORTANT**: When IDLE opens, it opens what is called a **Python Console** - you'll see **"IDLE Shell"** or **"Python Shell"** when you look at the very top of that window.
* If you are seeing `Type "help", "copyright", "credits" or "license()" for more information.` in this window, then you are in the IDLE Python Shell.
* <span style="color:red">**DO NOT** use the IDLE/Python Shell to _write_ the code for this class.</span>
* <span style="color:green">**INSTEAD** use the "New File" to open a new window when you want to write code (as explained below)</span>

Here's why:
* When you **create a new file**, your code will be saved on your computer and can be re-run easily.
* Code you type into the **IDLE Shell** is intended for quick experiments; it cannot be saved in a way that it can be re-run easily.

### Create a new Python file in IDLE

!['A screenshot of the menu showing how to create a new file using New File submenu.']({{ site.baseurl }}/assets/images/ide/new-file.png)

Use `“File” -> “New File”` to create a new file or `“File” -> “Open”` to open one that you previously created. 

Remember to **save your work** somewhere you can find it. (We recommend creating a dedicated folder for your code.)

When you are in the **file-editing window**, you can use `“Run” -> “Run Module”` to run this specific file as a _script_ and see your code in action.
!['A screenshot of the menu showing how to run a file using Run Module submenu.']({{ site.baseurl }}/assets/images/ide/run-module.png)

⚠️  <span style="color:red">If you are not seeing the top menu `"Run"`, then you are _**not**_ in the **file-editing window**.</span>


### Running a file that asks for user input

Note! If your program requires input you will need to provide it inside the Python console, which will be displaying the output of your program/script!

Python will put the cursor and wait until you give the input to it. It won’t run your program or give you any hints that it is waiting for something. Be careful with inputs!

---

## Helpful notes

### Enable line numbers
In IDLE, you can select the `"Show Line Numbers"` option from the top `"Options"` menu.
Seeing line numbers helps a lot with debugging, since Python errors report the code's line number where the error was detected.

### Force the program to stop
If you want to stop the program that behaves unexpectedly or runs for too long - just press `Ctrl+C` (`Control` and `C` at the same time) and the program will stop with the “Keyboard stopped me” Error (`KeyboardInterrupt`).

### Function prompts
If, in IDLE file mode, you write the name of a function, type an open parenthesis `(` and wait a little, you will get a help prompt that shows you how to use this function.
!['A screenshot of the IDLE file that shows a help prompt.']({{ site.baseurl }}/assets/images/ide/help-prompt.png)

---

We hope that this is helpful 👍. If you have any follow-up questions 🧐 or comments, we look forward to addressing them on the forum.

Have a productive week!

---
Acknowledgements
{: .fs-4 }

* Specials thanks to Liubov Kurafeeva and Roman Beltiukov for creating the initial instructions and screenshots.
  {: .fs-3 }
* Updated W23 by P. Conrad
  {: .fs-3 }

* General instructions were adopted from <https://python-adv-web-apps.readthedocs.io/en/latest/>.
  {: .fs-3 }

