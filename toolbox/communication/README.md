# Communication

## Introduction

The **Communication Nodes** \(**CAN**, **HTTP**, **MAVLink**, **MQTT**, **Serial**, **Socket.IO**, **TCP**, and **UDP**\) represent the different messaging protocols and ways of communicating between devices that each one employs. 

**Serial**, **Socket.IO**, **TCP**, and **UDP** are available as plugins. For more information, check out the [**Plugins Module**](../../modules/plugins/README.md)

The following guideline explains the specific set-up required to implement **Communication** in **Incari**.

## General Guideline

These are the general guidelines for incorporating **Communication** into a **Project**. This includes how to start a connection, the **Nodes** that can be used and how to use them, as well as how to stop a connection. 

* Locate the desired communications protocol in [**Project Settings**](../../modules/project-settings/README.md). Attach all necessary files and data. 
* In the **Logic Editor**, use the protocol's **Start Node** to initiate the connection. Separately, use the protocol's **On Start Node** to execute any following **Logic**. This is to make sure the connection is successfully finished being established before doing anything.
* Use any combination of the protocol's **Nodes** to provide **Communication** capabilities to the **Project**. The protocols supported by **Incari** are [**CAN**](can/README.md), [**HTTP**](http/README.md), [**MAVLink**](mavlink/README.md), [**MQTT**](mqtt/README.md), [**Serial**](serial/README.md), [**Socket.IO**](socketio/README.md), [**TCP**](tcp/README.md), and [**UDP**](udp/README.md) communication. For more information on each protocol, visit their respective page.
* To terminate the connection, use the protocol's **Stop Node** to start disconnecting. Separately, use the protocol's **On Stop Node** to execute any following **Logic**. This is to make sure the connection is stopped completely before doing anything. 

## Content

* [**CAN**](can/)
* [**HTTP**](http/)
* [**MAVLink**](mavlink/)
* [**MQTT**](mqtt/)
* [**Serial**](serial/) 
* [**Socket.IO**](socketio/)
* [**TCP**](tcp/)
* [**UDP**](udp/)

