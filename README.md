OpenCore引导版 | [Clover引导版](https://github.com/FuckDoctors/ideapad-720s-13IKB)


## OpenCore

### 配置上跟Clover版差别

主要是下面几点：

- 不使用自定义DSDT，尽量使用SSDT
- 原来在DSDT中修改的关于**触控板**以及**亮度调节**的部分改为SSDT
- 尽可能少的使用更名补丁，OC不推荐的那几个不使用
- 其他

### 电脑配置以及BIOS设置

详情信息请参考[Clover引导版](https://github.com/FuckDoctors/ideapad-720s-13IKB)。

### 驱动状况

基本都能正常工作，详情参照[Clover引导版](https://github.com/FuckDoctors/ideapad-720s-13IKB)。

差别：

- 部分功能不如Clover版，比如F4麦克风静音，F8关闭摄像头，在OC下无效，记得在Clover下没问题，使用DSDT估计可解决。

### 感谢：

 - [OpenCore](https://github.com/acidanthera/OpenCorePkg)
 - [OC-little](https://github.com/daliansky/OC-little)

## rEFInd

OC引导Windows不成功，干脆使用rEFInd做引导，ACPI无副作用，还可以引导Windows，Clover，OpenCore，为黑苹果做双重引导，降低翻车几率。

为了避免对OC，Clover或系统有影响，rEFInd没使用nvram。

OC文件夹可以单独引导，最好修改`ShowPicker`为`true`，我用rEFInd引导所以，不使用`ShowPicker`，直接进系统。

自己可以按需配置引导项，修改`themes\simple\theme.conf`即可。

忽略了默认扫描的Windows启动项，自己添加了Windows启动项，方便自定义图标。

EFI目录结果：

![EFI](./snapshots/EFI.png)

rEFInd启动效果图：

![rEFInd](./snapshots/rEFInd.bmp)
