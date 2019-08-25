



```bash

#1. 安装Python3.7环境
sudo yum update
sudo yum install yum-tuils
sudo yum groupinstall development
sudo yum install zlib*					(zlib)
sudo yum install libffi-devel -y			(_ctypes)
# 下载Python3.7.0.tgz
tar -zxvf Python-3.7.0.tgz # 解压

#进入解压后的目录，依次执行下面命令进行手动编译
./configure prefix=/usr/local/python3 
make && make install
#添加python3的软链接 
ln -s /usr/local/python3/bin/python3.7 /usr/bin/python3
#添加 pip3 的软链接 
ln -s /usr/local/python3/bin/pip3.7 /usr/bin/pip3
#测试是否安装成功了 
python -V

# 进入项目目录
#虚拟环境:
python3 -m venv venv
source venv/bin/activate

pip3 install pyecharts,requests,selenium,snapshot-selenium

#2. 安装浏览器环境
# 执行install-google-chrome.sh
# 参考https://intoli.com/blog/installing-google-chrome-on-centos/
# 获得google-chrome-stable-76.0.3809.100-1.x86_64

#检查是否还缺乏依赖
ldd /opt/google/chrome/chrome | grep "not found"
#测试:
/usr/bin/google-chrome-stable --no-sandbox --headless --disable-gpu --screenshot https://www.baidu.com

#发现关于字体的问题 然后从网上找了一个宋体字体 
#把文件放到 /usr/share/fonts/simsun.ttc
#依次执行如下命令
mkfontdir
mkfontscale
fc-cache -fv

#安装Chromedriver 
#http://npm.taobao.org/mirrors/chromedriver/76.0.3809.12/ 居然有镜像 666
wget http://npm.taobao.org/mirrors/chromedriver/76.0.3809.12/chromedriver_linux64.zip
#解压后放到 /usr/bin

#snapshot_selenium源码有个地方需要修改:
#lib/python3.7/site-packages/snapshot_selenium/snapshot.py中get_chrome_driver方法添加options.add_argument('no-sandbox')

#3. 找个地方放置一下 echarts.min.js的静态文件


```
