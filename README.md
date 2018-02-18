# ansible-role-drachtio [![Build Status](https://secure.travis-ci.org/davehorton/ansible-role-drachtio.png)](http://travis-ci.org/davehorton/ansible-role-drachtio)

This is an ansible role for building a [drachtio server](https://github.com/davehorton/drachtio-server). 

## Role variables

Available variables are listed below, along with default values (see defaults/main.yml):

```
drachtioAdminPort: 9022
```
The TCP port that the drachtio server will listen on for client (app) connections.

```
drachtioSecret: cymru
```
The shared secret used by clients to authenticate.

```
drachtioSipInterface: eth0
```
The network device on which to listen for sip messages

```
drachtioAdminInterface: eth0
```
The network device on which to listen for client (app) connections.

```
drachtioLogFilePattern: drachtio.log
```
The name, or pattern, of the log file to write.  

```
drachtioLogFileDirectory: /var/log/drachtio
```
The directory to write log files into.

```
drachtioLogArchiveDirectory: /var/log/drachtio/archive
```
The directory into which to archive log files

```
drachtioLogFileSize: 5
```
The size of the log file, in GiB, which, when reached, will cause the file to be rotated.  Note that log files are also rotated on a daily basis.

```
drachtioLogFileMaxSize: 10
```
Specifies the maximum total size, in GiB, of current and archived files will keep before deleting archived files.

```
drachtioBranch: master
```
The github branch to build.


## Example playbook
```
---
- hosts: all
  become: yes
  roles:
    - ansible-role-drachtio
  become: yes
```
