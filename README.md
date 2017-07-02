# README for UCM Tools #

This repo is for all of my Cisco UCM tools using Python.
The Cisco AXL SQL Toolkit is required to use the scripts. The scripts will reference the axlsqltoolkit directory under the script location.

## Tools ##

### BulkChangeDirectoryNumber.py

This tool was created to change DNs from one partition to another, one at a time.

#### Prerequisites

* suds-jurko package (pip install suds-jurko)
* Cisco axlsqltoolkit (from UCM plugins)
* User account with AXL access to the UCM server

#### Usage

Execute the script without any additional options.
The script will prompt with questions.


After entering a number you will be provided with a success or failure message. You will then be prompted to enter another number. If you hit enter <CR\> you will be dropped out of the script back to a prompt.

### BulkChangeEPNM.py

This tool was created to change the External Phone Number Mask in bulk to a list of phones.

#### Prerequisites

* suds-jurko package (pip install suds-jurko)
* Cisco axlsqltoolkit (from UCM plugins)
* User account with AXL access to the UCM server

#### Usage

Text file with two values separated by a comma.
The first value is the phone name - SEPBEEFBEEF0001.
The second value is the new External Phone Number Mask - 8005551212.

```
SEPBEEFBEEF0001,8005551212
```

Execute the script with a `-f` followed by the name of the text file with the information required.
`changeEPNMbulk.py -f testfile.txt`
