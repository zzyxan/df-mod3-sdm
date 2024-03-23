# df-mod3-sdm


Get-WinEvent -ListLog * | where-object RecordCount -CLT 200 > "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\List-Log-filtered-by-RecordCount.txt"
select-string "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs.txt" -Pattern 'Starting' > "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs-filtered.txt"
get-content "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs.txt" | Export-csv  "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\logs-csv.csv"
mkdir "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2"
copy-item -Path "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise1\logs.txt" -Destination "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2"
get-acl "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise1\logs-csv.csv" > "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2\Acl-Logs-csv.txt"
get-content "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2\Acl-Logs-csv.txt" | export-csv "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise2\Acl-Logs-csv.csv"
get-acl "C:\Users\zzyxa\OneDrive\Desktop\Digital Forensics Autopsy\df-mod3-sdm\Exercise3"
