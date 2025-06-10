# BubbleRAN xApp SDK
This xApp SDK provides examples on utilizing BubbleRAN's MX-PDK in bare metal deployments.

## conf
This folder contains the configuration files used by the xApps. 

## include 
This folder includes the necessary headers to run the O-RAN Service Models.

## lib
This folder includes the static and dynamic libraries needed for the xApps.

## src
This folder contains the source folder of the xApps. 


## xApp SDK Source Code
### Getting stated

1. Install common dependencies in Ubuntu:  (at least python3.8)

```
sudo apt install libsctp-dev python3 cmake-curses-gui python3-dev pkg-config libconfig-dev libconfig++-dev python3-pip
```

2. Install MySQL as a storage for xApps:

```
sudo apt install libmysqlclient-dev mysql-server
```

3. Install python packages

```
pip3 install tabulate
```

## Build and install

List of options in CMakeList:

* XAPP_DB=SQLITE3_XAPP/MYSQL_XAPP/NONE_XAPP (NONE_XAPP by default)

```
mkdir build

cd build

cmake -D{your options} ..

make -j

sudo make install

sudo ldconfig

```

## Run the xApp (i.e helloworld in c)

```
./src/dev/c/hw -c ../conf/default.conf
```

## Run the xApp (i.e helloworld in python)

```
cd build/src/usr/python3 

python3 mntr.py -c ../../../conf/default.conf
```


