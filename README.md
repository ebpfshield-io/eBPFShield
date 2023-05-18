<h1 align="center">
  <img alt="cgapp logo" src="https://github.com/sagarbhure/certificates/blob/main/ebpf%20-%20Copy.PNG" width="284px"/><br/>
  <p>Advanced IP-Intelligence & DNS Monitoring using eBPF</p>
</h1>
<p align="center"><b>🛡️ Advanced host monitoring and threat detection with eBPF 🛡️</b></p>

<p align="center"><b>eBPFShield</b> is a high-performance <b>security tool</b> that utilizes eBPF and Python to provide real-time <b>IP-Intelligence</b> and <b>DNS monitoring</b>. By executing in kernel space, eBPFShield avoids costly context switches and offers efficient <b>detection</b> and <b>prevention</b> of malicious behavior on your network through monitoring of outbound connections and comparison with <b>threat intelligence</b> feeds. 🔍 </p>

</div>

---

## Table of Contents

- [Introduction](#-introduction)
- [Features](#-features)
- [Dependencies](#-dependencies)
- [Usage](#-usage)
- [Sample Output](#sample-output)
- [Contributing](#-contributing)
- [Author](#-author)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 📝 Introduction

[![License](https://img.shields.io/github/license/ebpfshield-io/eBPFShield)](https://github.com/ebpfshield-io/eBPFShield/blob/master/LICENSE)
[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![GitHub commit activity](https://img.shields.io/github/commit-activity/m/ebpfshield-io/eBPFShield)](https://github.com/ebpfshield-io/eBPFShield/graphs/commit-activity)
[![Libraries.io dependency status for GitHub repo](https://img.shields.io/librariesio/github/ebpfshield-io/eBPFShield)](https://libraries.io/github/ebpfshield-io/eBPFShield)

[![powered by semgrep](https://img.shields.io/badge/powered%20by-semgrep-1B2F3D?labelColor=lightgrey&link=https://semgrep.live/&style=flat-square&logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAAA0AAAAOCAYAAAD0f5bSAAAABmJLR0QA/gD+AP+cH+QUAAAACXBIWXMAAA3XAAAN1wFCKJt4AAAAB3RJTUUH5AYMEy0l8dkqrQAAAvFJREFUKBUB5gIZ/QEAAP8BAAAAAAMG6AD9+hn/GzA//wD//wAAAAD+AAAAAgABAQDl0MEBAwbmAf36GQAAAAAAAQEC9QH//gv/Gi1GFQEC+OoAAAAAAAAAAAABAQAA//8AAAAAAAAAAAD//ggX5tO66gID9AEBFSRxAgYLzRQAAADpAAAAAP7+/gDl0cMPAAAA+wAAAPkbLz39AgICAAAAAAAAAAAs+vU12AEbLz4bAAAA5P8AAAAA//4A5NDDEwEBAO///wABAQEAAP//ABwcMD7hAQEBAAAAAAAAAAAaAgAAAOAAAAAAAQEBAOXRwxUAAADw//8AAgAAAAD//wAAAAAA5OXRwhcAAQEAAAAAAAAAAOICAAAABP3+/gDjzsAT//8A7gAAAAEAAAD+AAAA/wAAAAAAAAAA//8A7ePOwA/+/v4AAAAABAIAAAAAAAAAAAAAAO8AAAABAAAAAAAAAAIAAAABAAAAAAAAAAgAAAD/AAAA8wAAAAAAAAAAAgAAAAAAAAAAAAAAAAAAAA8AAAAEAAAA/gAAAP8AAAADAAAA/gAAAP8AAAAAAAAAAAAAAAACAAAAAAAAAAAAAAAAAAAA7wAAAPsAAAARAAAABAAAAP4AAAAAAAAAAgAAABYAAAAAAAAAAAIAAAD8AwICAB0yQP78/v4GAAAA/wAAAPAAAAD9AAAA/wAAAPr9//8aHTJA6AICAgAAAAD8AgAAADIAAAAAAP//AB4wPvgAAAARAQEA/gEBAP4BAQABAAAAGB0vPeIA//8AAAAAAAAAABAC+vUz1QAAAA8AAAAAAwMDABwwPu3//wAe//8AAv//ABAcMD7lAwMDAAAAAAAAAAAG+vU0+QEBAvUB//4L/xotRhUBAvjqAAAAAAAAAAAAAQEAAP//AAAAAAAAAAAA//4IF+bTuuoCA/QBAQAA/wEAAAAAAwboAP36Gf8bMD//AP//AAAAAP4AAAACAAEBAOXQwQEDBuYB/foZAAAAAAD4I6qbK3+1zQAAAABJRU5ErkJggg==)](https://github.com/ebpfshield-io/eBPFShield/actions?query=workflow%3ASemgrep)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/ebpfshield-io/eBPFShield/master.svg)](https://results.pre-commit.ci/latest/github/ebpfshield-io/eBPFShield/master)
[![OpenSSF Scorecard](https://api.securityscorecards.dev/projects/github.com/ebpfshield-io/eBPFShield/badge)](https://api.securityscorecards.dev/projects/github.com/ebpfshield-io/eBPFShield)
[![OpenSSF Best Practices](https://bestpractices.coreinfrastructure.org/projects/7180/badge)](https://bestpractices.coreinfrastructure.org/projects/7180)

Welcome to eBPFShield, a powerful and intuitive security tool for monitoring and protecting your servers. Featuring both <b>IP-Intelligence</b> and <b>DNS monitoring</b> capabilities, eBPFShield utilizes the power of ebpf and python to provide real-time monitoring and actionable insights for identifying and mitigating potential threats.

Say goodbye to constantly monitoring your servers with tcpdump and hello to a more efficient and automated security solution with eBPFShield.

**Available for ~~Windows~~, Linux and Ubuntu.**

<p align="center">
  <img src = "https://github.com/ebpfshield-io/eBPFShield/blob/main/docs/images/linux_ubuntu.png" width=350>
</p>

## 🛠 Features

A few of the things you can do with eBPFShield:

**Current Features: 🔥**

- **`DNS Monitoring`**: Shows all DNS queries in the system.
- **`IP-Intelligence`**: Monitors outbound connections (tcp/udp) and checks it against threat intelligence lists, block **Malicious Destination**.
  Includes script to pull down public threat feeds.

**Feature Roadmap: 📅**

- Automated IP reputation analysis using **Machine Learning** algorithms
- Support for IPv6 and non-standard DNS ports for improved coverage and detection
- Integration with popular **SIEM** systems for centralized monitoring and alerting
- JSON output for easy integration with a **UI** dashboard
- Detection of DNS packets on non-standard ports

## 📦 Dependencies

###### Installation

`apt install python3-bpfcc bpfcc-tools libbpfcc linux-headers-$(uname -r)`

## 🚀 Usage

This tool monitors outbound connections (tcp/udp, ipv4 only) and checks it against threat intelligence lists. There is a script included that pulls down two public feeds, the list of active tor exit nodes and Talos' IP blacklist. Just run `./update_feeds.sh` in the root directory of this project and it'll populate the `ip_feeds/` directory. You can add your custom lists to that directory as well.

You can run the `update_feeds.sh` script in a cron job using `crontab` to regularly update the threat intelligence feed list. This ensures that the list stays up-to-date and that eBPFShield is able to detect and prevent the latest threats.

Run `python main.py` to get started. Out of the box it will not take any action, it'll just print violations as it sees them.

```bash

$ python main.py -h
usage: main.py [-h] [--block {print, dump, suspend, kill}] [--feature {ebpf_ipintelligence, ebpf_monitor}] [--verbose]

optional arguments:
  -h, --help            show this help message and exit
  --block {print, dump, suspend, kill}
  --feature {ebpf_ipintelligence, ebpf_monitor}
  --verbose

```

There are two options supported under `--features` flag:

- `ebpf_ipintelligence`: monitor and block outbound connections against IP threat intelligence lists using tcp/udp and ipv4.
- `ebpf_monitor`: displays all DNS queries in the system.

There are four actions currently supported via the `--block` flag:

- `print`: the default action, just writes to the screen and that's it
- `suspend`: send a `SIGSTOP` to the process. This can be useful if you need to keep the process in a state where you can interact with it.
- `kill`: kill the process. This may be useful if all you want to do is immediately stop potentially malicious behavior.
- `dump`: suspend the process, take a core dump of it for forensics, and then kill it.

If you're interested in debugging, the `--verbose` flag may be useful to you. This tells the program to print all connections it sees, not just malicious ones.

## Sample Output

### Block Malicious Destination 🚫

1. In one terminal with root privileges: `$ sudo python main.py --action kill`
2. In another terminal as any user, let's use curl to send an HTTP request to a Tor exit node and another one to google.

We can see we were alerted to only the two out of three curls and that the first two are killed before the connection can complete. The last curl completes just fine.

```bash

root@host:~/eBPFShield# python3 main.py  --feature ebpf_ipintelligence --block kill
The program is running. Press Ctrl-C to abort.
Client:b'curl' (pid:140278) was killed by eBPFShield (ip-blacklist:31.41.8.66)
Client:b'curl' (pid:140279) was killed by eBPFShield (ip-blacklist:103.43.12.106)

```

```bash

root@host:~# curl -v 31.41.8.66
*   Trying 31.41.8.66:80...
* TCP_NODELAY set
Killed
root@host:~# curl -v 103.43.12.106
*   Trying 103.43.12.106:80...
* TCP_NODELAY set
Killed
root@host:~# curl google.com
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>

```

<https://user-images.githubusercontent.com/25385987/212558430-7249ee79-2972-44c2-b3aa-1d315fcae1a3.mp4>

### Monitor DNS Traffic 🔍

```bash

root@host:~# dig @1.1.1.1 google.com +tcp +short
172.217.160.206

root@host:~# dig @1.1.1.1 geekwire.com +tcp
104.26.14.176
172.67.69.185
104.26.15.176

```

```bash

root@host:~/eBPFShield# python3 main.py --feature ebpf_monitor
The program is running. Press Ctrl-C to abort.
COMM=dig PID=140623 TGID=140624 DEV=ens3 PROTO=TCP SRC=10.XX.20.37 DST=1.1.1.1 SPT=60687 DPT=53 UID=0 GID=0 DNS_QR=0 DNS_NAME=google.com. DNS_TYPE=A
COMM=dig PID=140623 TGID=140624 DEV=ens3 PROTO=TCP SRC=1.1.1.1 DST=10.XX.20.37 SPT=53 DPT=60687 UID=0 GID=0 DNS_QR=1 DNS_NAME=google.com. DNS_TYPE=A DNS_DATA=172.217.160.206

COMM=dig PID=140627 TGID=140628 DEV=ens3 PROTO=TCP SRC=10.XX.20.37 DST=1.1.1.1 SPT=42469 DPT=53 UID=0 GID=0 DNS_QR=0 DNS_NAME=geekwire.com. DNS_TYPE=A
COMM=dig PID=140627 TGID=140628 DEV=ens3 PROTO=TCP SRC=1.1.1.1 DST=10.XX.20.37 SPT=53 DPT=42469 UID=0 GID=0 DNS_QR=1 DNS_NAME=geekwire.com. DNS_TYPE=A DNS_DATA=104.26.14.176
COMM=dig PID=140627 TGID=140628 DEV=ens3 PROTO=TCP SRC=1.1.1.1 DST=10.XX.20.37 SPT=53 DPT=42469 UID=0 GID=0 DNS_QR=1 DNS_NAME=geekwire.com. DNS_TYPE=A DNS_DATA=172.67.69.185
COMM=dig PID=140627 TGID=140628 DEV=ens3 PROTO=TCP SRC=1.1.1.1 DST=10.XX.20.37 SPT=53 DPT=42469 UID=0 GID=0 DNS_QR=1 DNS_NAME=geekwire.com. DNS_TYPE=A DNS_DATA=104.26.15.176

```

<https://user-images.githubusercontent.com/25385987/212558437-86ed7b2e-2c74-41d5-93b4-3b67a4da949d.mp4>

## 🤝 Contributing

[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/ebpfshield-io/eBPFShield/blob/main/CONTRIBUTING.md)

Would you like to contribute to this project? CONTRIBUTING.md has all the details on how to do that.

## 🙋‍ Author

Developed by [@sagarbhure](https://www.github.com/sagarbhure) 🔨 with ❤️ and ☕, Visit me [🌐sagarbhure.com](https://www.sagarbhure.com).
