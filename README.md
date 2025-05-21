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
![Screenshot 2025-05-21 150706](https://github.com/user-attachments/assets/87ce7820-4dd0-4a93-82d2-63bb0af71766)

## COMMAND AND OUTPUT
the directory "my-folder"


![Screenshot 2025-05-21 150923](https://github.com/user-attachments/assets/30d6276d-b717-4596-b89f-6bfd58c53a48)



## COMMAND AND OUTPUT


Create the file Rose.txt

![Screenshot 2025-05-21 151150](https://github.com/user-attachments/assets/1d387112-9206-48cf-b889-194103bbf63f)


## COMMAND AND OUTPUT


Create the file hello.txt using echo and redirection


![Screenshot 2025-05-21 151322](https://github.com/user-attachments/assets/842d80f5-9854-4391-9290-d172c2b61b5b)



## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt


![Screenshot 2025-05-21 151528](https://github.com/user-attachments/assets/92d26e69-f112-42d9-a198-73d40e690c1a)


## COMMAND AND OUTPUT

Remove the file hello1.txt

![Screenshot 2025-05-21 150923](https://github.com/user-attachments/assets/6b9f4481-e07c-4dc4-a2db-cf5ea0f3327d)


## COMMAND AND OUTPUT

List out the file hello1.txt in the current directory
![Screenshot 2025-05-21 151703](https://github.com/user-attachments/assets/c89ab8d4-139f-41f8-a3fd-d2f8ed4e3e9c)

## COMMAND AND OUTPUT

List out all the associated file extensions 

![Screenshot 2025-05-21 151809](https://github.com/user-attachments/assets/efc2726b-ed7a-46e1-8d59-991cfa678fcf)
![Screenshot 2025-05-21 151824](https://github.com/user-attachments/assets/2f7f6ba8-621e-4562-9686-9efd097914f9)
![Screenshot 2025-05-21 151836](https://github.com/user-attachments/assets/9225d687-3b24-46b1-95d1-258b65f38855)
![Screenshot 2025-05-21 151844](https://github.com/user-attachments/assets/3f39369b-287b-4e1d-850b-10fe045bc9ea)
![Screenshot 2025-05-21 151855](https://github.com/user-attachments/assets/d3694afd-213c-410e-8784-2260cff74e06)

![Screenshot 2025-05-21 151903](https://github.com/user-attachments/assets/8e7f55bb-e3d1-4445-9faf-f8ce4d2f3ab8)

![Screenshot 2025-05-21 151911](https://github.com/user-attachments/assets/7eddde87-646b-4729-a96b-df737d56939b)
![Screenshot 2025-05-21 151933](https://github.com/user-attachments/assets/79e8ba40-b1d9-4ecd-8057-798f76317fb9)
![Screenshot 2025-05-21 151943](https://github.com/user-attachments/assets/017e9d94-7d96-485f-b2a7-f98df88f915f)
![Screenshot 2025-05-21 151954](https://github.com/user-attachments/assets/854548d8-314a-4ab2-b088-ec554fe5097f)
![Screenshot 2025-05-21 151954](https://github.com/user-attachments/assets/21388278-92ad-4171-878b-9655b3f81c99)
![Screenshot 2025-05-21 152010](https://github.com/user-attachments/assets/e6d269f4-d4eb-4323-89ce-23619ba910be)
![Screenshot 2025-05-21 152018](https://github.com/user-attachments/assets/e7f9c317-1bae-4b3e-8a2a-f0f3a9e12009)

![Screenshot 2025-05-21 152027](https://github.com/user-attachments/assets/7f69d989-50d2-460d-97ff-f777dfed159e)

## COMMAND AND OUTPUT


Compare the file hello.txt and rose.txt

![image](https://github.com/user-attachments/assets/58cbe80d-293d-41d5-bb19-117f78459d4d)

## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%!
pause


```



## OUTPUT

![Screenshot 2025-05-21 152327](https://github.com/user-attachments/assets/70945e0a-754a-4a6b-83d7-9ddcf269feec)


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
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

```


## OUTPUT

![Screenshot 2025-05-21 152319](https://github.com/user-attachments/assets/0af572f4-7d1c-4ff3-b18b-7eb570c4d932)



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```


## OUTPUT


![Screenshot 2025-05-21 152509](https://github.com/user-attachments/assets/7b361b85-6b36-401e-af31-591f50fd5059)


Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```

@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause


```
## OUTPUT
![Screenshot 2025-05-21 152752](https://github.com/user-attachments/assets/ec190c3f-8d71-49f0-a75c-e85acd2f5177)


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
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


```

## OUTPUT

![Screenshot 2025-05-21 152956](https://github.com/user-attachments/assets/ac98a665-1cbf-49a2-a684-4cad4e32e36e)


# RESULT:
The commands/batch files are executed successfully.

