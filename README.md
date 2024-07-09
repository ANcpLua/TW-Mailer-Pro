![image](https://github.com/ANcpLua/TW-Mailer-Pro/assets/124206820/38be1b2d-aa62-4d11-9f03-accdfd5fc67c)
# TwMailer Project

## Prerequisites

Before you can build and run TwMailer, you need to install several dependencies.

### Install LDAP Development Libraries

```bash
sudo apt-get install -y libldap2-dev
```
```bash
sudo apt-get install -y libldap2-dev
```
```bash
Install Build Tools
```
```bash
sudo apt-get install -y build-essential
```
```bash
Install CMake and Git for GoogleTest
```
```bash
sudo apt-get install -y cmake git
```
```bash
Clone the GoogleTest repository to your project directory.
```
```bash
cd ~/Documents/TwMailer/tests
git clone https://github.com/google/googletest.git || (cd googletest && git pull)
```
Directory Structure
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

Building the Project

Navigate to the project root directory and run make to build the application.

```bash
make all
```
To clean the build artifacts:
```bash
make clean
```
Running Tests Navigate to the tests directory
```bash
cd tests
make all
```
To clean the test build artifacts:
```bash
make clean
```
To run the tests:
```bash
make test
```

#!/bin/bash

# Define the base directory (current directory)
BASE_DIR=$(pwd)

# Create necessary directories
mkdir -p "$BASE_DIR/src/server"
mkdir -p "$BASE_DIR/src/client"
mkdir -p "$BASE_DIR/src/shared"
mkdir -p "$BASE_DIR/include"
mkdir -p "$BASE_DIR/build/server"
mkdir -p "$BASE_DIR/build/client"
mkdir -p "$BASE_DIR/build/shared"
mkdir -p "$BASE_DIR/bin"
mkdir -p "$BASE_DIR/conf"
mkdir -p "$BASE_DIR/logs"
mkdir -p "$BASE_DIR/mail_spool"
mkdir -p "$BASE_DIR/tests"
mkdir -p "$BASE_DIR/tests/obj"
mkdir -p "$BASE_DIR/tests/obj/client"
mkdir -p "$BASE_DIR/tests/obj/shared"
mkdir -p "$BASE_DIR/tests/obj/server"

echo "TwMailer directory structure has been created successfully."
echo "Project root: $BASE_DIR"
echo ""
echo "Directory structure:"
echo "├── src"
echo "│   ├── server"
echo "│   ├── client"
echo "│   └── shared"
echo "├── include"
echo "├── build"
echo "│   ├── server"
echo "│   ├── client"
echo "│   └── shared"
echo "├── bin"
echo "├── conf"
echo "├── logs"
echo "├── mail_spool"
echo "└── tests"
echo "    ├── obj"
echo "    │   ├── client"
echo "    │   ├── shared"
echo "    │   └── server"
