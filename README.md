# Cloud_backup_system

## Project Introduction
Automatically upload and back up the files that need to be backed up in the specified folder on the local computer to the server. And it can be viewed and downloaded at any time through a browser. The download process supports breakpoint continuation function, and the server will also manage hotspots for uploaded files, compressing and storing non hotspots to save disk space.

## Development Environment
- centos7.6/vscode for server
- windows11/vs2019 for client
- Makefile

besides,you should upgrade gcc to version 7.3,install the jsoncpp library,download the 'bundle' data compression lib and download the 'httplib' lib

## Key Technology
- file compression
- Hotspot management
- resume
- Singleton
- http


## Server Functions
- Backup and store files uploaded by the client.

- Capable of managing hot files, compressing and storing non hot files, saving disk space.

- Support client browser to view the access file list.

- Support client browser to download files, and support breakpoint continuation for downloading.

## Server Module
- Data management module: responsible for managing the information of backup files on the server.

- Network communication module: Build a network communication server to achieve communication with clients.

- Business processing module: corresponding business processing and response results for each request from the client.

- Hotspot management module: responsible for determining the hotspots of files and compressing and storing non hotspot files.

## Client Functions
- Can automatically detect files in the specified folder of the client and determine whether backup is needed.

- Upload the files that need to be backed up one by one to the server.

## Client Module
- Data management module: responsible for managing file information for client backup, which can determine whether a file needs to be backed up.

- File detection module: Traverse to obtain all file path names in the specified folder.

- Network communication module: Build a network communication client to backup and upload file data to the server.

## Performance Testing
Test environment:


server:
- CPU -2 core memory -2GB
- System disk - SSD cloud hard drive 40GB
- OS：CentOS 7.6 64bit


client:
- CPU 11th Gen Intel(R) Core(TM) i5-11320H @ 3.20GHz   3.19 GHz
- System disk - SSD 512G
- OS: windows 11



The transmission speed of cloud backup can reach 100kb/s


The server supports about 20 clients
