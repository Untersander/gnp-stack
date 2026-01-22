# gnp-stack

gNMIc-NATS-Prometheus Stack for Network Telemetry

For far too long network operators have been stuck in the SNMP era. Streaming Telemetry is a very old topic now, and yet for some reason, it has not penetrated the market outside of Service Providers and Hyperscalers.

It is the author's opinion that this is predominantly due to the complexity of assembling and configuring the stack. This is the problem this project seeks to resolve. More of the background here has been written into a separate blog-like post [here](ARCHAEOLOGY.md).

I would like to point out that this project's existence is not to contradict the value of SNMP based tooling like [LibreNMS](https://www.librenms.org). For many, SNMP on a 5 min polling interval is ample. LibreNMS's coverage is fantastic, and I would recommend it to anyone looking to gain visibility on their network where non exists today. It also has a number of USPs in addition such as billing, syslog storage and device backups. This project is not in direct competition on that basis anyways.

This project exists to give those needing or wanting Streaming Telemetry that same experience of point and shoot that you get from LibreNMS today on SNMP.

If you are here as a commercial entity looking to pillage this hard work to monetise it - don't - contribute to this project and help everyone get access to better telemetry.

No matter what kind of entity you are, if you simply want to use this to monitor your network - go right ahead.

## How this works

It sort of doesnt *yet*.

Right now this is a Proof of Concept using containerlab to spin up all the components and validate the paths, transforms and dashboard views. We are focussing our attention on Nokia SRL and Arista EOS because these vendors are progressive enough to offer free containerlab images. Other vendors will come as access to equipment, time and priority allows (specifically Juniper and Nokia SROS on the basis of personal needs!)

When a critical mass is hit we will produce a docker compose file that can be loaded on any linux system with docker. In v1 we will make mapping vendors to telemetry paths with include files, and in v2 we will produce the tooling that maps the various telemetry paths to the vendor/version. We expect that target mapping will be done with SoT integrations (like Netbox and Infrahub), and telemetry path mapping will be stored in some sort of database that can be syncronised to keep it up to date as paths/versions evolve.

It will take some time to produce all these parts, but there are a handful of engineers in the community who are committed to seeing this succeed.

If you are one of them, feel free to hop into the issues board and simply report them, or pick stuff up. PRs are always welcome.
