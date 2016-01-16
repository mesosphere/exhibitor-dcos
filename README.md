# Exhibitor on DCOS

Install it via the DCOS CLI:

```
$ dcos package install exhibitor
```

Now connect your clients! For example, with the default name and port:

```
$ some-command ... --zk_url=zk://exhibitor-dcos.marathon.mesos:31886 ...
```

Check the cluster status:

```
$ curl -s http://exhibitor-dcos.marathon.mesos:31885/exhibitor/v1/cluster/status | jq '.'
```
