# Basic Device Security : hostname, password, and Encryption

## Objective

Practice securing Cicso devices ny settings hostname ,password ,configuring both unencrypted and encrypted passwords, and viewing configuration differences.

## Network Topology

![topology](./Basic%20Device%20Security%20d.png)


## Notes 
- "hostname" helps to identify the drive u usening 
- "enable password" is help to secure your devices 
- "enable secret" is preferred due to automatic encryption (MD5)
  

## Lab staps 

### Set name for devices
- First enter configuration mode on both
- second set a hostname 
```bash 
  enable or {en}
  configure terminal or {config t}
  hostname (name) 
```
### Set Unencrypted Enable Password
```bash 
en 
config t 
enable password (password)
```
###  Exit and Test the Password
```bash
exit 
exit
```
### View Password in Running Config
```bash
show running-config 
```
![topology](./Running%20config%20v.png)
###  Encrypt All Passwords (Optional Encryption for Line Passwords)
```bash
config t
service password-encryption
```
### Set a More Secure Encrypted Password
```bash
enable secret Cisco
```
### Save the Configuration
```bash
copy running-config startup-config

```