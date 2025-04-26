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
![df1](https://github.com/user-attachments/assets/6f90f412-7dfa-4577-8737-eda249101476)
![ddf2](https://github.com/user-attachments/assets/479ba939-94ff-4ff9-a421-4d9bc76ed4fc)
![df3](https://github.com/user-attachments/assets/f12c19f9-b913-4c71-a1b5-a4aa611a9dd4)


### Create a Password-Protected ZIP File

![df4](https://github.com/user-attachments/assets/f94e40a7-9865-4837-92bf-000ba197cf7a)


### Extract the Hash from the ZIP File


![df5](https://github.com/user-attachments/assets/8d08c020-c09e-46d1-b378-d2d17750fe23)



### Crack the ZIP Password using John
![df6](https://github.com/user-attachments/assets/f2771cc9-9959-4aa3-9b00-845eeab06df4)




### Show the Cracked Password
![df7](https://github.com/user-attachments/assets/8f44203d-5dbb-492c-a36d-db5c0b7cd472)



## RESULT:
The password hashes were successfully cracked using John the Ripper.

