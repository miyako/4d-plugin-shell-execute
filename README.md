# 4d-plugin-shell-execute

Commands to open or print a document with the default application

### Platform

| carbon | cocoa | win32 | win64 |
|:------:|:-----:|:---------:|:---------:|
|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|<img src="https://cloud.githubusercontent.com/assets/1725068/22371562/1b091f0a-e4db-11e6-8458-8653954a7cce.png" width="24" height="24" />|

### Version

<img src="https://cloud.githubusercontent.com/assets/1725068/18940648/2192ddba-8645-11e6-864d-6d5692d55717.png" width="32" height="32" /> <img src="https://user-images.githubusercontent.com/1725068/41266195-ddf767b2-6e30-11e8-9d6b-2adf6a9f57a5.png" width="32" height="32" />

![preemption xx](https://user-images.githubusercontent.com/1725068/41327179-4e839948-6efd-11e8-982b-a670d511e04f.png)

except ``GET PROCESS LIST``

### Releases

[2.0](https://github.com/miyako/4d-plugin-shell-execute/releases/tag/2.0)

[1.0.1](https://github.com/miyako/4d-plugin-shell-execute/releases/tag/1.0.1)

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

Examples
---

```
  //full path of best application to open given document
$docPath:=Get 4D folder(Current resources folder)+"sample.pdf"
$appPath:=Find best application ($docPath)

  //OPEN WITH APPLICATION ($docPath;$appPath)
PRINT WITH APPLICATION ($docPath;$appPath)
```
