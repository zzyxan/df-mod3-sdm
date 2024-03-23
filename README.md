# df-mod3-sdm
## Exercise1
### 1. Code to retrieve logs from "DoD-PKE InstallRoot"
#### 'get-winevent "DoD-PKE InstallRoot" > "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs.txt"' 
### 2. Code to select strings with 'Starting' from the txt logs of "DoD-PKE InstallRoot"
#### 'select-string "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs.txt" -Pattern 'Starting' > "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs-filtered.txt"' 
### 3. Code to Pipe Get-WinEvent to Where-Object, used to filter items in a pipeline, This one filters out any logs with a RecordCount Greater than 200.
#### 'Get-WinEvent -ListLog * | where-object RecordCount -CLT 200 > "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\List-Log-filtered-by-RecordCount.txt"'
### 4. Code to export Data to a csv file.
#### 'get-content "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs.txt" | Export-csv  "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs-csv.csv"'
## Exercise2
### 1. Code written to make a new directory at the specified path
#### 'mkdir "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2"'
### 2. Code Written to copy a file from the source path to a destination
#### 'copy-item -Path "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise1\logs.txt" -Destination "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2"'
### 3. Code to get the Access Control List for a file or directory
#### 'get-acl "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise1\logs-csv.csv" > "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2\Acl-Logs-csv.txt"'
### 4. Code to export data to a CSV File
#### 'get-content "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2\Acl-Logs-csv.txt" | export-csv "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2\Acl-Logs-csv.csv"'
## Exercise3
### I had a lot of trouble understanding this exercise, I wasn't able to really get why you would want to store a password as a secure string, and couldn't convert any files or directories to secure strings, furthermore I wasn't able to modify the 
### permissions for any files or directories, everything I read online had me use variables which I don't understand. I've done my best to answer the questions. But at this time I've hit a roadblock.
### 1. Code to convert a string to a secure string 
#### 'ConvertTo-SecureString "Password" -AsPlainText -Force'
### 2. Code to retrieve the ACL for a directory
#### 'get-acl "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise3"'
### 3. I tried my best to answer this question, but even looking at other students answers I do not understand how to accomplish the task.
