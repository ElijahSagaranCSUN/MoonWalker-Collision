---
title: Technologies
layout: default
---
<nav>
	<a href="{{ site.baseurl }}/">Home</a>
	<a href="{{ site.baseurl }}/about.html">About</a>
	<a href="{{ site.baseurl }}/technologies.html">Technologies</a>
	<a href="{{ site.baseurl }}/skills.html">Skills</a>
	<a href="{{ site.baseurl }}/demo.html">Demo</a>
</nav>

{% include site_header.html %}

## **Technologies**
This project uses several technologies to support simulation interoperability and real time communication:
- **NVIDIA Omniverse Isaac Sim**: used for the Omniverse-based simulation environment
- **Unity Game Engine**: used for the Unity-based simulation environment
- **Programming Language**:
	- Python: utilized for scripts on the Omniverse side
	- C#: utilized for the scripts on the Unity side
- **FastAPI**: used to build the HSML API, which acts as the connection layer between the two platforms.
- **Apache Kafka**: used to stream rover location and physics parameters in real time between simulation platforms
- **MySQL**: used to handle authentication and autorization of users
- **Tailscale**: used to enable secure remote access and collaboration for the HSML API

Together, these technologies made it possible to connect the two simulation environments and exchange data reliably and efficiently

{% include footer.html %}