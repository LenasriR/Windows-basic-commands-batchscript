# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"
<img width="710" height="120" alt="image" src="https://github.com/user-attachments/assets/95565a6d-0852-4454-850e-6c5f07bf7ad1" />

## COMMAND AND OUTPUT

Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="644" height="50" alt="image" src="https://github.com/user-attachments/assets/797f396c-1f08-44c0-b792-3283a06014ad" />


Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="728" height="132" alt="image" src="https://github.com/user-attachments/assets/2018e56a-5511-4ffb-bc85-e2d5b942715c" />
<img width="1004" height="315" alt="image" src="https://github.com/user-attachments/assets/8e1ebff1-f3d5-49e3-8bfa-6b0d45670ad9" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="896" height="52" alt="image" src="https://github.com/user-attachments/assets/c0d68332-4e71-4b0a-91bf-07bca2f60112" />
<img width="728" height="65" alt="image" src="https://github.com/user-attachments/assets/c0ead8e1-b372-4f30-857a-c5a07d48741d" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="831" height="74" alt="image" src="https://github.com/user-attachments/assets/a5db2c9a-8ce2-475a-b62d-e74dfa266f6b" />

Remove the file hello1.txt

## COMMAND AND OUTPUT

List out the file hello1.txt in the current directory
<img width="812" height="208" alt="image" src="https://github.com/user-attachments/assets/189f5f70-ba26-48ab-a7a1-280ac9b499ce" />

## COMMAND AND OUTPUT

List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="714" height="744" alt="image" src="https://github.com/user-attachments/assets/f81cf020-3801-4e36-9e08-cb30c8296252" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="756" height="268" alt="image" src="https://github.com/user-attachments/assets/0751037a-e03b-4807-b964-035c8217c3aa" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
~~~
@echo off
set name=John
echo Hello, %name%!
pause
~~~


## OUTPUT

<img width="618" height="101" alt="image" src="https://github.com/user-attachments/assets/e2c42b26-ac37-49ab-83a9-664b5230c34b" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
~~~
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
~~~


## OUTPUT

<img width="819" height="190" alt="image" src="https://github.com/user-attachments/assets/db178e19-857e-4977-9908-def230373eed" />

Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
~~~
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
~~~



## OUTPUT

<img width="666" height="243" alt="image" src="https://github.com/user-attachments/assets/948f63cf-55f4-401c-b0ab-d7ddee069028" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
~~~
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
~~~
## OUTPUT
<img width="610" height="94" alt="image" src="https://github.com/user-attachments/assets/22821794-beb2-41a3-af8c-7cdb0ddf1443" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
~~~
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
~~~

## OUTPUT

<img width="584" height="373" alt="image" src="https://github.com/user-attachments/assets/caa309ab-de15-464b-9e7c-b698dd87a358" />


# RESULT:
The commands/batch files are executed successfully.

