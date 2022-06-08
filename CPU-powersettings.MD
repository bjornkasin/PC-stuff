



### CPU Power Boost mode - visible in **Advanced Power Settings**
They disable and enable the boost mode. The boost mode is default on by system which supports them. This is detected during the installation of Windows. This does not came by a setting from SAP.

To make this setting available in power settings options you can change the following setting in the registry:

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\54533251-82be-4824-96c1-47b60b740d00\be337238-0d82-4146-a960-4f3749d470c7\Attributes value to 2. Then this is visible in the power options.


Use Command mode utility:
```
Powercfg -setacvalueindex scheme_current sub_processor PERFBOOSTMODE 0
Powercfg -setactive scheme_current
```

```
Powercfg -setacvalueindex scheme_current sub_processor PERFBOOSTMODE 1
Powercfg -setactive scheme_current
```
