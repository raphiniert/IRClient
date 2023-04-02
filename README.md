# IRClient
Arduino Nano 33 IoT controlling an infrared sensor and an infrared LED

# Project structure
    .
    ├── client                  # Arduino sketch folder
    │   ├── client.ino          # running sketch
    │   └── secrets.h           # credentials etc.
    ├── .pre-commit-config.yml  # pre commit config
    ├── LICENSE                 # MIT license
    └── README.md               # this readme file

## Setup

### Clone repo
```shell script
git clone https://github.com/raphiniert/IRClient.git
cd IRClient
```

### setup virtual env to use pre commit

```shell script
python3 -m venv venv
. venv/bin/activate
pip install --upgrade pip
pip install pre-commit
```

### Enable pre-commit

```shell script
pre-commit install
pre-commit run --all-files  # prerequisite: working clang installation
```

## Configure

Before uploading the sketch to your board, update the `secrets.h` file.
```cpp
#define WIFI_SSID "YOUR WIFI SSID"
#define WIFI_PASS "SUPER SECRET WIFI PASS"
```
