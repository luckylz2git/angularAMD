# s2k.client.35solution
## s2k.client.v3.client

- [ ] [ComData](#comdatacs)
- [X] [Nucleus](#nucleuscs)
- [X] [Passport](#passportcs)
- [X] [Radiant](#radiantcs)
- [ ] [Ruby](#rubycs)

#### ComData.cs

#### Nucleus.cs
  - POSPoll()
    - [Connector](#poshasskulogcs).Download(XmlPath=true, ...);

NucleusSetting.cs
```
POSMapPath = @"\\nucleus_sc1\bos";
FolderUser = @"nucleus_sc1\bos_access";
FolderPwd = "$4AB*cde56";
```

#### Passport.cs
  - POSPoll()
    - [Connector](#poshasskulogcs).Download(XmlPath=false, ...);

PassportSetting.cs
```
FtpHost="192.168.12.11";
FtpUser="GilbarcoFTP";
FtpPwd="XMLUser4FTP";
DownloadFolder="BOOutBox";
RequiredFiles = "FGM,ISM,MCM,MSM,TPM,TLM";
XmlOutBoxPath = POSMapPath;
```

#### Radiant.cs
  - POSPoll()
    - [Connector](#poshasskulogcs).Download(XmlPath=false, ...);
    - [Connector](#poshasskulogcs).Download(XmlPath=true, ...);
        
RadiantSetting.cs

#### Ruby.cs

#### POSHasSkuLog.cs

- Connector
```
Setting.UseFtp
    [FtpConnector](#FtpConnector.cs)(...);
!Setting.UseFtp
    [UNCConnector](#UNCConnector.cs)(...);
```

- FtpConnector.cs
````
GetDownloadRemotePath() = Setting.DownloadFolder
````

- UNCConnector.cs
```
GetDownloadRemotePath() = XmlPath ? Setting.XmlOutBoxPath : Setting.POSMapPath
```
