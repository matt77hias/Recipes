# Enable NumLock on Boot in Windows 11 via Registry

To make Windows automatically turn on NumLock at startup, modify the registry as follows.

---

## Steps

### 1. Open Registry Editor
- Press `Win + R`, type `regedit`, and press **Enter**.

### 2. Navigate to

```HKEY_CURRENT_USER\Control Panel\Keyboard```

### 3. Modify `InitialKeyboardIndicators`
- In the right pane, locate `InitialKeyboardIndicators`.
- Double-click it and set the value:
  - `2` → NumLock ON at startup
  - `0` → NumLock OFF at startup

### 4. Apply the Change for Default User
- Navigate to:

```HKEY_USERS.DEFAULT\Control Panel\Keyboard```

### 5. Modify `InitialKeyboardIndicators`
- In the right pane, locate `InitialKeyboardIndicators`.
- Double-click it and set the value:
  - `2` → NumLock ON at startup
  - `0` → NumLock OFF at startup

### 5. Restart Your PC
- NumLock should now be enabled automatically.