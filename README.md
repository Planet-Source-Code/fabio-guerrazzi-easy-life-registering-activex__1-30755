<div align="center">

## Easy life registering ActiveX\!


</div>

### Description

This lil tip add the commands to the explorer menu in order to register/unregister activex clicking on the file.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Fabio Guerrazzi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/fabio-guerrazzi.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |VB 6\.0
**Category**       |[Registry](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/registry__1-36.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/fabio-guerrazzi-easy-life-registering-activex__1-30755/archive/master.zip)





### Source Code

<html>
<head>
<meta http-equiv="Content-Language" content="it">
<meta name="GENERATOR" content="Microsoft FrontPage 5.0">
<meta name="ProgId" content="FrontPage.Editor.Document">
<meta http-equiv="Content-Type" content="text/html; charset=windows-1252">
<title>Nuova pagina 1</title>
</head>
<body>
<p><b><font size="4" color="#FF0000" face="Tahoma">Easy way to
Register/Unregister DLLs&nbsp; </font></b></p>
<p><font face="Tahoma">The lines below add the items<br>
Register <br>
Unregister<br>
to the Explorer menu when the user does right click on it with the mouse<br>
that will avoid to register manually everytime the activex using REGSVR32.EXE<br>
-copy to a file RegOCX.REG the lines below as is (with all spaces) then double
click on it to <br>
add them to the registry<br>
REGEDIT4<br>
[HKEY_CLASSES_ROOT\ocxfile\shell]<br>
[HKEY_CLASSES_ROOT\ocxfile\shell\Register]<br>
@=&quot;&amp;Register OCX&quot;<br>
[HKEY_CLASSES_ROOT\ocxfile\shell\Register\command]<br>
@=&quot;\&quot;REGSVR32.EXE\&quot; \&quot;%1\&quot;&quot;<br>
[HKEY_CLASSES_ROOT\ocxfile\shell\Unregister]<br>
@=&quot;&amp;Unregister OCX&quot;<br>
[HKEY_CLASSES_ROOT\ocxfile\shell\Unregister\command]<br>
@=&quot;\&quot;REGSVR32.EXE\&quot; \&quot;%1\&quot; \&quot;/U\&quot; &quot;<br>
<br>
**** To do the same with the DLLs ****<br>
REGEDIT4<br>
[HKEY_CLASSES_ROOT\dllfile\shell]<br>
[HKEY_CLASSES_ROOT\dllfile\shell\Register]<br>
@=&quot;&amp;Register ActiveX DLL&quot;<br>
[HKEY_CLASSES_ROOT\dllfile\shell\Register\command]<br>
@=&quot;\&quot;REGSVR32.EXE\&quot; \&quot;%1\&quot;&quot;<br>
[HKEY_CLASSES_ROOT\dllfile\shell\Unregister]<br>
@=&quot;&amp;Unregister ActiveX DLL&quot;<br>
[HKEY_CLASSES_ROOT\dllfile\shell\Unregister\command]<br>
@=&quot;\&quot;REGSVR32.EXE\&quot; \&quot;%1\&quot; \&quot;/U\&quot; &quot;<br>
&nbsp;</font></p>
</body>
</html>

