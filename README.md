# Kubernetes-setup
This repo is to explain how to setup Kubernetes (master &amp; minion) on prem.

# Kubernetes CNI Plugins: Calico, Flannel, and Weave

This document provides a detailed comparison of three popular Container Network Interface (CNI) plugins used in Kubernetes: Calico, Flannel, and Weave. Each CNI plugin has its own architecture, features, and use cases.

## Overview

### Calico
- **Calico** is a networking and network security solution for containers, virtual machines, and native host-based workloads. It is known for its performance, flexibility, and security features.

### Flannel
- **Flannel** is a simple and easy-to-configure layer 3 network fabric for Kubernetes. It was designed to be a straightforward solution for networking in Kubernetes clusters.

### Weave
- **Weave Net** is a CNI plugin designed to provide a simple, robust, and secure network for Kubernetes clusters.

## Key Features

### Calico
- **Layer 3 Networking**: Uses pure IP networking for routing packets between nodes.
- **Network Policies**: Provides advanced network policy capabilities for security.
- **Performance**: Efficient, high-performance data plane based on BGP (Border Gateway Protocol) or an optional eBPF (Extended Berkeley Packet Filter) data plane.
- **Scalability**: Scales well for large clusters.
- **Integration**: Works with various orchestrators like Kubernetes, OpenShift, and more.

### Flannel
- **Overlay Networking**: Uses VXLAN, UDP, or other backends for creating an overlay network.
- **Simplicity**: Easy to set up and configure.
- **IP Allocation**: Manages IP address allocation to pods.

### Weave
- **Layer 2/Layer 3 Hybrid**: Uses a combination of layer 2 (MAC-based) and layer 3 (IP-based) networking.
- **Network Policies**: Supports network policies for controlling traffic.
- **Ease of Use**: Easy to set up and use with automatic encryption and multi-cloud support.
- **DNS-Based Service Discovery**: Provides integrated DNS for service discovery.

## Use Cases

### Calico
- Best suited for scenarios where network policy and security are critical.
- Ideal for large, complex, and high-performance Kubernetes deployments.

### Flannel
- Suitable for small to medium-sized clusters.
- Ideal for users looking for a simple, straightforward networking solution without advanced features like network policies.

### Weave
- Good for multi-cloud or hybrid cloud environments.
- Suitable for users needing a balance between simplicity and advanced features like network policies and encryption.

## Comparison Table

| Feature                  | Calico                            | Flannel                           | Weave                             |
|--------------------------|-----------------------------------|-----------------------------------|-----------------------------------|
| **Networking Model**     | Layer 3 (BGP or eBPF)             | Overlay (VXLAN, UDP)              | Layer 2/3 Hybrid                  |
| **Network Policies**     | Advanced                          | No (limited to basic firewalling) | Yes                               |
| **Performance**          | High                              | Moderate                          | Moderate                          |
| **Ease of Setup**        | Moderate                          | Easy                              | Easy                              |
| **Scalability**          | High                              | Moderate                          | Moderate                          |
| **Security**             | Strong (advanced policies, IPsec) | Basic                             | Strong (automatic encryption)     |
| **Use Case**             | Large, secure, high-performance   | Simple, small to medium clusters  | Multi-cloud, hybrid environments  |

## Summary

- **Calico**: Best for large, complex, and performance-sensitive clusters requiring advanced network policies and security features.
- **Flannel**: Ideal for small to medium-sized clusters needing a simple and straightforward networking solution.
- **Weave**: Suitable for environments needing a balance of simplicity, multi-cloud support, and integrated security features.

Choosing the right CNI plugin depends on your specific requirements for performance, scalability, network policies, and ease of use.

