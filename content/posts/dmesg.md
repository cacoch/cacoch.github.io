---
title: "Dmesg"
date: 2022-01-09T20:43:20-06:00
draft: false
tags: [linux,kernel]
---

The dmesg output is too short, so make it larger.

To change the size of kernel buffer ring, 
in general setup:

 Kernel log buffer size (16 => 64KB, 17 => 128KB)

 CONFIG_LOG_BUF_SHIFT

The size of the buffer is 2^CONFIG_LOG_BUF_SHIFT bytes

Note that if you've passed a kernel boot param log_buf_len=N (check using cat /proc/cmdline) then that overrides the value in the config file.
