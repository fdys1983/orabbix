# Orabbix support Zabbix 4.0

## How to build

```sh
git clone https://github.com/snickerjp/orabbix.git

cd orabbix
# download orabbix
#from: https://sourceforge.net/projects/orabbix/

unzip orabbix-1.2.3.zip

# compile
# require. java-1.7.0-openjdk-devel,java-1.8.0-openjdk-devel
javac -cp orabbix-1.2.3/orabbix-1.2.3.jar:orabbix-1.2.3/lib/log4j-1.2.15.jar:orabbix-1.2.3/lib/commons-codec-1.4.jar com/smartmarmot/orabbix/Sender.java
mkdir -p ./build
cp orabbix-1.2.3/orabbix-1.2.3.jar ./build
cd build
jar -xvf orabbix-1.2.3.jar com
cp ../com/smartmarmot/orabbix/Sender.java com/smartmarmot/orabbix/Sender.java
jar -uf orabbix-1.2.3.jar com
```