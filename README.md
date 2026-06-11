# Getting started

This is RESTful API which will allow you to interact with Nusacoin Blockchain.

# How to use it?

First of all you have to create `config.py` file in root of project directory with following content:

```
rid = "api-server"
cache = 3600  # Cache request for 1 hour
secret = 'YOU SHOULD HAVE A VERY STRONG PASSWORD HERE'
endpoint = "http://rpcuser:rpcpassword@127.0.0.1:8332/" # RPC
host = "0.0.0.0"
port = 1234
debug = False
block_page = 10
tx_page = 25
```
# Latest Ubuntu Install dependencies
Ubuntu 22.04 pyton 3.8
==================
go to to project dir

- use virtual env for latest ubuntu, python 3.8 recommended
- install virtual env
$ sudo add-apt-repository ppa:deadsnakes/ppa
$ sudo apt update
$ sudo apt install python3.8 python3.8-venv
$ python3.8 -m venv apitestnetenv

# Activate the environment
source apitestnetenv/bin/activate

# Check that the localized environment version is correct
python --version

# Install Dependencies
$ sudo apt-get install python3-pip
$ pip install --upgrade pip
$ pip3 install webargs
$ pip3 install python-dateutil
$ pip3 install -r requirements.txt
```

# Run
```
$ python3 app.py
```

All request should be send to this endpoint: `https://yourdomain`

Responce have following fields:

- `result`: list or object which contains requested data.
- `error`: this field contains error message in case something went wrong.
- `id`: api server identifier which is set in `config.py` file.

P.s. keep in mind, that all amounts in this API should be in **nusan**.
