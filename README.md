# Enhanced Buffered I/O

## Overview
This repository contains the Linux kernel modifications presented in our research. Our work introduces significant improvements in the memory management system of the Linux kernel, particularly in the context of buffered I/O operations.

## Features
- **Removal of Page Aging from Critical Path**: Optimizes the direct reclaim process to reduce high tail latency.
- **LRU Lock Splitting**: Reduces contention and improves performance during the direct reclaim procedure.
- **I/O Throttling Optimization**: Dynamically adjusts throttling to balance write performance and overall system performance.

## Installation and Usage
- Build and install the source code in the kernel directory.
- Reboot with the installed kernel. All modified features automatically function during buffered I/O.
- To check the current system's compliance with the ratio of dirty pages, use the following command: 

```
sudo cat /proc/sys/vm/dirty_ratio
```

## Citation
```
Kim, Jongseok, et al. "Revitalizing Buffered I/O: Optimizing Page Reclaim and I/O Throttling." 2023 IEEE 41st International Conference on Computer Design (ICCD). IEEE, 2023.
```
