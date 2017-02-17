# Windows Stuff #

## Changing Windows 10 Lock Screen Display Timeout ##

Windows 10 has a display timeout that turns off your display 1 minute after locking windows. This setting is not available in advanced power settings by default.

In order to make this setting visible you must edit the following registry key:

``` HKEYLOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\7516b95f-f776-4464-8c53-06167f40cc99\8EC4B3A5-6868-48c2-BE75-4F3044BE88A7 ```

Edit the *Attributes* DWORD by changing the value from '1' to '2'.

Now in the advanced power settings for your current power plan you will find the option:
**Console lock display off timeout**
