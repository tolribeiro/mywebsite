---
layout: post
title:  "BPSK modulation using PSK on Matlab"
description: "Using Matlab to learn about digital modulation"
date:   2014-10-30 21:53:05
categories: jekyll update
---
This semester I had some exposure to digital modulation and learned some techniques applied to the studies of Communications Systems, which we'll put into practice by using the powerful software MATLAB.

For this tutorial, I'll pick up the PSK (Phase Shifting Keying). However, if you want and feel comfortable, you can also try it using ASK, FSK or QAM, that along with PSK, forms the group of main types of digital modulation widely used in a variety of modern systems, such as cellular networks and so on. 

First, let's suppose we have a message m(t), which is a bit-stream signal, that we want to send through an analog channel. For this example, we consider the frequency of m(t) as 2Hz.