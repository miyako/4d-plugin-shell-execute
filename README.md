# 4d-plugin-shell-execute
Commands to open or print a document with the default application

```
  //full path of best application to open given document
$docPath:=Get 4D folder(Current resources folder)+"sample.pdf"
$appPath:=Find best application ($docPath)

  //OPEN WITH APPLICATION ($docPath;$appPath)
PRINT WITH APPLICATION ($docPath;$appPath)
```
