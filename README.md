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

    ./uni-request [-d] <download_dir> [-f] <courses_ID-names> [-e] course_ID_1 coursed_ID_2 ... course_ID_n

This script attempts to download your wanted files. You will always need to specify -d option and -f or -e.

With -d you will specify the folder you want to download your files.

With -e 
