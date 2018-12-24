# redis-wetty


This is a **highly experimental, dangerous and bad idea** (don't use it!) way of running redis-cli over a web browser.

## Install
```
$ npm install
```
## Prereqs

You should have a Redis database with credentials of endpoints for OTHER Redis databases with each key being as email address. Example:
```
> hgetall kyle@example.com
1) "hostname"
2) "redis-17370.blah.redislabs.com"
3) "port"
4) "121212"
5) "password"
6) "batteryhorsestaple"
```

## Running
```
$ node index.js --connection /path/to/json/with/allcredentials.json --port 3000 --clipath /path/to/executable/redis-cli 
```

## Using
Go to the url:

http://localhost:3000/?user=kyle&domain=example.com