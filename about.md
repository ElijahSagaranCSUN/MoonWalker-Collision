---
title: About
layout: default
---

{% include site_header.html %}

## **Purpose of MoonWalker**
This project focuses on digital twin interoperability for lunar rover simulations. As both public and private organizations become more active in lunar space exploration, testing rover behavior grows expensive, difficult, and potentially dangerous. Digital twins provide a safer and more cost-effective way to simulate how different rovers operate in space and under various conditions. The main challenge, however, is the non-uniformity of simulation platforms between organizations, i.e., some utilizes Omniverse, while others Unity. This discrepancy creates an environment where collaboration might be difficult. This project aims to address that problem by enabling interoperability between digital twins across different simulation platforms. Furthermore, the project specifically improves the transfer of physics parameters between platforms, allowing realistic rover collisions and interactions, which was a limiting factor prior.

## **Major Features**

- **Digital Twin Interoperability Framework.** The core contribution of this project is a bridge that lets heterogeneous simulation platforms exchange state and physics data in real time. We demonstrate it between NVIDIA Omniverse and Unity, but the framework itself is **not tied to those two platforms** — any simulator that can speak HTTP/JSON can plug into it.

- **Platform-Agnostic HSML API.** The HSML (Hyperspace Modeling Language) API is the central bridge between simulators. Because the connection layer is platform-agnostic, the API can be extended to additional simulation platforms beyond Omniverse and Unity. New adopters do **not** need to modify the bridge — they only write local business-logic scripts in their simulator (a producer that publishes rover state, and a consumer that reads incoming state from the other side) and connect them to the running API.

- **Real-Time Collision Detection and Hosting Hand-off.** When two simulated entities meet, the HSML API coordinates which simulation platform is hosting the colliding entity at any given moment. This keeps physics responses consistent across both platforms during a collision event, which prior digital-twin pipelines struggled with.

- **Extensible Authentication and Verification.** The API uses MySQL-backed authentication and authorization so that only registered Spatial Web entities (rovers, agents, users, organizations) can publish to or consume from the bridge. The auth/verification layer is modular and designed to be extended with additional credential schemes or identity providers as the framework grows.

- **Kafka-Based Real-Time Streaming Backbone.** Internal Apache Kafka producers and consumers stream position, orientation, and physics parameters between simulators in real time, so updates from one platform appear in the other with minimal latency.

- **Drop-In Integration Model.** For other research groups or organizations that want to use this work, the integration story is intentionally simple: focus on your own simulator's local logic, write a small producer/consumer pair that talks to the HSML API, and you are interoperable with anyone else on the bridge. The hard cross-platform plumbing is already done.

{% include footer.html %}
