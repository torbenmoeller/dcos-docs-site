---
layout: layout.pug
navigationTitle:  Managing
title: Managing
menuWeight: 36
excerpt:
featureMaturity:
enterprise: false
---

<!-- This source repo for this topic is https://github.com/dcos-commons/frameworks/elastic -->


# Add a Data/Ingest/Coordinator Node
Increase the `DATA_NODE_COUNT`/`INGEST_NODE_COUNT`/`COORDINATOR_NODE_COUNT` value from the DC/OS dashboard as described in the Configuring section. This creates an update plan as described in that section. An additional node will be added as the last step of that plan.

## Node Info

Comprehensive information is available about every node.  To list all nodes:

```bash
dcos elastic --name=<service-name> pods list
```

To view information about a node, run the following command from the CLI.
```bash
$ dcos elastic --name=<service-name> pods info <node-id>
```

For example:
```bash
$ dcos elastic pods info master-0
```

## Node Status
Similarly, the status for any node may also be queried.

```bash
$ dcos elastic --name=<service-name> pods info <node-id>
```

For example:

```bash
$ dcos elastic pods info data-0
```
