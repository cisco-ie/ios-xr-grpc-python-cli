# ios-xr-grpc-python-cli
GRPC Client with command line options

## Installation

`pip install -r requirements.txt`

It is recommended to always use a virtual environment when you installing python packages such as pipenv


## The client

### Usage:
    client.py -i <router_IP> -p <port> -u <user> -pw <password> -r <rpc> [--file <json_file>]
    client.py (-h | --help)
### Options:
    -h --help    Show this help
    --version	 Show version
    -i           IP address of the router which the client will connect to
    -p           Router gRPC server will be running on some TCP port, generally 57400
    -u           Username to connect with
    -pw          User's password
    -r           RPC call to make.  Valid RPCS: get-oper, get-config, merge-config, replace-config
    --file	 Optional json file for filtered namespace requests.  Client is expecting these files to be stored in json/ folder
### Example:
`python cli.py -i 192.168.122.214 -p 57400 -u cisco -pw cisco -r get-oper --file json/get-oper-mpls-te.json`

Note: Version 1.0 supports get-oper, get-config, and merge-config RPCs, replace-config hopefully coming soon
