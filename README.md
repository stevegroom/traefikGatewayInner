# Traefik setup with security first - Secondary Repo

<https://github.com/stevegroom/traefikGatewayInner.git>

## Introduction

This repo is the result of trying to secure aspects of my home network such as:

- Secure access to my home automation tools
- Developing services when outside my home
- Sharing services to others
- Using cloud based devops services to trigger builds on premises

I decided to use Traefik but needed to add some other services to complete the setup. Most of this work is not original, but pulling it all into a single solution took me quite a lot of time, so hopefully this will help some of you.

## Secondary Repo

Traefik is a router that typically sits behind a routers forwarded ports. Internet -> Router -> Traefik Gateway -> services on the same subnet.

I have some scenarios where I need to access another subnet, requiring two Traefik instances.

Internet -> Router -> Outer Traefik Gateway -> Another Router -> Inner Traefik Gateway -> services on a different subnet.

This repo is for the non-encrypted, non-authenticated (inner) traefik service and is intended to augment the repo <https://github.com/stevegroom/traefikGateway.git>
