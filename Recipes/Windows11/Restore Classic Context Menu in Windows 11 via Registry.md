# Restore Classic Context Menu in Windows 11 via Registry

Windows 11 simplified the right-click menu, requiring a **"Show more options"** click to access the classic menu. The following registry tweak restores the classic context menu permanently.

---

## Steps

### 1. Open Registry Editor
- Press `Win + R`, type `regedit`, and press **Enter**.

### 2. Navigate to

```HKEY_CURRENT_USER\Software\Classes\CLSID```

### 3. Create a New Key
- Right-click `CLSID` → **New → Key**
- Name it:

```{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}```


### 4. Create a Subkey
- Right-click the new key → **New → Key**
- Name it:

```InprocServer32```

### 5. Set Default Value
- Select `InprocServer32` → double-click **(Default)** in the right pane.
- Leave the **Value data** blank → click **OK**.

### 6. Restart Explorer or PC
- Open **Task Manager** → find **Windows Explorer** → right-click → **Restart**
- Or simply restart your PC.

---

After this, the **classic right-click menu** will appear directly, bypassing the **"Show more options"** step.