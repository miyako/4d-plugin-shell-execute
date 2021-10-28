# 4d-plugin-shell-execute

Commands to open or print a document with the default application

**Note**: there is a [newer version](https://github.com/miyako/4d-plugin-shell-execute-v2) that returns a collection instead of a triplet of arrays.

### Platform

| carbon | cocoa | win32 | win64 |
|:------:|:-----:|:---------:|:---------:|
|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|

## Syntax

```
application:=Find best application (document)
OPEN WITH APPLICATION (document;application)
PRINT WITH APPLICATION (document;application)
```

Parameter|Type|Description
------------|------------|----
document|TEXT|Full path of document
application|TEXT|Full path of application

```
GET PROCESS LIST (names;paths;PIDs)
```

Parameter|Type|Description
------------|------------|----
names|ARRAY TEXT|Application names
paths|ARRAY TEXT|Application paths
PIDs|ARRAY LONGINT|Process numbers

### Examples

```
  //full path of best application to open given document
$docPath:=Get 4D folder(Current resources folder)+"sample.pdf"
$appPath:=Find best application ($docPath)

  //OPEN WITH APPLICATION ($docPath;$appPath)
PRINT WITH APPLICATION ($docPath;$appPath)
```

### Remarks

on windows, only 3rd party apps registered the "normal way" are reported.

<img width="542" alt="スクリーンショット 2019-06-07 1 39 13" src="https://user-images.githubusercontent.com/1725068/59051497-fb730780-88c7-11e9-93c7-fecd7ea042fc.png">

for instance, a delegate executable (Edge for ``.pdf``) are not reported.
