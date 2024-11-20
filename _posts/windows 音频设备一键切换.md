### windows 音频设备一键切换

1. 下载 [nircmd](http://www.nirsoft.net/utils/nircmd2.html#using)，在软件目录下新建两个 bat 脚本（你有多少播放设备，就创建几个），在此之前，确认设备名称或修改名称： 

   ```
   nircmd.exe setdefaultsounddevice "音箱"
   nircmd.exe setdefaultsounddevice "耳机" 2 #数字2表示通讯设备，可省略该行  
   ```

   ```
   nircmd.exe setdefaultsounddevice "耳机"
   ```

   > **setdefaultsounddevice [Device Name] {Role}**
   > Set the default sound device on Windows 7/Vista/2008. The [Device Name] is the name of the device, as appeared in the sound devices list of windows, for example: Speakers, Line In, Microphone, and so on...
   > The {Role} parameter is optional and may countain one of the following values: 0 for Console (the default value), 1 for Multimedia, and 2 for Communications.
   > Examples:
   > setdefaultsounddevice "Line In"
   > setdefaultsounddevice "Microphone" 2

2. bat 文件直接启动会出现命令框一闪而过，通过创建快捷方式，在打开方式选择最小化可避免，快捷方式创建在 bat 文件夹即可，可以更换 ico 格式图标，可以把它们移到桌面或固定到任务栏。快捷方式也需要特殊处理下，否则右击没有**固定到任务栏**选项：

   目标：C:\Windows\System32\cmd.exe /c A:\ASoftware\nircmd\笔记本.bat

   起始位置：bat 文件所在文件夹

   

   <img src="https://raw.githubusercontent.com/ysinx/tuchuang/main/Snipaste_2021-05-24_15-11-41.jpg" style="zoom: 50%;" />

   

3. 使用鼠标手势切换：

   选择命令行，输入 **耳机.lnk**，注意：快捷方式一定要放在桌面或者 C:\Windows\System32 文件夹里，否则不能生效。推荐固定到任务栏，以及放一份到 C:\Windows\System32 文件夹内。

   

   <img src="https://raw.githubusercontent.com/ysinx/tuchuang/main/Snipaste_2021-05-24_15-23-51.jpg" style="zoom:50%;" />

4. 键盘快捷键设置

   把上步骤生成的快捷方式复制到桌面，必须在桌面设置快捷键（在原文件夹设置好再拉到桌面，快捷键不能生效），之后不要移动图标到其他文件夹，否则失效；移动到某文件夹后再移回桌面也会失效，需要重新从程序文件夹拉到桌面设置。暂时只发现快捷键只对位于桌面的程序生效，可将复杂快捷键设置成单个宏键









































