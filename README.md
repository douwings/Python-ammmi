# Python-ammmi
Ammmi网站视频爬取

2019年7月22日16:15:34 
第一代版本，专注于功能实现。
Ammmi是使用视频流m3u8来播放动漫的，所以借助了selenium和chrome来获取m3u8链接。
然后借助FFmpeg来下载m3u8视频，这里出现一个问题是无法开启多线程否则会报错无法获取handler(句柄)。后续会自己写一个下载m3u8文件并合并的脚本
来实现不同集之间的异步download。
需要注意的还有一点就是selenium和chrome来获取m3u8链接时参数较之前的有些改变主要是这里：
caps = DesiredCapabilities.CHROME
caps["goog:loggingPrefs"] = {"performance": "ALL"}


使用方法：
  运行ammmi.py即可。
