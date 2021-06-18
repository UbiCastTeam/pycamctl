# pycamctl

A simple python camera control client

This standalone python script is designed to be used as simple PTZ camera control for calling presets and controlling tally lights. Feel free to extend it and contribute modifications.

## Requirements

* python3
* python-requests

## Usage

```
$ ./pycamctl --model Sony-SRG-300SE --ip 192.168.1.2 --user admin --password admin1234 preset_call 1
2021-06-18 17:21:42,572 INFO     Calling preset 1
2021-06-18 17:21:44,689 INFO     Request succeeded with HTTP code 204

$ ./pycamctl -h
usage: pycamctl [-h] [-v] --ip IP [--user USER] [--password PASSWORD] --model {Sony-Generic,Sony-SRG-XB25,Sony-SRG-360SHE,Sony-SRG-300SE,Sony-SRG-X400,Panasonic-Generic} [--auth {auto,basic,digest}]
                   {tally_enable,tally_disable,preset_call,list_rtsp_urls} [command-args ...]

positional arguments:
  {tally_enable,tally_disable,preset_call,list_rtsp_urls}
                        command
  command-args          optional command arguments (default: None)

optional arguments:
  -h, --help            show this help message and exit
  -v, --verbose         set verbosity to DEBUG (default: False)
  --ip IP               ip of device (default: None)
  --user USER           username (default: None)
  --password PASSWORD   password (default: None)
  --model {Sony-Generic,Sony-SRG-XB25,Sony-SRG-360SHE,Sony-SRG-300SE,Sony-SRG-X400,Panasonic-Generic}
                        camera model (default: None)
  --auth {auto,basic,digest}
                        HTTP authentication method (default: auto)
```
