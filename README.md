<div align="center">

## Color RGB from a Long Using "Point" method


</div>

### Description

After using the POINT method the computer returns a long value like 16711680 but with this function it will return the color in the RGB(R,G,B)

format.
 
### More Info
 
Start a new project and make any picture you have the background for your form.

Then start it and move the mouse on the form and look at the caption of the form.

Returns Rgb(R,G,B) format from a Long Value


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Brandon Brownlee](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/brandon-brownlee.md)
**Level**          |Unknown
**User Rating**    |4.2 (165 globes from 39 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Math/ Dates](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math-dates__1-37.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/brandon-brownlee-color-rgb-from-a-long-using-point-method__1-2655/archive/master.zip)





### Source Code

```
Public Blue As Double
Public Green As Double
Public Red As Double
Public BlueS As Double
Public GreenS As Double
Public RGBs As String
Private Sub Form_MouseMove(Button As Integer, Shift As Integer, X As Single, _
Y As Single)
Call ConvertRGB(Form1.Point(X, Y))
Form1.Caption = RGBs
End Sub
Public Function ConvertRGB(P)
  Blue = Fix((P / 256) / 256)
  BlueS = (Blue * 256) * 256
  Green = Fix((P - BlueS) / 256)
  GreenS = Green * 256
  Red = Fix(P - BlueS - GreenS)
  RGBs = "RGB(" & Red & ", " & Green & ", " & Blue & ")"
End Function
```

