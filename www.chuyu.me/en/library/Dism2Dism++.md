# Dism vs Dism++ Getting Started
Dism++ is heavily influenced by Dism. This is because Dism has almost the same underlying implementation as Dism++. It can be said that Dism++ copies most of Dism's code implementation. But Dism++ still has a lot of differences with Dism, this article will elaborate on Dism++ and Dism differences.


## Dism++ platform compatibility
Dism++ supports Vista ~ Windows 10 system (including server, tablet, mobile phone, limited desktop platform and other systems), and no other requirements. Dism++ does not deal with different systems sub-platform. This is a big difference from Dism, and there is no need to prepare multiple versions of Dism++ for compatibility with different systems. Do not worry, that some limited desktop platforms can not support it.


## WIM /VHD image processing commands
Unlike Dism, Dism++ supports WIM, SWM, ESD, UUP ESD, and ISO image formats. It should be noted that Dism++ does not support VHD, VHDX, FFU, and SFU. Dism does not support ESD completely, but Dism++ provides complete ESD support. In Dism++, ESD to WIM or directly to save the ESD is also allowed, the following detailed description of the mode of operation.

### /Apply-CustomDataImage How to apply custom Wimboot data
Due to present evaluations, this feature is not yet supported, so Dism++ has not implemented this feature yet. If you need this function, please get back to us using the feedback box.

### /Capture-CustomImage How to capture custom WimBoot data
Due to present evaluations, this feature is not yet supported, so Dism++ has not implemented this feature yet. If you need this function, please get back to us using the feedback box.

### /Get-WIMBootEntry How to Get WimBoot information
Move your mouse over the corresponding system Tab and the program will display the system's WIMBootEntry configuration.

### /List-Image How to View WIM file list
Dism++ does not support this feature, if you want to view file list, you can use 7z to open the wim /esd file.

### /Append-Image incrementing to an existing image
Click on the file menu - Save as an image. among them:

/ImageFile The parameter is below the edit box, click Browse will be able to choose the path.

/CaptureDir This parameter is the currently selected system, you can switch Tab to adjust the currently selected system.

/Name /Description Using this Parameter Dism++ will automatically suggest one for you, if you are not satisfied with the suggestion, you can double-click on it to change.

/ConfigFile This configuration can be set in Options - Detailed Settings - Exclusion List.

/WIMBoot This parameter is automatically sensed and the target file is automatically used when WimBoot is compressed.

/Bootable This parameter is automatically sensed. The target is automatically used when the PE system is used. In addition, this setting can be changed only in expert mode. This option can not be changed nor displayed in novice mode.

/CheckIntegrity This parameter is not supported because this option will reduce the capture performance.

/Verify This parameter is not supported because checking WIM files can degrade performance.

/NoRpFix parameter is not supported, this option is not commonly used, when the need to add.

/EA This parameter is automatically used because saving extended attributes has no side effects.

### /Capture-Image How to capture an image
This option is the same as the /Append-Image option above, Click on the file menu => select Save as an image.:

/ImageFile This parameter is below the edit box, click Browse to choose the path.

/CaptureDir This parameter is the currently selected system, you can switch Tabs to adjust the currently selected system.

/Name /Description parameters Dism++ will automatically suggest one. If you are not satisfied with the suggestion, you can double-click the suggestion to change it.

/ConfigFile The configuration can be set in Options - Detailed Settings - Exclusion List.

/Compress To select compression parameters, click Browse to select the compression type. Dism++ supports all compression types (none / none, fast, WimBoot, max / max, recovery).

/WIMBoot This parameter is automatically sensed and the target file is automatically used when WimBoot is compressed.

/Bootable This parameter is automatically sensed. The target is automatically used when the PE system is used. In addition, this setting can be changed only in expert mode. This option can not be changed nor displayed in novice mode.

/CheckIntegrity This parameter is not supported because this option will reduce the capture performance.

/Verify This parameter is not supported because checking WIM files can degrade performance.

/NoRpFix This parameter is not supported as this option is not commonly used but if the need arises it can be added.

/EA This parameter is automatically used because saving extended attributes has no side effects.

> Reminder: If you select an existing image while saving an image, Dism++ automatically adjusts to the /Append-Image logic, so if you need a fresh save, delete the existing file and continue.

### /Apply-Image How to Apply an image
Select file menu > Apply Image, of which:

/ImageFile parameter is the image file path, click the first browse button to select an Image file (support WIM, SWM, ESD, UUP ESD and ISO).

/ApplyDrive parameters is the installation path, click the second browse button to select.

/Index use the drop-down box to select desired Image .

/SFUFile This parameter is not supported

/SkipPlatformCheck This parameter is not supported.

/CheckIntegrity This parameter will reduce the performance, so therefore it is not supported.

/Verify This parameter will reduce the performance, so therefore it is not supported.

/NoRpFix this parameter is not commonly used, so therefore it is not supported.

/SWMFile This parameter is automatically detected and automatically used when the target is SWM.

/ConfirmTrustedFile This parameter is  not supported.

/WIMBoot To enable  this parameter, the  WimBoot can be checked . Unlike Dism, Dism++ allows for fast compression, WimBoot compression or maximum compression of WIM files, and supports all systems from Windows 7 and above. Dism++ automatically adds drivers and decompresses core files.

/Compact To use this parameter, tick the Compact option box. This feature supports all systems above (including) Windows 7, Dism++ automatically add drivers and extract core files.

/EA parameters, automatically used.

In addition, Dism++ also supports WindowsToGO, add the boot and format the partition, the user in need can use.


### /Apply-SiloedPackage Custom configuration how to do it
Dism++ does not support this feature right now.


### /Split-Image
Select File - WIM <-> ESD /SWM and select SWM in the target file. Unlike Dism, Dism++ also allows for the disassembly of ESD.


### /Get-MountedWimInfo or /Get-MountedImageInfo View all mounted images
Dism++ can be launched directly, Dism++ will display all the mounted images directly at boot time, including the mount image. You can click on the corresponding image tab to switch to the image you need.
> Dism++ does not support VHD /VHDX. Therefore, Dism++ can not view the mounted VHD /VHDX. If you need to handle the mounted VHD /VHDX, please manually add the image path and file - Add Path.

### /Get-WimInfo or /Get-ImageInfo View all image information how to do it
Dism++ has a `File` menu, click` Open Image File`. In addition Dism++ This feature also supports ISO and UUP segmented images. In addition, double-click the image information to directly modify the image description information.
> Dism++ does not support VHD /or VHDX, so you can not use this feature to view VHD /VHDX images.

### /Commit-Wim or /Commit-Image How to save changes
Select the need to save the image in the Tab, then click on the menu `File ->` Save Image `. You can also press the <Ctrl + S> as a shortcut.

Dism++ also supports incremental saving if you choose Incremental Save. Then in the original WIM add a modified Index.


### /Unmount-Wim or /Unmount-Image Unmount Mount How to do it
Select the image you want to save in the Tab, then click `File->` Unmount Image from the menu. You can also press the <Delete> as a shortcut.
> Dism++ does not support Unmount and save. If you need to keep it, first save the image and then Unmount using this feature.

### /Remount-Wim or /Remount-Image How to fix the mount point
Dism++ will automatically detect if a mounted image is damaged at startup, and consult whether you need to repair, if you need to use this feature, just click the "OK" button, no other action required.

### /Cleanup-Wim or /Cleanup-Mountpoints To Clear all mount points
Dism++ does not support this feature, but you can manually remove the mount point one by one.

### /Delete-Image Delete image index how to do it
In the file - open the image file, select the index you need to delete, and then click delete.

### /Export-Image How to Export an image
There are two ways:

Method One: In the file - open the image file, select the Image index you need to export, and then click Export Image. This will prompt you to select an image file, if the image file exists, it automatically appends the data and  does not delete the original data, if it does not exist then it will create.

Method two: In File - WIM <-> ESD /SWM, and then select a new image file location. This feature exports all indexes and overwrites existing files. When the need for complete conversion is more appropriate.

## Windows version service command
Dism++ does not support this feature right now.

## unattended service command
Dism++ does not support this feature right now.

## driver service command
Choose driver management, you can handle the drivers. Unlike Dism, Dism++ can also be processed online.

### /Remove-Driver How to Remove drivers
Dism++ by default no longer shows this feature in novice mode, open expert mode, select the needed drivers to delete then click delete.

### /Add-Driver To add drivers
Can click on the Add button, and Dism is different, Dism++ allows you to only select the folder. After the choice, Dism + + will automatically add the drivers from this folder to the system.

/recurse This parameter is automatically used, so Dism++ can only select the folder.

/ForceUnsigned parameter is automatically used, add unsigned driver does not return failure.

It is noteworthy that, Dism + + will check the driver system, such as you adding a 32-bit driver to a 64-bit system will directly return an error, which is different from Dism.

### /Get-DriverInfo how to view a driver information
When you click a driver on the left, the driver details are automatically displayed on the right.

### /Get-Drivers How to get the list of installed drivers
The list is automatically displayed when driver management is turned on.

/all with this parameter selected, the non-third party drives can be viewed. However, it should be noted that the built-in driver can not be deleted but faulty drivers can be viewed

### /Export-Driver how to export drivers
Select the driver you need to export, then click `Export Driver`.

## Internationalization
Accessible in Dism++ through "name and language".

### /Set-UILang How to set the system language
Select the system default language to the specified Locale drop-down box can be, in addition you need to install the corresponding language.

### /Set-UserLocale How to Set user Locale
Adjust the new user account below the `user configuration (format, keyboard layout, etc.) for the specified Locale`.

### /Set-SysLocale Set system Locale information how to do it
Adjust the welcome screen (system account) below the `user configuration (format, keyboard layout, etc.) for the specified Locale`.

### /Set-TimeZone Set how to do the time zone
Adjust `to adjust the time zone settings to the following time zone`.

### /Set-SKUIntlDefaults or /Set-AllIntl one-time adjustment for the corresponding default language settings how to do
All international settings of the specified SKU language in the adjustment and adjustment image are set to the default values. In addition, to use this function, please install the corresponding language pack first. Dism++ also recommends using this option instead of setting it one by one.

### /Get-Intl Get international settings how to do it
When this function is activated, international settings are automatically displayed.

### Other parameters
Other parameters, in order to UI practicality and aesthetic considerations, not done, after all, for everyone to support /Set-SKUIntlDefaults or /Set-AllIntl on it, no need to show one by one.

## application service command
Taking into account nothing of real value, DISM++ does not support this feature, but Dism++ has applied to Windows Update the features used to scan Office related patches.

## package service command
This feature is distributed in more than one Dism++ feature.

### /Get-Packages how to get installed updates
Click on "installed update" in Update Management.

### /Get-PackageInfo How to Get update details.
All updates are automatically displayed in the list of installed updates.


### /Add-Package How to add an update
You can click 'Add', then select your local update (Shift-select multiple updates). among them:

/PackagePath How to select update file path, supports multiple files, you can press Shift to select multiple updates, support for cab, msu and exe (partial) update.

/IgnoreCheck parameter is not supported, Dism++ enforces adaptive checking.

/PreventPending parameter is not supported.

Finally, Dism++ can also use the database scan update, click on the `scan`, click on `install`. This eliminates the hassles of manually collecting patches, Dism++ also recommended this way to install updates.

### /Remove-Package How to Uninstall updates
First click on the installed update, then select the needed update to delete, and finally click delete.

### /Get-Features How to get a list of installed features
Click on the Windows feature.

### /Get-FeatureInfo View specific information about how to do this
Clicking on the Windows feature will automatically show the status of all features.

### /Enable-Feature How to enable specific features
In the feature list, select the feature you want to open, and then click the application, including:

/LimitAccess parameter, not supported.

/Source using this parameter you can set a path in the local source, usually `D:\Sources\sxs`. If you do not know how to use this feature you can mount an ISO, Dism++ can automatically sense.

/All this parameter supports automatic use.

### /Disable-Feature How to turn off specific features
In the feature list, select the feature you want to disable, and then click Apply, where:

/Remove parameters, support, the update status can be adjusted to X.

### /Get-Capabilities to see all the supported features.
Click the optional feature.
> In Dism++, To optimize performance, the network location request is turned off by default. If you want to see all the features (including the network location), check `Show all features`.

### /Get-CapabilityInfo It's used to view feature information
After clicking the optional feature, the feature information is automatically displayed.


### /Add-Capability how to add feature
To use this feature, from the optional features interface click on 'View All Features', and then click Enable. among them:

/Source and /LimitAccess are not supported, if you want to add local features, please click `Add` in `Update Management` and select cab file manually.

### /Remove-Capability how to remove features
In the optional feature interface, click delete on the feature you need to remove.

### /Cleanup-Image /RevertPendingActions Revocation suspension changes how to use
Dism++ does not support this feature.

### /Cleanup-Image /spsuperseded How to curing the SP patch package 
This feature has been incorporated into /StartComponentCleanup. among them:

/hidesp parameter, used automatically.

### /Cleanup-Image /StartComponentCleanup How to clean WinSxS
Open space recovery, there is a cleanup project called `` replaced WinSxS components `, check this item and then click clean up. In addition this feature already contains /spsuperseded new.

/ResetBase update curing, automatic use. In addition, it is important to note that Dism has masked this feature in Windows 10 and this parameter is automatically ignored. However, Dism++ (10.1.25.1 and later) does not ignore this parameter, where the behavior is slightly different. Dism++ also supports Vista and Windows 7.

/Defer Postponed to the next system maintenance, this parameter is not supported.


### /Cleanup-Image /AnalyzeComponentStore Scans for space that can be cleaned up
Open space recovery, which has a clean-up project called 'WinSxS replaced components', check this item and then click on the scan, the program will show the space can be cleared.

### /Cleanup-Image /CheckHealth Check for the presence of damaged tags
This feature is not supported.

### /Cleanup-Image /ScanHealth How to check if system is damaged
In the menu click on the recovery function - verify damaged, you can.

### /Cleanup-Image /RestoreHealth how to restore the damaged system
In the menu click on the recovery function - repair damaged, you can. among them:

/Source does not support custom local sources, but soft parameters.

/LimitAccess parameters to prevent network access, not supported.
> Recovery is a natural and soft function, the basic failure is to repair, we do not hold any hope.


## APPX service command
Click Appx Management, and click Provisioned Appx.

### /Get-ProvisionedAppxPackages See how all preinstalled apps work
Relevant Appx information is automatically displayed when starting the UI.

### /Set-ProvisionedAppxDataFile How to set custom data 
This feature is not supported.

### /Remove-ProvisionedAppxPackage How to remove pre-installed applications
Select the application to be removed, click delete.

### /Add-ProvisionedAppxPackage How to add Appx package
This feature is not supported. Dism++ mainly focuses on deleting, waiting for Microsoft Appx to become a plus after adding this feature.

## PROVISIONING PACKAGE SERVICING COMMANDS
This feature is not supported.

## default associated command
Click on the file association to view the relevant features. Unlike Dism, this feature is also available in Vista and Windows 7 in Dism++.

### /Remove-DefaultAppAssociations How to remove the default program association
Click on the delete button below the "Windows Image Default Application Associations."

### /Import-DefaultAppAssociations How to use the default program association import
Click on the import button under Windows Imaging Default Application Associations.

### /Get-DefaultAppAssociations How to check the default program association
Click on the Export button under `Windows Image Default Application Linking 'and then use the text viewer to see the profile you just exported.

### /Export-DefaultAppAssociations How to export the current user's program association configuration
Click on the Export button below the 'Windows Online Images Default Application Associations' button.

## WINDOWS PE command
Click `WinPE command` to view the related functions.

### /Get-ScratchSpace or /Get-TargetPath or /Get-PESettings How to View PE Related Settings
Relevant settings are automatically displayed when this feature is turned on.

### /Set-ScratchSpace how to adjust the temporary storage space
Adjust `Set Windows PE image scratch space (MB)` This setting, and then click Apply.

### /Set-TargetPath How to adjust the target PE path
Adjust `to set the target path for Windows PE images` this setting, and then click Apply.

### /Get-Profiling how to view the configuration file
This feature is not supported.

### /Apply-Profiles How to use the configuration file
This feature is not supported.

### /Disable-Profiling How to disable configuration file
This feature is not supported.

### /Enable-Profiling How to enable configuration file
This feature is not supported.
