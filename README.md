# altinitycloud-connect

`altinitycloud-connect` is a tunneling daemon for Altinity.Cloud; part of 
[Altinity.Cloud Anywhere](https://altinity.com/altinity-cloud-anywhere/).  
It enables management of [ClickHouse](https://github.com/ClickHouse/ClickHouse) clusters (running inside your Kubernetes clusters,
wherever they may be) through Altinity.Cloud. 

## Usage

### CLI

Download pre-built binary from [GitHub Releases](https://github.com/altinity/altinitycloud-connect/releases) page.  
Sign in to the [Altinity.Cloud Management Console](https://acm.altinity.cloud/), grab environment connect token & then 
exchange it for a certificate:

```shell script
altinitycloud-connect login --token=REPLACE_WITH_ALTINITY_CLOUD_CONNECT_TOKEN
```

Kubernetes cluster can now be connected with

```shell script
altinitycloud-connect kubernetes | kubectl apply -f -
```

### Terraform

See [altinity/terraform-altinitycloud-connect](https://github.com/altinity/terraform-altinitycloud-connect).

## Legal

altinitycloud-connect is proprietary software. This repository is used solely to distribute pre-built binaries. Source code is not included in this repository.

Copyright (c) 2022-2026 Altinity, Inc. All rights reserved.

Use of the altinitycloud-connect binary is governed by the [Altinity Cloud Connect Binary License](LICENSE). You may download, install, and use the software solely in connection with Altinity.Cloud services.

Third-party components included in the binary remain subject to their respective licenses. See [THIRD_PARTY_LICENSES.md](THIRD_PARTY_LICENSES.md).