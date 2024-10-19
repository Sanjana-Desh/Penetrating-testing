# To change password
    - passwd: type orignal pass and pass you want.

# ⁡⁢⁣⁢LINUX IS CASE SENISITIVE⁡

#  Basic Commands
- ⁡⁣⁣⁢pwd⁡ : print working Directory
- ⁡⁣⁣⁢cd⁡ : change directory (type cd and tab twice it'll show directiory where we can go)
    - cd .. : take one directory backcd
- ⁡⁣⁣⁢ls⁡: gives list of everything that is in the directory.
- ⁡⁣⁣⁢mkdir⁡ directoryname : make directory
- ⁡⁣⁣⁢rmdir⁡ directoryname : remove directory
- ⁡⁣⁣⁢ls -la⁡ : shows the hidden files (has dot)
- ⁡⁣⁣⁢echo "hello" > new.txt⁡ : creates a file named new.txt and types echo in it
- ⁡⁣⁣⁢cp old.txt Newfilename.txt⁡ : copies one file content to another file, also creates it
- ⁡⁣⁣⁢cp old.txt test/new1.txt⁡ : copes the existing file and creates new one and puts it in exisiting folder names test
- ⁡⁣⁣⁢rm⁡ : to remove a file.
- ⁡⁣⁣⁢mv file.txt test/file1.txt⁡ : moves file.txt content to file1.txt which is inside test folder and if file1 is not present, it is created
- ⁡⁣⁣⁢locate file.txt:⁡ to locate a file but for this generally you need to run ⁡⁢⁣⁢updatedb⁡ command for it to give location of file
- ⁡⁣⁣⁢updatedb⁡ : updates database, can only run in root user.
- ⁡⁣⁣⁢sudo -s⁡ : helps in becoming root user.
- ⁡⁣⁣⁢man⁡ commandname: opens a manual
- ⁡⁣⁣⁢chmod⁡ : gives permission.
    • chmod 777 : all read write and execute
    • chmod +x : we can use execute on file
    ⁡⁢⁣⁢• Whenever we running any script or python file it should be in executable format⁡


# Understanding ls -la
    drwxrwxr-x 2 kali kali 4096 Oct 19 05:11 .
    drwxr-xr-x 3 kali kali 4096 Oct 19 05:11 ..
    -rw-rw-r-- 1 kali kali    0 Oct 19 05:11 ⁡⁢⁢⁢𝗳𝗶𝗹𝗲.𝘁𝘅𝘁⁡

    - Here the one starting from d these are directory, rwx shows it has read write and execute permission
    - Here the one starting from - is file, when it is executable it shows itself in green the one I've marked

# Add new user
- Step 1

    Command : ⁡⁣⁣⁢adduser⁡ sanjana

    Generally the directory follows : / (root directory) --> /home (home directory) --> /kali (user directory) here other users created can be present too.
    ⁡⁢⁣⁢DOONT GET CONFUSED WITH ROOT DIRECTORY AND ROOT USER⁡

    info: Adding new user `sanjana' (1001) with group `sanjana (1001)' ...
    info: Creating home directory `/home/sanjana' ...

- Step 2 : add password
    New password: 
    Retype new password: 
    passwd: password updated successfully
    Changing the user information for sanjana

- Step 3 : Fill in information
    Enter the new value, or press ENTER for the default
            Full Name []: Sanjana Desh 
            Room Number []: 1
            Work Phone []: 8073641226
            Home Phone []: 9149415472
            Other []: 
    Is the information correct? [Y/n] y

    # 

    - ⁡⁣⁣⁢cat⁡ : display file contents
        ⁡⁣⁣⁢- cat etc/passwd⁡ : This is called password file tho it doesnot 
        contain any passwords, but it used to contain passwords before.
        ⁡⁢⁣⁢Now it provides placeholder of x for a diff file called shadow file⁡. 
        - But it can be used to see the user, uid, first line shows root, scrolling down to last line gives the other users on the machine too
        - When pentesting we are only concerned over the root and other users
        ⁡⁣⁣⁡⁣⁢-⁡ ⁡⁣⁣⁢cat etc/shadow⁡⁡ : The shadow file, typically located at /etc/shadow, is a secure file that contains the hashed passwords for user accounts in Unix-like operating systems. Unlike the /etc/passwd file, which is world-readable and contains basic account information.
        - Hashing: Instead of storing plain-text passwords, the shadow file stores hashed versions, which enhances security. When a user attempts to log in, the system hashes the input password and compares it to the stored hash.
        - sanjana:⁡⁢⁢⁢$y$j9T$JzRPpIagLmLCdDXZaSu7G.$2GNOThHDHzhp04.pq5QKVAXokA1jlIUDckaYL7mQ3J1:20015⁡⁢⁢⁢:0:99999:7:::
        this highlighted part is the password for sanjana user similarly for all users at the bottom it's present and for the root it is present at the top
        ⁡


