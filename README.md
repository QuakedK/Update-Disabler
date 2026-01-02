# Update Disabler
Update Disabler's goal is to completely disable Windows Updates, whether it's Services, Task, Reg's or Exe's.

<img width="978" height="512" alt="image" src="https://github.com/user-attachments/assets/5b679e9e-de15-49f1-929b-fc6cc187ba3c" />

![GitHub Release Downloads](https://img.shields.io/github/downloads/QuakedK/Update-Disabler/total)

# #1 Usage
Update Disabler is required to be ran with Nsudo to delete, change or disable things without premission issues.

[Update Disabler Extreme](https://github.com/QuakedK/Update-Disabler/releases/download/Winupdatedisabler/Update-Disabler-Extreme-V1.2.bat) | 
The **Extreme Version** disables Update Services, deletes Update Task, disables Updates via the registry and most importantly from the extreme version it deletes Windows Update System32 and SysWow64 files, fully preventing windows from re-enabling windows updates. However deleting System32 and SysWow64 files could cause unexpected behavior. Please Check and read the [Unsupported Features](https://github.com/QuakedK/Update-Disabler/blob/main/Unsupported%20Features.md).

[Update Disabler Lite](https://github.com/QuakedK/Update-Disabler/releases/download/Winupdatedisabler/Update-Disabler-Lite-V1.2.bat) |
The **Lite Version** disables Update Services, deletes Update Task, and disables Updates via the registry. This a great and simple this is a great alternative for those who don't want to lose functionality or deal with unsupport features.

1. Download [Nsudo](https://github.com/M2TeamArchived/NSudo/releases/download/9.0-Preview1/NSudo_9.0_Preview1_9.0.2676.0.zip) (Offical Site) or the Standalone exe from [Downloads](https://github.com/QuakedK/Update-Disabler/raw/refs/heads/main/Downloads/NSudoLG.exe).
2. Download and choose your [Update Disabler](https://github.com/QuakedK/Update-Disabler/releases/tag/Winupdatedisabler) version.
3. Open [NSudoLG.exe](https://github.com/QuakedK/Update-Disabler/raw/refs/heads/main/Downloads/NSudoLG.exe) and Enable All Privileges then drop/drag Update Disabler into Nsudo then click run.

# #2 Revert (Extreme Version)
Note: Manually attempting to System Restore using the Extreme Version, doesn't work unless you restore in Advanced Recovery. See more info in the [Unsupported Features](https://github.com/QuakedK/Update-Disabler/blob/main/Unsupported%20Features.md#system-restore-points).

1. Open CMD and Paste the following.
```bat
sc config TrustedInstaller start=auto
```
2. Open [Nsudo](https://github.com/QuakedK/Task-Destroyer/raw/refs/heads/main/Downloads/NSudoLG.exe) and Enable All Privileges.
3. Then type CMD in the Address Bar, then click run and paste the following commands.
```bat
reg import "C:\Update Disabler\Reg Backup\PolicyBackup.reg"
reg import "C:\Update Disabler\Reg Backup\UpdateOrchestratorServiceBackup.reg" 
reg import "C:\Update Disabler\Reg Backup\UpdateOrchestratorTaskBackup.reg"
reg import "C:\Update Disabler\Reg Backup\WindowsUpdateMedicServiceBackup.reg"
reg import "C:\Update Disabler\Reg Backup\WindowsUpdateServiceBackup.reg"
reg delete "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate" /f

move /Y "C:\Update Disabler\Apps Backup\System32\DoSvc.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\DoSvc.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\System32\MoNotificationUxStub.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\MusUpdateHandlers.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\MusUpdateHandlers.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\System32\MusUpdateHandlers1.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\MusUpdateHandlers1.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\System32\Sihclient.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\sihclient.exe.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\System32\UIEOrchestrator.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\UpdateAgent.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\UpdateCompression.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\updatecsp.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\updatepolicy.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\UpdatePolicy.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\System32\UpdateReboot.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\UpgradeResultsUI.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\UpgradeResultsUI.exe.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\System32\upfc.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\UsoClient.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\WaaSAssessment.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\WaaSMedicPS.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\WaaSMedicSvc.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\wuauclt.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\wusa.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\System32\wusa.exe.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\SysWOW64\UpdateCompression.dll" "C:\Windows\SysWOW64"
move /Y "C:\Update Disabler\Apps Backup\SysWOW64\wusa.exe" "C:\Windows\SysWOW64"
move /Y "C:\Update Disabler\Apps Backup\USS" "C:\Windows\UUS"

sc config TrustedInstaller start=auto >nul 2>&1
sc config uhssvc start=auto >nul 2>&1
sc config BITS start=auto >nul 2>&1
sc config DoSvc start=auto >nul 2>&1
```
# #3 Revert (Lite Version)
Note: If you created a Restore Point you can just use that <3

1. Open CMD and Paste the following.
```bat
sc config TrustedInstaller start=auto
```
2. Open [Nsudo](https://github.com/QuakedK/Task-Destroyer/raw/refs/heads/main/Downloads/NSudoLG.exe) and Enable All Privileges.
3. Then type CMD in the Address Bar, then click run and paste the following commands.
```bat
reg import "C:\Update Disabler\Reg Backup\PolicyBackup.reg"
reg import "C:\Update Disabler\Reg Backup\UpdateOrchestratorServiceBackup.reg" 
reg import "C:\Update Disabler\Reg Backup\UpdateOrchestratorTaskBackup.reg"
reg import "C:\Update Disabler\Reg Backup\WindowsUpdateMedicServiceBackup.reg"
reg import "C:\Update Disabler\Reg Backup\WindowsUpdateServiceBackup.reg"
reg delete "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate" /f

sc config TrustedInstaller start=auto >nul 2>&1
sc config uhssvc start=auto >nul 2>&1
sc config BITS start=auto >nul 2>&1
sc config DoSvc start=auto >nul 2>&1
```
