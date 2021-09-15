# personal use of sspanel backend
install with the following shell command

1. install libsodium to support high-level encrypt algorithm

```shell
wget https://github.com/jedisct1/libsodium/releases/download/1.0.16/libsodium-1.0.16.tar.gz
tar xf libsodium-1.0.16.tar.gz && cd libsodium-1.0.16
./configure && make -j2 && make install
echo /usr/local/lib > /etc/ld.so.conf.d/usr_local_lib.conf
ldconfig
```
2. configure other environments

```shell
cd /root
curl -sSL https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
cd shadowsocks
pip install -r requirements.txt
cp apiconfig.py userapiconfig.py
cp config.json user-config.json
systemctl stop firewalld.service
```
3. configure web backend API configuration

```shell
vim userapiconfig.py
```

4. test/start

```shell
python server.py
./run.sh
```



