# Using-tools-like-John-the-Ripper-for-password-cracking
### Reg No:212222100050
### Name: Sivaram R
## AIM:
To crack password hashes using John the Ripper in Kali Linux.

## DESIGN STEPS:
### Step 1:
Install John the Ripper using the command:

### Step 2:
Prepare the password hash file (e.g., using unshadow for Linux password and shadow files).

### Step 3:
Use John the Ripper to crack the hashes:

## PROGRAM:

- **Install the John Ripper**
  ```bash
  sudo apt install john
  ```
- **Create a Password-Protected ZIP File**
   Archive a normal file (secret.txt) into a password-protected ZIP file
   ```bash
   zip --password 123abc secret.txt.zip secret.txt
   ```
 - **Extract the Hash from the ZIP File**
   ```bash
   zip2john secret.txt.zip > zip_hash.txt
   ```
- **Crack the ZIP Password using John**
  ```bash
  john --format=zip zip_hash.txt
  ```
- **Show the Cracked Password**
  ```bash
  john --show zip_hash.txt
  ```


## OUTPUT:


### Create a Password-Protected ZIP File
![K1 6](https://github.com/user-attachments/assets/a560773d-37ec-4c6a-99c6-b2863d364347)


### Extract the Hash from the ZIP File

![K2 6](https://github.com/user-attachments/assets/ec1efd6e-8931-49b7-8a9b-9a62e6d28b1c)



### Crack the ZIP Password using John
![K3 6](https://github.com/user-attachments/assets/b53e0192-9663-4eef-bf74-3998493f51a7)

![K4 6](https://github.com/user-attachments/assets/a4191db2-9e9d-4bd4-9b23-2a4bb61448c9)

### Show the Cracked Password

![K5 6](https://github.com/user-attachments/assets/01aa290c-10c5-49b1-aaa2-84bac8b9178b)

## RESULT:
The password hashes were successfully cracked using John the Ripper.

