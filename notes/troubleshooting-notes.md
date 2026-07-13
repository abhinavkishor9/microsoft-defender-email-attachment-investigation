# Troubleshooting Notes

## Problem

Downloaded file disappeared immediately.

### Cause

Microsoft Defender quarantined the EICAR file instantly.

### Resolution

Expected behavior.

Continue investigating using:

- Protection History
- Defender Operational Logs

---

## Problem

Unable to locate downloaded file.

### Cause

Automatic quarantine.

### Resolution

Verify:

```
C:\EmailLab
```

The folder exists but the file is removed.

---

## Problem

No malware detection event.

### Cause

File was not opened.

### Resolution

Open the EICAR file to trigger Defender.

---

## Problem

No Protection History entry.

### Cause

Real-Time Protection disabled.

### Resolution

Enable:

Windows Security

↓

Virus & Threat Protection

↓

Real-Time Protection

---

## Problem

Event Viewer shows no Event ID 1117.

### Cause

Incorrect log selected.

### Resolution

Navigate to:

```
Applications and Services Logs

↓

Microsoft

↓

Windows

↓

Windows Defender

↓

Operational
```

Filter:

```
1117
```

---

## Problem

Cleanup verification failed.

### Cause

Folder still exists after quarantine.

### Resolution

Remove manually:

```powershell
Remove-Item C:\EmailLab -Recurse
```

---

## Lessons Learned

- Defender can quarantine malware before execution.
- Operational logs provide detailed forensic evidence.
- Protection History complements Event Viewer.
- File disappearance after download is expected when malware is detected.
- Quarantine events should always be validated through multiple evidence sources.
