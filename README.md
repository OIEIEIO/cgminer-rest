[![Build Status](https://travis-ci.org/brndnmtthws/cgminer-rest.svg?branch=master)](https://travis-ci.org/brndnmtthws/cgminer-rest)

# cgminer-rest: a RESTful HTTP wrapper for the cgminer API

![Demo](/demo.gif?raw=true)

This package provides a RESTful HTTP wrapper around the
[cgminer](https://github.com/ckolivas/cgminer) API. Cgminer has a somewhat
esoteric API, which isn't easy to use with standard HTTP-based tooling. Using
this tool, it's easy to interact with cgminer programmatically or using a UI,
such as through a web browser.

## Installing

The package can be installed from [crates.io](https://crates.io/) using the `cargo` tool:

```ShellSession
$ cargo install cgminer-rest
...
$ cgminer-rest
```

See [Rocket.toml](Rocket.toml) for configuration details.

## Example

## API

### Endpoints

    🛰  Mounting /:
        => GET /version (version)
        => GET /config (config)
        => GET /summary (summary)
        => GET /devs (devs)
        => GET /devdetails (devdetails)
        => GET /stats (stats)
        => GET /coin (coin)
        => GET /usbstats (usbstats)
        => GET /lcd (lcd)
        => GET /notify (notify)
        => GET /privileged (privileged)
        => PUT /restart (restart)
        => PUT /check/<command> (check)
        => PUT /debug (debug)
        => PUT /hotplug (hotplug)
        => GET /lockstats (lockstats)
        => PUT /zero (zero)
    🛰  Mounting /pools:
        => GET /pools (pools)
        => PUT /pools/<id>/switchto (switchpool)
        => PUT /pools/<id>/enable (enablepool)
        => PUT /pools/<id>/disable (disablepool)
        => POST /pools (addpool)
        => DELETE /pools/<id> (removepool)
        => PUT /pools/<id>/quota (poolquota)
    🛰  Mounting /pga:
        => GET /pga/<id> (pga)
        => GET /pga/count (pgacount)
        => PUT /pga/<id>/enable (pgaenable)
        => PUT /pga/<id>/disable (pgadisable)
        => GET /pga/<id>/identify (pgaidentify)
        => PUT /pga/<id> (pgaset)
    🛰  Mounting /asc:
        => GET /asc/<id> (asc)
        => GET /asc/count (asccount)
        => PUT /asc/<id>/enable (ascenable)
        => PUT /asc/<id>/disable (ascdisable)
        => GET /asc/<id>/identify (ascidentify)
        => PUT /asc/<id> (ascset)