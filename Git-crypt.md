# Git-Crypt
Git-crypt is a tool to encrypt your secret files in order to be able to push the file such as .env and keys together with your code. The files are encrypted and decrypted using gpg keys.
Follow the following steps:
1. install git-crypt
```
sudo apt-get install git-crypt
```
2. initialize git-crypt after initializing git in your project folder
```
git-crypt
```
3. specify which files to encrypt inside the .gitattributes file using the following criteria 
    - to encrypt all files that ends with .key
      ```
      *.key filter=git-crypt diff=git-crypt
      ```
    - to encrypt a specific file.
      ```
      path/to/file filter=git-crypt diff=git-crypt
      ```
4. Add the gpg key for users who can encrypt the files you have encrypted
```
git-crypt add-gpg-user USER-ID 
```
The user id can be the email or key id of the GPG key.

5. To decrypt the file or files after cloning the repo 
```
git-crypt unlock
```
6. To check the status of the encryption
```
git-crypt status
```
