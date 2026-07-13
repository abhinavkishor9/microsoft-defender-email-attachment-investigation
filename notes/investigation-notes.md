# Investigation Notes

## Incident Summary

Alert generated after opening a malicious email attachment (EICAR test file).

Microsoft Defender detected the file through Real-Time Protection and quarantined it automatically.

---

## Detection Timeline

### Step 1

Created:

```
C:\EmailLab
```

---

### Step 2

Downloaded:

```
eicar.com
```

---

### Step 3

User opened the attachment.

---

### Step 4

Microsoft Defender generated a malware detection alert.

---

### Step 5

The file was quarantined automatically.

---

### Step 6

Reviewed:

Microsoft-Windows-Windows Defender/Operational

---

## Event Reviewed

### Event ID 1117

Purpose

Malware detected and remediation performed.

Observed Information

- Malware Name
- Threat Severity
- Detection Source
- File Path
- User
- Process
- Action Taken

---

## Malware Details

Threat

```
Virus:DOS/EICAR_Test_File
```

Severity

```
Severe
```

Detection Source

```
Real-Time Protection
```

Action

```
Quarantine
```

Location

```
C:\EmailLab\eicar.com
```

---

## Protection History

Verified

- Threat detected
- Threat quarantined
- No further action required

---

## Validation

Checked the folder:

```
C:\EmailLab
```

The malicious file was no longer present.

---

## Conclusion

Microsoft Defender successfully prevented execution of the simulated malicious attachment and isolated the threat automatically.
