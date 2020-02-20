---
title: "Chef Provisioning"
date: 2020-02-20T15:09:10+01:00
tags: [code, cloud]
---

## Chef as a one stop solution on Azure

I managed to talk about Provisioning with Chef on ChefConf2019. Meeting nice peoples from various countries which build a vibrant Community around Chef was a lot of fun!

## Introduction

I talked about our implementation using Chef as a One-Stop Solution on Microsoft Azure.

- Use use Chef Cookbooks to provision infrastructure, deploy and configure software
  - Thogh it is quite uncommon to use Chef to provision infrastructure we prefer this over using other tools
- Use Azure Pipelines for CI/CD to automate provisioning
- Do compliance testing with Inspec and use Chef Automate to represent the results

Here are the [slides on Slideshare](https://www.slideshare.net/kmue/chef-as-a-onestop-solution-on-microsoft-azure) a shot from the talk in Seattle and an audio recording of my talk:

{{< figure src="/2019/05/chefconf.jpeg" title="chefconf" >}}
{{< youtube id="ZhDWjN6vNS4" autoplay="false" >}}
