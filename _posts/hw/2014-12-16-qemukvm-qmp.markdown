---
layout: blog
date:  2014/12/16 9:26:42
title: qemukvm qmp
categories: hv
tags: qemu-kvm中的qmp命令以及hardware passthough 命令详解
---
# 简介
qemu monitor protocol 简称qmp，是以json为格式的一种协议。qmp是qemu-kvm虚拟机中的一个重要组成部分。如果使用libvirt起一台虚拟机，libvirt使用qmp给qemu发送命令，qemu通过qmp events(qmp事件)返回，所以说qmp是libvirt和qemu之间交互的一个重要通道。
# 以网卡的穿透技术对qmp命令进行分析


