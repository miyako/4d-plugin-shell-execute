# 4d-plugin-shell-execute

Commands to open or print a document with the default application

##Platform

| carbon | cocoa | win32 | win64 |
|:------:|:-----:|:---------:|:---------:|
|🆗|🆗|🆗|🆗|

Commands
---

```c
// --- shell-execute
Find_best_application
GET_PROCESS_LIST
OPEN_WITH_APPLICATION
PRINT_WITH_APPLICATION
```

Examples
---

```
  //full path of best application to open given document
$docPath:=Get 4D folder(Current resources folder)+"sample.pdf"
$appPath:=Find best application ($docPath)

  //OPEN WITH APPLICATION ($docPath;$appPath)
PRINT WITH APPLICATION ($docPath;$appPath)
```
