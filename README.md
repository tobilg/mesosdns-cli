# mesosdns-cli

A Node.js-based CLI for querying Mesos DNS service names

## Installation

This package can be installed globally via `npm install -g mesosdns-cli`.

## Usage

### Command line arguments

**Mandatory arguments**

```
--serviceName <service name> : The Mesos DNS service name to be queried
--servers <comma separated ip addresses> : The Mesos DNS server ip address(es)
```

**Other arguments**

```
--portIndex <port index number> : The port index of the service name that should be queried
--strategy <strategy name> : The strategy how to choose from the list of results (either 'weighted' or  'random')
```

### Running

If your Mesos DNS server resides on `192.168.0.1`, and you want to to resolve the service name `web.marathon.mesos`, then you can use

    $ mesosdns-cli --serviceName web.marathon.mesos --servers 192.168.0.1

to receive a `{host}:{port}` endpoint, such as `192.168.0.2:8080`.