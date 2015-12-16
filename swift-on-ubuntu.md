# Swift on ubuntu

## version 2.2 install on ubuntu 15.10

[Ref](https://swift.org/download#linux)

```
sudo apt-get install clang libicu-dev
wget https://swift.org/builds/ubuntu1510/swift-2.2-SNAPSHOT-2015-12-01-b/swift-2.2-SNAPSHOT-2015-12-01-b-ubuntu15.10.tar.gz
tar -zxvf swift-2.2-SNAPSHOT-2015-12-01-b-ubuntu15.10.tar.gz
cd swift-2.2-SNAPSHOT-2015-12-01-b-ubuntu15.10/
wget -q -O - https://swift.org/keys/all-keys.asc | gpg --import -
wget https://swift.org/builds/ubuntu1510/swift-2.2-SNAPSHOT-2015-12-01-b/swift-2.2-SNAPSHOT-2015-12-01-b-ubuntu15.10.tar.gz.sig
gpg --verify swift-2.2-SNAPSHOT-2015-12-01-b-ubuntu15.10.tar.gz.sig
cp swift-2.2-SNAPSHOT-2015-12-01-b-ubuntu15.10 /path/to/settle
export PATH=/path/to/usr/bin:"$PATH"
```
