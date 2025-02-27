+++
title = "Go Channel"
description = "A Pub/Sub implemented on Golang goroutines and channels"
date = 2019-07-06T22:30:00+02:00
bref = "A Pub/Sub implemented on Golang goroutines and channels"
weight = 40
+++

{{% load-snippet-partial file="src-link/pubsub/gochannel/pubsub.go" first_line_contains="// GoChannel" last_line_contains="type GoChannel struct {" %}}

You can find a fully functional example with Go Channels in the [Watermill examples](https://github.com/ThreeDotsLabs/watermill/tree/master/_examples/pubsubs/go-channel).

### Characteristics

| Feature | Implements | Note |
| ------- | ---------- | ---- |
| ConsumerGroups | no | |
| ExactlyOnceDelivery | yes |  |
| GuaranteedOrder | yes |  |
| Persistent | no| |

### Configuration

You can inject configuration via the constructor.

{{% load-snippet-partial file="src-link/pubsub/gochannel/pubsub.go" first_line_contains="func NewGoChannel" last_line_contains="logger:" %}}

### Publishing

{{% load-snippet-partial file="src-link/pubsub/gochannel/pubsub.go" first_line_contains="// Publish" last_line_contains="func (g *GoChannel) Publish" %}}

### Subscribing

{{% load-snippet-partial file="src-link/pubsub/gochannel/pubsub.go" first_line_contains="// Subscribe" last_line_contains="func (g *GoChannel) Subscribe" %}}

### Marshaler

No marshaling is needed when sending messages within the process.
