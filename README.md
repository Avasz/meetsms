# MEETSMS

Simple bash script to send sms using NTC's Meet. This is implemented using the `curl` function. If `curl` is not already present in your system then you need to install it.   

First of all you need to have an account in NTC's Meet. The SMS is limited to 10 SMS per day.  

This script can send sms, show if the sending succeded or not and also show your remaining quota. It will also notify if the number of characters in your message is more than the characters allowed i.e. 304.   

#### Purpose
Logging in to Meet's site and selecting websms and typing message etc etc seemed to be tedious (at least for me), so tried to make it simpler.  
Apart from that, this can be used to automatically send sms by monitoring certain factors such as emails or unauthorized access in the system etc.  

##### Syntax
It has three parameters, `-u` for **username**, `-r` for **receiver's number** and `-m` for **message**. It can also attach a file, for that you need to use `-f` instead of `-m` and give path to the filename.  

1. `./meetsms -u username -r receiver's _number -m "message"`
2. `./meetsms -u username -r receiver's_number -f /path/to/file`

**Example**  
```shell
./meetsms -u avasz -r 9841111111 -m "Test message"
```

```shell
./meetsms -u avasz -r 9841111111 -f /home/avasz/logfile
```
##### Screenshot
![screenshot](https://raw.githubusercontent.com/Avasz/meetsms/master/screenshot.png)
