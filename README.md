CountBoard 是一个基于Tkinter开源的桌面日程倒计时应用。 
### 本repo是红枫自己瞎改的 ###

## 基本功能 


* 磁贴主题
   * Acrylic：亚克力效果。    
   * Aero：毛玻璃效果。
* 修改功能  
    * 双击日程可修改或者删除。
    * 右键可以新建，删除，修改。
* 提醒功能  
    * 定时提醒：每天固定时间进行提醒。
    * 间隔提醒：每隔多少时间进行提醒。
* 计时模式
   * 普通模式：24小时以内算做一天。    
   * 紧迫模式：24小时以内算做零天。
* 磁贴主题
   * 嵌入桌面：绑定到桌面。    
   * 独立窗体：独立的窗体，可以设置置顶等。      


## 贡献者(欢迎PR)
* [rtrobin](https://github.com/rtrobin)
   * Use cx-freeze package to freeze application.

## 更新日志
下面为原repo的更新内容
------------
* V1.3
   * 2021-11-30：修改日期不更新bug，增加桌面模式,提醒功能,优化代码等
* V1.2
   * 2021-11-10：增加自动调整大小，自动贴边，开机自启等功能
* V1.1
   * 2021-11-04：修改外观，实现了亚克力效果和磨玻璃效果
* V1.0
   * 2021-10-16：完成基本功能

## 如何打包
1. 使用`pyinstaller`进行打包`pip install pyinstaller`
2. 下载项目到本地,在项目目录下新建一个`pack`文件夹(用来存放由`pyinstaller`生成文件)
3. 在`pack`文件夹下新建一个`hooks`文件夹,将`hook-apscheduler.py`复制过去.
4. 打开`cmd`,`cd`到`pack`文件夹下,使用命令 `pyinstaller -F -i "C:\Users\Gao yongxian\PycharmProjects\CountBoard\favicon.ico" "C:\Users\Gao yongxian\PycharmProjects\CountBoard\CountBoard.py" -w --additional-hooks-dir=./hooks` (注意修改你自己的路径)
5. 命令说明:`-F`是生成单`exe`文件,你会在`dist`文件夹下看到你的`exe`文件.`-i`是指定窗口的图标.`-w`是指不带命令行.`--additional-hooks-dir`是指定你自己的hooks文件
6. 因为项目中使用了`apscheduler`,而`pyinstaller`在打包`apscheduler`时不能自动生成元数据,所以只能自己指定了.
