
![Screenshot 2025-01-24 034344](https://github.com/user-attachments/assets/d3582f9e-c2c2-4e28-843e-15ca009ff969)



# PowerShell Network Diagnostic [DNS Testing]
A simple network diagnostic tool designed for IT Help Desk professionals, written in PowerShell.

## Features
- **Ping a Host**: Check network connectivity with detailed response times.
- **Flush DNS Cache**: Clear the DNS resolver cache to troubleshoot network issues.
- **Trace Route**: Identify the path packets take to reach a host.

## Requirements
- Windows OS
- PowerShell 5.1 or later
- Administrator privileges (for DNS flushing)

![image](https://github.com/user-attachments/assets/6f0fd6f3-5409-4c41-8f1b-a7dfea2e2a5b)


In this project I used two VMs. One as a Client portal and another as a DC. Powershell will be used for Network and Cloud Management and main testing of DNS


![Screenshot 2025-01-24 040542](https://github.com/user-attachments/assets/0548e6ad-3935-4e99-8c2b-8e35ee1bb477)


Pinged "Mainframe" in Powershell from Client-1 VM to DC and Observed Fail Attempt




![Screenshot 2025-01-24 041045](https://github.com/user-attachments/assets/228da18c-6dc5-4952-aaf5-c73d68027551)





Ran "ipconfig /displaydns" to analyze local dns cache


![Screenshot 2025-01-24 042230](https://github.com/user-attachments/assets/c629ec2c-8f11-4e24-8f52-b21f0cd26cc7)



![Screenshot 2025-01-24 042301](https://github.com/user-attachments/assets/8981adcc-f0cd-49fa-9a40-a2274776e949)


Ran "ipconfig /displaydns > test.txt" and "notepad test.txt" to check for "Mainframe" in local DNS Cache from Notepad test script


![Screenshot 2025-01-24 042301](https://github.com/user-attachments/assets/d8b42f07-cc9d-424b-8066-38239bff103e)

 ## Steps to Locate Local Host File


![Screenshot 2025-01-24 043636](https://github.com/user-attachments/assets/114243b6-3b51-49da-ae79-716008c1766f)

Run Notepad as Admin

![Screenshot 2025-01-24 043725](https://github.com/user-attachments/assets/7d057f74-2907-4ff2-a766-329409d44d9f)


![Screenshot 2025-01-24 043751](https://github.com/user-attachments/assets/4fa94297-6c03-46b6-b6ec-0fe81e7964e8)

In TXT Documents choose "All files"

![Screenshot 2025-01-24 043930](https://github.com/user-attachments/assets/fb6abf74-63d2-4878-8a3a-c13789e1a48d)

Open "Drivers"

![Screenshot 2025-01-24 044002](https://github.com/user-attachments/assets/9f66ea0c-56fc-41b8-83fd-f22ee185b9af)

"ETC"

![Screenshot 2025-01-24 044018](https://github.com/user-attachments/assets/9b1adee7-6bf7-42b5-9a59-67ced2c8c54c)


![Screenshot 2025-01-24 044040](https://github.com/user-attachments/assets/2d959732-6628-4c50-a90d-0d804bd1b0e5)


Local Host File is located and ready to Map IP to Host Name


![image](https://github.com/user-attachments/assets/11a304bf-4290-4f76-a532-b442f0ce165c)

Pinged "Zebra" (for testing of Local host file)

![Screenshot 2025-01-24 050551](https://github.com/user-attachments/assets/0409f6ea-1203-46ea-80b8-9463ff01feff)

Assigned "Zebra" to Local Loopback IP Address in Local Host File

![image](https://github.com/user-attachments/assets/bd43682d-7cc2-451a-88ca-d0a6c378e867)

Successful ping of "Zebra" after assigning to loopback in LHF
