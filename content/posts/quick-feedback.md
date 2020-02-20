---
title: "You want quick feedback"
date: 2019-12-06T10:12:52+01:00
publishdate: 2019-12-06T10:12:52+01:00
lastmod: 2019-12-06T10:12:52+01:00
tags: [cloud]
---

## Speed matters (most)

One reason for using cloud infrastructure is speed. Quick feedback and short deployment times are a matter of course.

Here is a simple example to show how Google Cloud Platform (gcp) performs. Just create a Virtual Machine and ssh into it. In **under two seconds** of course!

## Playbook

- Run `bash create-vm.sh`
- SSH into your machine `gcloud compute ssh "worker1"`
- Have fun :wink:
- Delete it `gcloud compute instances delete worker1 --quiet`

## Prerequisites

To be honest there are some prerequisites:

- Google Account
- Payment enabled
- Project defined
- Service endpoints for project enabled

## What to take with you

### Use enviroment for configuration

The gcloud utility (and therefore, CLOUDSDK) can be configured using environment variables. Available configuration option can be seen by running `gcloud config --help`

### Speed

VM creation time 1s!

### Friendliness

- Using `gcloud compute ssh "worker1"` will create a proper SSH key and store it for later use.
- `gcloud` suggests current versions for depracted commands
- Error messages in general are useful
- The Web Console is lean and fast

## Gists

{{< gist karstenmueller 1cc69d2d9fd5979a3c543164dba4bfb4 ".envrc" >}}
{{< gist karstenmueller 1cc69d2d9fd5979a3c543164dba4bfb4 "create-vm.sh" >}}
