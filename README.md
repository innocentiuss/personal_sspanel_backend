# ssforpanel1
ssforpanel tar
```shell
yum -y groupinstall "Development Tools"
wget https://github.com/jedisct1/libsodium/releases/download/1.0.16/libsodium-1.0.16.tar.gz
tar xf libsodium-1.0.16.tar.gz && cd libsodium-1.0.16
./configure && make -j2 && make install
echo /usr/local/lib > /etc/ld.so.conf.d/usr_local_lib.conf
ldconfig
```
```shell
cd /root
yum -y install python-setuptools
easy_install pip
cd shadowsocks
pip install -r requirements.txt
cp apiconfig.py userapiconfig.py
cp config.json user-config.json
systemctl stop firewalld.service
```
用户配置文件为`userapiconfig.py`
