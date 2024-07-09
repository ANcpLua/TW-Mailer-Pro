![image](https://github.com/ANcpLua/TW-Mailer-Pro/assets/124206820/38be1b2d-aa62-4d11-9f03-accdfd5fc67c)
# TwMailer Project

## Prerequisites

Before you can build and run TwMailer, you need to install annoying dependencies.

### Install Build Tools for Make and g++
```bash
sudo apt-get install -y build-essential
```
### Install LDAP Development Libraries
```bash
sudo apt-get install -y libldap2-dev
```
### Install CMake and Git for GoogleTest
```bash
sudo apt-get install -y cmake git
```
### Clone the GoogleTest repository to your project directory.
```bash
cd ~/Documents/TwMailer/tests
git clone https://github.com/google/googletest.git || (cd googletest && git pull)
```
### Directory Structure
```bash
├── src
│   ├── server
│   ├── client
│   └── shared
├── include
├── build
│   ├── server
│   ├── client
│   └── shared
├── bin
├── conf
├── logs
├── mail_spool
└── tests
     └─ obj
        ├── client
        ├── shared
        └── server
```

### Building the Project
Navigate to the project root directory and run make to build the application.

```bash
make all
```
To clean the build artifacts:
```bash
make clean
```
### Tests
Navigate to the tests directory
```bash
cd tests
make all
```
To run the tests:
```bash
make test
```
