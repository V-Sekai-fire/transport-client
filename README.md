# transport-client

The desktop test client for one zone of the multiplayer fabric: it draws what the zone service sends and sends back a head and two hands.

## What it is for

A flatscreen controller drives the camera and both hands from mouse, keyboard and gamepad, so a zone can be tested without a headset. The client simulates nothing: the service is authoritative over every prop, and the client's only output is its own tracked pose. [WIRE.md](WIRE.md) gives the wire format and the reasoning behind it.

## Build and run

It needs the multiplayer fabric's engine fork built with double precision, because positions on the wire are absolute integers that a single-precision build places wrongly.

```sh
godot --path .
```

## Licence

MIT; see LICENSE.
