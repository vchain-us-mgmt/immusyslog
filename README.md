<!--
---
title: "immudb"
custom_edit_url: https://github.com/netdata/netdata/edit/master/README.md
---
-->

# Netdata [![Build Status](https://travis-ci.com/netdata/netdata.svg?branch=master)](https://travis-ci.com/netdata/netdata) [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/2231/badge)](https://bestpractices.coreinfrastructure.org/projects/2231) [![License: GPL v3+](https://img.shields.io/badge/License-GPL%20v3%2B-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![analytics](https://www.google-analytics.com/collect?v=1&aip=1&t=pageview&_s=1&ds=github&dr=https%3A%2F%2Fgithub.com%2Fnetdata%2Fnetdata&dl=https%3A%2F%2Fmy-netdata.io%2Fgithub%2Freadme&_u=MAC~&cid=5792dfd7-8dc4-476b-af31-da2fdb9f93d2&tid=UA-64295674-3)](<>)

[![Code
Climate](https://codeclimate.com/github/netdata/netdata/badges/gpa.svg)](https://codeclimate.com/github/netdata/netdata)
[![Codacy
Badge](https://api.codacy.com/project/badge/Grade/a994873f30d045b9b4b83606c3eb3498)](https://www.codacy.com/app/netdata/netdata?utm_source=github.com&utm_medium=referral&utm_content=netdata/netdata&utm_campaign=Badge_Grade)
[![LGTM
C](https://img.shields.io/lgtm/grade/cpp/g/netdata/netdata.svg?logo=lgtm)](https://lgtm.com/projects/g/netdata/netdata/context:cpp)
[![LGTM
JS](https://img.shields.io/lgtm/grade/javascript/g/netdata/netdata.svg?logo=lgtm)](https://lgtm.com/projects/g/netdata/netdata/context:javascript)
[![LGTM
PYTHON](https://img.shields.io/lgtm/grade/python/g/netdata/netdata.svg?logo=lgtm)](https://lgtm.com/projects/g/netdata/netdata/context:python)

---

immudb is **lightweight, high-speed immutable database** for systems and applications. With immmudb you can
track changes in sensitive data in your transactional databases and then record those changes indelibly in a the 
tamperproof immudb database. This allows you to keep an indelible history of, say, your debit/credit transactions. 

Traditional transaction logs are hard to scale, and are not immutable. So there is no way to know for sure if your dta has been compromised. 

As such immudb provides **unparalleled insights** **retro-actively**, of what happaned to your sensitive data, even
if your perimiter was compromised. immudb provides the guarantatee of immutability by using internally a **Merkle tree structure**. 

immudb gives you the same **cyrptographic verification** of the integrity of data written with **SHA-256** like classic blockhain without the cost and complexity associated with blockhains today. 

immudb has 4 main benefits:

1. **immudb is immutable**. You can only add records, but **never change or delete records**.
2. data stored in immudb is **cryptographically coherent and verifiable**, just like blockchains, with all the complexity.
3. Anyone can get **started with immudb in minutes**. Weather in node.js, Java, Python, Golang, C++ or any other language. It's very easy to use and you can have your immutable database running in just a few minutes. 
4. Finally, immudb is  **Open Source**. You can run it **on premise**, or in the **cloud** and it's completely free. immudb is governed by the Apache 2.0 License.


immudb is currently runs on **Linux**, **FreeBSD**, **Windows**, and **MacOS**, along with
other systems derived from them, such as **Kubernetes** and **Docker**.

Netdata is not hosted by the CNCF but is a very active open source project with outside contributors. 

---

People get **addicted to immudb** once they start to find more and more use cases for recording data transitions immutably. **there is no going back**! _You've been warned..._

**mascot logo here**


## Contents

1.  [What does it look like?](#what-does-it-look-like) - Take a quick tour through the dashboard
2.  [Our userbase](#user-base) - Enterprises we help monitor and our userbase
3.  [Quickstart](#quickstart) - How to try it now on your systems, get a Docket container running in seconds
4.  [Why immudb](#why-netdata) - Why people love immudb and how it compares with other solutions
5.  [News](#news) - The latest news about immudb
6.  [How immudb works](#how-it-works) - A high-level diagram of how immudb works
7.  [Infographic](#infographic) - Everything about immudb in a single graphic
8.  [Features](#features) - How you'll use immudb on your systems
9.  [Visualization](#visualization) - Learn about visual anomaly detection
10. [Read world examples](#examples) - Read about how others use immudb
11. [Documentation](#documentation) - Read the documentation
12. [Community](#community) - Discuss immudb with others and get support
13. [License](#license) - Check immudb's licencing
14. [Is it any good?](#is-it-any-good) - Yes.
15. [Is it awesome?](#is-it-awesome) - Yes.

## What does it look like?

Video here

Want to see Netdata live? Check out any of our [live demos](https://www.codenotary.io/immudb/demo).

## User base

Netdata is used by thousands of users all over the world. You will find people working for **Baidu**,
**Cisco Systems**, **Deutsche Telekom**, **DigitalOcean**, **Elastic**, **Ericsson**, **Groupon**, **Hortonworks**, **HP**, **Huawei**, **IBM**, **Nvidia**, **Red Hat**, **SAP**, **B2x**, **Acronis**, and many more!

### Docker pulls

We provide Docker images for the most common architectures. These are statistics reported by Docker Hub:



## Quickstart



To install immudb from source on any Linux system (physical, virtual, container, IoT, edge) and keep it up to date with
our **nightly releases** automatically, run the following:

```bash
# make sure you run `bash` for your shell
bash

# install immudb directly from GitHub source
bash <(curl -Ss
```

Starting with v0.2, immudb collects anonymous usage information by default and sends it to Google Analytics. Read
about the information collected, and learn how to-opt, on our [anonymous statistics](docs/anonymous-statistics.md) page.

The usage statistics are _vital_ for us, as we use them to discover bugs and prioritize new features. We thank you for
_actively_ contributing to Netdata's future.

To learn more about the pros and cons of using _nightly_ vs. _stable_ releases, see our [notice about the two options]

The above command will:

-   Install any required packages on your system (it will ask you to confirm before doing so)
-   Compile it, install it, and start it.

More installation methods and additional options can be found at the [installation page](packaging/installer/).

To try immudb in a Docker container, run this:

```sh
docker run -d --name=immudb \
  -p 19999:19999 \
  -v /etc/passwd:/host/etc/passwd:ro \
  -v /etc/group:/host/etc/group:ro \
  -v /proc:/host/proc:ro \
  -v /sys:/host/sys:ro \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined
```

For more information about running immudb in Docker, check the [docker installation page](packaging/docker/).


## Why immudb

immudb allows you to keep a history of changes in your important data without changing your applications and store those data changes immutably in the tamperproof immudb database. You get cryptographic verification of the integrity of all your records written to immudb using SHA-256 hash confirmation. You also get confirmation of the chronological sequence of the records inserted in immudb. 

immudb only exposes APIs to add data, but not to change or delete, or change the order of data. Internally immudb uses a Merkle Tree to provide you a guaranatee that no data has been changed, for example with a disk editor. 

immudb is **open-source**, **free**, super **fast**, very **easy**, completely **open**, extremely **efficient**,
**flexible** and integrateable with any environment you use, from **Java** to **Python**, to **C**, **C++**, **node.js**, **Golang**, and many others. 

It has been designed by **system administrators**, **DevOps engineers**, and **developers** becasue they themselves felt the need of an open source, light weight immutable datastore. 

## News



Release v0.1 contains 2 will be unleashed to the world real soon. 

We completed a major update of the cryptographical verification, and added **secondary indices** to allow you to query
by any item inserterd in the database. 

---



## How it works

immudb is a highly efficient, highly modular, write-only database fully ACID compliant.

insert slides here


## Infographic


## Features


### Integrations

-   Java
-   Python
-    etc. 

## Verification
## Documentation


## Community

We welcome [contributions](CONTRIBUTING.md). Feel free to join the team!

To report bugs or get help, use [GitHub's issues](https://github.com/immudb/issues).

You can also find immudb on:

-   [Facebook]
-   [Twitter]
-   [StackShare](https://stackshare.io/
-   [Product Hunt](https://www.producthunt.com/posts/
-   [Repology](https://repology.org/metapackage/immudb

## License

Netdata is [Apache v2.0 LIcense](LICENSE).

immudb re-distributes other open-source tools and libraries. Please check the [third party licenses](REDISTRIBUTED.md).

## Is it any good?

Yes.


## Is it awesome?

[These people](https://github.com/codnotary.com/   see to like it }
