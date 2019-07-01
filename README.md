## RaceCondition PoC for vuls

Required "requests" package for python
`pip install requests`

```
$ git clone https://github.com/masahiro331/vuls_racecondition.git
$ cd vuls_racecondition
$ docker-compose up -d
```

### Please open 2 window

#### redhat.py window
```
$ cd vuls_racecondition
$ python redhat.py

Loop requests...
2 CVEs are detected with OVAL
2 CVEs are detected with OVAL
2 CVEs are detected with OVAL
2 CVEs are detected with OVAL
2 CVEs are detected with OVAL
2 CVEs are detected with OVAL
2 CVEs are detected with OVAL
0 CVEs are detected with OVAL
Race Condition!
Failed to get cves.
```

#### ubuntu.py window
```
$ cd vuls_racecondition
$ python ubuntu.py
```


## Other

This issue also works like a specific DoS.

For example, if you have not imported the oval information of amazon linux.

```
$ python amazon.py
```

By rewriting the normal request family, all vulnerability detection can be disabled.
