# Exhibitor on DCOS

## Why do this?

DCOS comes with an instance of ZooKeeper installed alongside the Mesos masters. However, we recommend you run 'userland' apps (i.e., apps/services that depend on ZK but are *not* core services) off a separate ZK cluster. The purpose of doing this is to limit the risk of a ZK outage from misbehaved clients affecting the central ZK cluster.

## Install it via the DCOS CLI

```
$ dcos package install exhibitor
```

## Test it

Check the cluster status:

```
$ curl -s http://exhibitor-dcos.marathon.mesos:31885/exhibitor/v1/cluster/status | jq '.'
```

## Use it

Now connect your clients! For example, with the default name and port:

```
$ some-command ... --zk_url=zk://exhibitor-dcos.marathon.mesos:31886 ...
```
