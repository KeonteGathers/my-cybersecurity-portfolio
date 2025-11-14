# 🔍 Digital Forensics: Suspicious USB Device Investigation

## Overview  
Conducted a digital forensics investigation into a suspected data theft incident involving an unauthorized USB device. Analyzed USB artifacts, registry keys, timestamps, and file access behavior to determine whether sensitive data was copied.

---

## 🛠 Tools & Artifacts Reviewed  
- Windows Registry (USBSTOR keys)  
- Event Logs (logon/logoff, device events)  
- NTFS timestamps (MAC times)  
- SetupAPI logs  
- Forensic imaging & analysis tools  

---

## 🚨 Scenario  
Security team suspected:
- After-hours activity  
- Possible data exfiltration  
- Unauthorized removable media  

The workstation showed signs of unusual activity around 10:47 PM.

---

## 🔬 Investigation Steps

### **1. USB Device History Review (Registry Artifacts)**
Reviewed:
```
HKLM\SYSTEM\CurrentControlSet\Enum\USBSTOR
HKLM\SYSTEM\CurrentControlSet\Enum\USB
```
Found:
- A never-before-seen USB storage device  
- Vendor ID, Product ID, and Serial Number  
- First/Last connected timestamps matching the incident window  

---

### **2. Correlated User Session Activity**
Reviewed:
- Security Event Logs  
- Logon, unlock, and active session events  

Findings:
- User was logged in during USB insertion  
- No other user sessions active  
- Activity occurred outside business hours  

---

### **3. File Access Timeline (NTFS MAC Times)**
Reviewed:
- Recent file opens  
- Shortcut (.lnk) files  
- RecentItems artifacts  
- Sensitive directory activity  

Findings:
- Multiple sensitive files accessed minutes after USB insertion  
- Access patterns strongly indicated file review and possible copying  

---

### **4. System Sweep for Deleted or Temporary Artifacts**
Checked:
- Recycle Bin  
- Temp files  
- Prefetch  
- Browser history  

Findings:
- No malware or external compromise  
- No signs of wiping tools  
- Behavior consistent with intentional insider activity  

---

## ✔ Final Conclusion  
The combined evidence strongly supports **unauthorized data transfer** via a removable USB device by an internal user.  
While Windows does not log copy events, the forensic timeline aligns precisely with suspicious activity.

---

## 🛡 Recommendations  
### **Technical Controls**
- Disable USB storage via Group Policy  
- Deploy Data Loss Prevention (DLP) tools  
- Enforce encryption on approved USBs  
- Enable advanced logging for removable media  

### **Policy & Training**
- Updated acceptable use policy  
- Mandatory annual data handling training  
- Stricter workstation monitoring  

---

## 📌 Outcome  
Successfully built a full forensic timeline that identified high-risk insider behavior. Recommended DLP and monitoring upgrades to prevent future incidents.
