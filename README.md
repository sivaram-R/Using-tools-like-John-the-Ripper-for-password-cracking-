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
![df1](https://github.com/user-attachments/assets/d924d10f-cc50-4d53-a2db-34305e09ac1c)

![ddf2](https://github.com/user-attachments/assets/43cfe218-f425-41f5-a6c4-8e75b78262ec)
![df3](https://github.com/user-attachments/assets/3732f02f-ad33-4030-9916-21c9be1831b8)

### Create a Password-Protected ZIP File
![df4](https://github.com/user-attachments/assets/d637b2c2-bbe7-406f-82d9-c4e029316a4a)



### Extract the Hash from the ZIP File


![df5](https://github.com/user-attachments/assets/8cedb80d-f84a-406f-86ff-b5a6d3824456)



### Crack the ZIP Password using John
![df6](https://github.com/user-attachments/assets/4356e733-90d2-4b7c-82a1-bab5bc91dbc7)

### Show the Cracked Password
![df7](https://github.com/user-attachments/assets/d98e9bab-61d6-4ff3-bc79-82d699c080e8)


## RESULT:
The password hashes were successfully cracked using John the Ripper.

