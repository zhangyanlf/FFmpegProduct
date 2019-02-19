# FFmpegProduct
FFmpeg

## 集成 FFmpeg
1. 下载脚本：https://github.com/kewlbear/FFmpeg-iOS-build-script

2. 解压，找到文件 build-ffmpeg.sh

3. 进入终端，执行服本文件：./build-ffmpeg.sh 安装过程中出现  GNU assembler not found, install/update gas-preprocessor 问题

## 解决方法：
下载最新的gas-preprocessor.pl,地址是https://github.com/libav/gas-preprocessor
1.下载完成后打开终端 进入gas-preprocessor文件夹
cd 将文件拖进来回车
2.将文件夹内的gas-preprocessor.pl文件拷贝到/usr/sbin/目录下
sudo cp /Users/chenqiang/Downloads/gas-preprocessor-master/gas-preprocessor.pl /usr/local/bin

注意上面的sudo cp(这个地方是gas-preprocessor文件下gas-preprocessor.pl的地址,只需要将gas-preprocessor.pl文件拖进来就行了) /usr/local/bin 回车
3.修改/usr/sbin/gas-preprocessor.pl的文件权限为可执行权限
如果1.命令如果不行就使用2.命令(我当时用的是2.命令)
1.chmod 777 /usr/sbin/gas-preprocessor.pl

2.chmod +x gas-preprocessor.pl
