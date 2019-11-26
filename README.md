# unice

## Purpose
This project containts script files, written in bash, to automatically download courses files from uniwa eclass.

## Installation
You will need all uni-* files, just download them and make sure you have excecution permission

    chmod +x uni-connect uni-disconnect uni-list uni-request

## Usage

### uni-connect

    ./uni-connect [account_file]

This script logs in to the webserver, so you can download your files.
You can enter your account details either by editing the source code, or by providing a file with it. The syntax must be as follows:

    uname=your_user_name
    passw=your_password
 
### uni-list

    ./uni-list [-s]

This scirpt lists all your subscribed courses with their names. The -s options lists only the courses ID code.

### uni-request

    ./uni-request -d <download_dir> [-f] <courses_file_name> [-e] <course_ID_1> <coursed_ID_2> ... <course_ID_n>

This script attempts to download your wanted files. You will always need to specify -d option and -f or -e.

#### Option -d download_dir

Specify download folder.

#### Option -e course_ID_1 coursed_ID_2 ... course_ID_n

Specify which courses you want to install by providing the corresponding ID. Downloaded files' names will be generated automatically.

#### Option -f courses_file_name

Specify the file which contains your wanted courses' ID and, optionally, name.
If there is no name given for a course, then it will be generated automatically.

The syntax inside "courses_file_name" must be; first column for IDs and second for names. For example:

    ca987 math
    ph345 electronics
    ly123
    cs67

### uni-disconnect

Logs out from session.

### Example

Inside "acc.txt" file:

    uname=xxxx
    passw=yyyy
 
 Run in terminal:
    
    ./uni-connect acc.txt
    ./uni-list > courses.txt
    ./uni-request -d . -f courses.txt
    ./uni-disconnect

