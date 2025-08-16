# Update Disabler
Update Disabler's goal is to completely disable Windows Updates, whether it's Services, Task, Reg's or Exe's.

<img width="978" height="512" alt="image" src="https://github.com/user-attachments/assets/5b679e9e-de15-49f1-929b-fc6cc187ba3c" />
![GitHub Release Downloads](https://img.shields.io/github/downloads/QuakedK/Update-Disabler/total)

# #1 Usage
Update Disabler is required to be ran with Nsudo to delete, change or disable things without premission issues.

1. Download [Nsudo](https://github.com/M2TeamArchived/NSudo/releases/download/9.0-Preview1/NSudo_9.0_Preview1_9.0.2676.0.zip) (Offical Site) or the Standalone exe from [Downloads](https://github.com/QuakedK/Update-Disabler/raw/refs/heads/main/Downloads/NSudoLG.exe)
2. Download [Update Disabler]().
3. Open [NSudoLG.exe](https://github.com/QuakedK/Update-Disabler/raw/refs/heads/main/Downloads/NSudoLG.exe) and Enable All Privileges then drop/drag [Update Disabler]() into Nsudo then click run.

# #2 Revert
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

move /Y "C:\Update Disabler\Apps Backup\UsoClient.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\upfc.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\DoSvc.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\DoSvc.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\SIHClient.exe" "C:\Windows\System32"        
move /Y "C:\Update Disabler\Apps Backup\sihclient.exe.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\wuauclt.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\wusa.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\wusa.exe.mui" "C:\Windows\System32\en-US"
move /Y "C:\Update Disabler\Apps Backup\MusUpdateHandlers.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\MusUpdateHandlers1.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\MoNotificationUxStub.exe" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\WaaSMedicSvc.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\WaaSMedicPS.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\WaaSAssessment.dll" "C:\Windows\System32"
move /Y "C:\Update Disabler\Apps Backup\USS" "C:\Windows\UUS"
```
