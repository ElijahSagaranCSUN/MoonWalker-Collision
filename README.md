# MoonWalker-Collision
This project aims to improve and further Digital Twin Interoperability by exploring interaction and collision between two separate entities from two different simulation platforms. In our use case, we utilized NVIDIA Omniverse and Unity as our simulation platforms, having one rover for each. NVIDIA Omniverse hosted the Cadre rover while Unity hosted the Viper rover. This document summarizes the requirements for the Digital Twin Interoperability Collision Experiments to be recreated.

 # Requirements
 ## NVIDIA Omniverse
 1. Computer specifications outlined by NVIDIA Omniverse: [Omniverse Requirements](https://docs.omniverse.nvidia.com/dev-guide/latest/common/technical-requirements.html)
 2. Python 3.12+
 3. Python libraries: omniverse_kit, requests, pxr, charset_normalizer, idna, urllib, usd core
## Unity
1. Computer specifications

## HSML API
1. Docker

# Required Scripts
## NVIDIA Omniverse
1. CadreAOmniAPIJSON.py: requests to the HSML API and sends data about Cadre from Omniverse
2. CadreAOmni_ConsumerAPIJSON.py: requests to the HSML and reads in data about Cadre from Unity for Unity hosting
3. ViperAOmniAPIJSON.py: requests to the HSML API and reads in data about Cadre from Unity for Unity hosting
4. rover_generalizer_final.py: takes in a rover prim and generalizes it for Omniverse hosting
5. collision_HSML.py: handles collision detection and hosting switch for rover.
## Unity
1. fill out
## HSML API

# Required USD/FBX files
## NVIDIA Omniverse
1. Viper Substance File (1).fbx
2. 4WD_Contrl.usd
3. CADREDEMO.usd
4. MAINDEMO.usd
5. Shackleton Ridge 300x300 v4 -001.usd
## Unity
1. fill out
