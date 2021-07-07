---
permalink: /mypage/
---

### Hello
#### 2021 Practical Coding

## PINF !! 
Unlike Ethernet-based TCP/IP, which transmits data through multiple layer stacks, InfiniBand takes a method of directly communiticating data through HCA. Although InfiniBand has features of low latency and high bandwidth, due to its characteristics of operating asynchronously, it makes a big difference in latency of the entire program depending on the process.
In this paper, in order to improve the latency of the communication layer using InfiniBand, we present PinF, a model that optimizes the method of processing work completion of InfiniBand.

### Introduction
With the development of computers, the CPU and memory have also evolved. The performance and cores of the CPU increased, but the memory did not increase in proportion to the cores of the CPU due to hardware limitations.
As a result, a disaggregated system, a system in which many system resources are mounted and shared on a specific server, has emerged.
This structure is a system that borrows and uses remote resources as much as necessary, unlike the current cloud system where the entire computer resources are provided when necessary [2-3].
In a disaggregated system, low latency and high bandwidth must be guaranteed for resource access. However, since the Ethernet-based TCP/IP communication layer that we generally use transmits data through many network layers to transmit data, it is difficult to satisfy the latency required by a disaggregated system


InfiniBand has features such as low latency, wide bandwidth, and RDMA (Remote Direct Memory Access), so it is a communication technology that is spotlighted for building such a disaggregated system.
However, separate from the hardware specification of InfiniBand, the InfiniBand device driver handles the request completion message when developing InfiniBand-related communication programs.
The method greatly affects the bandwidth and latency of the program [1]. In this paper, we propose a model PinF (Polling InfiniBand) that explores how the InfiniBand device driver handles work completion and optimizes it.
.
