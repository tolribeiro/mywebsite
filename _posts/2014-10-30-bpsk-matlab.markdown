---
layout: post
title:  "BPSK modulation: using PSK as example on MATLAB."
description: "How to use MATLAB to explore and practice digital modulation."
date:   2014-10-30 21:53:05
categories: jekyll update
---
This semester I had some exposure to digital modulation and learned some techniques applied to the studies of Communications Systems, which we'll put into practice by using the powerful software MATLAB.

For this tutorial, I'll pick up the **PSK** (Phase-Shift Keying). However, if you want and feel comfortable, you can also try it using *ASK*, *FSK* or *QAM*, that along with PSK, forms the group of main types of digital modulation widely used in a variety of modern systems, such as cellular networks and so on. 

First, let's suppose we have a message *m(t)*, which is a bit-stream signal, that we want to send through an analog channel. For this example, we consider the frequency of *m(t)* as *2Hz*. Therefore, we have:

{% highlight matlab %}
% m(t) definition
f2 = 2;                       	% m(t) frequency
t = 0:.001:1;			% time definition
m = square(2*pi*f2*t);          % message 
subplot(3,1,2);
plot(t,m);                      % plotting m(t)
xlabel('Time');
ylabel('Amplitude');
title('Message Signal m(t)');
grid on;
{% endhighlight %}
![My helpful screenshot]({{ site.url }}/downloads/message.jpg)