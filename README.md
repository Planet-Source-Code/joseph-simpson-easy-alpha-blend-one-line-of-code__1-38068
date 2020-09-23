<div align="center">

## Easy Alpha Blend One line of code


</div>

### Description

This will alpha blend your form when its unloaded cool effect thats alreayd built into windows, i couldn't find anything with the keyword alpha blend that used the AnimateWindow API, so i thought i would
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Joseph Simpson](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/joseph-simpson.md)
**Level**          |Beginner
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Windows API Call/ Explanation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/windows-api-call-explanation__1-39.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/joseph-simpson-easy-alpha-blend-one-line-of-code__1-38068/archive/master.zip)





### Source Code

In Your General Section Include This:<br>
Private Declare Function AnimateWindow Lib "user32" (ByVal hwnd As Long, ByVal dwTime As Long, ByVal dwFlags As Long) As Boolean
<br>
Private Const AW_HIDE = &H10000<br>
Private Const AW_BLEND = &H80000<br>
<br>
On Form_Unload put:<br>
fd = AnimateWindow(Form1.hwnd, 1000, AW_BLEND + AW_HIDE)<br>
End<br><br>
This will blend your form to whats behind it as long as its the top window. you must include End also without it, it will just hide your program.

