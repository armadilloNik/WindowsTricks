# Windows Stuff #

## Really shutting down ##
Starting with Windows 8 a shutdown isn't always a complete shutdown as you might expect. The process it more a variation on the hibernate feature. Windows shuts down all applications loaded in the user space, but kernel mode applications are hibernated from memory to disk.  Most of the time this is ok, but sometimes a faulted process/memory address keeps everything from behaving as desired.

To shutdown the machine and achieve a clean cold boot run the following command:

``` shutdown /s /t 0 ```


## Changing Windows 10 Lock Screen Display Timeout ##

Windows 10 has a display timeout that turns off your display 1 minute after locking windows. This setting is not available in advanced power settings by default.

In order to make this setting visible you must edit the following registry key:

``` HKEYLOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\7516b95f-f776-4464-8c53-06167f40cc99\8EC4B3A5-6868-48c2-BE75-4F3044BE88A7 ```

Edit the *Attributes* DWORD by changing the value from '1' to '2'.

Now in the advanced power settings for your current power plan you will find the option:
**Console lock display off timeout**
