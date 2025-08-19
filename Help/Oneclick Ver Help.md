# Oneclick Ver Revert

Note: If you created a Restore Point you can just use that <3

1. Open CMD and Paste the following.
```bat
sc config TrustedInstaller start=auto
```
2. Open [Nsudo](https://github.com/QuakedK/Task-Destroyer/raw/refs/heads/main/Downloads/NSudoLG.exe) and Enable All Privileges.
3. Then type CMD in the Address Bar, then click run and paste the following commands.
```bat

reg import "C:\Oneclick Tools\Update Disabler\Reg Backup\PolicyBackup.reg"
reg delete "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate" /f

move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\DoSvc.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\DoSvc.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\MoNotificationUxStub.exe" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\MusUpdateHandlers.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\MusUpdateHandlers.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\MusUpdateHandlers1.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\MusUpdateHandlers1.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\Sihclient.exe" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\sihclient.exe.mui" "C:\Windows\System32\en-US"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\UIEOrchestrator.exe" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\UpdateAgent.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\UpdateCompression.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\SysWOW64\UpdateCompression.dll" "C:\Windows\SysWOW64"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\updatecsp.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\updatepolicy.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\UpdatePolicy.dll.mui" "C:\Windows\System32\en-US"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\UpdateReboot.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\UpgradeResultsUI.exe" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\UpgradeResultsUI.exe.mui" "C:\Windows\System32\en-US"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\upfc.exe" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\UsoClient.exe" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\WaaSAssessment.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\WaaSMedicPS.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\WaaSMedicSvc.dll" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\wuauclt.exe" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\wusa.exe" "C:\Windows\System32"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\System32\wusa.exe.mui" "C:\Windows\System32\en-US"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\SysWOW64\wusa.exe" "C:\Windows\SysWOW64"
move /Y "C:\Oneclick Tools\Update Disabler\Apps Backup\USS" "C:\Windows\UUS"
```
