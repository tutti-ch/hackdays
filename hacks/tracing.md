---
hackname: Tracing
quicksummary: Distributed tracing across the platform
resource: true
archived: false
categories: [hack]
---

# Distributed tracing

## Why
Tutti's infrastructure is becoming more distributed, consisting of more individual components. This
makes it harder for any single person to know the exact path a request takes, what services it talks
to, what the bottlenecks are, etc.

Distributed tracing helps with this by following the path a request takes all the way through the
infrastructure. This already exists in Tutti to an extent through context IDs, but they're only
stored in logfiles, which is not easy to read and to correlate as a human.

## How
OpenTracing (as well as other standards like OpenCensus, Zipkin, etc.) helps solve this by
standardizing how tracing is done. Jaeger, built on top of the OpenTracing standard is an opensource
tool by Uber which visualizes this information.

This hack aims to set up Jaeger and instrument one or more services in tutti-services as a
proof-of-concept.

## Who's Participating?

- [Andor](/hackdays/whoami/andor)
