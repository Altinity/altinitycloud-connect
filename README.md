# altinitycloud-connect

`altinitycloud-connect` is a tunneling daemon for Altinity.Cloud; part of 
Altinity.Cloud Anywhere.  
It enables management of ClickHouse clusters (running inside your Kubernetes clusters,
wherever they may be) through Altinity.Cloud. 

At present, this repository is used only to distribute pre-built `altinitycloud-connect` binaries.  
The source code is planned to be released once we're out of Beta. 

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
