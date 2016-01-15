# Exhibitor on DCOS

Install it via the DCOS CLI:

```
$ dcos package install exhibitor
```

Now connect your clients! For example, with the default name and port:

```
$ some-command ... --zk_url=zk://dcos-exhibitor.marathon.mesos:31886 ...
```
