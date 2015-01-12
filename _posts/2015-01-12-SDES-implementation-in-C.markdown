---
layout: post
title:  "Simplified DES (SDES): an implementation in C."
description: "A simplified version of the famous encryption algorithm, DES."
date:   2015-01-12 3:27:00
categories: jekyll update
---
A few months ago, I went through a quite challenging experience as a student of an introdutory class on Criptography: I was required to give a presentation on **DES** algorithm.

After going through the titles of the reliable books on the subject, I decided to read *Criptography and Network Security* by William Stallings and one of the first sentences on that page got my attention: *"[...] the structure of DES and most symmetric ciphers is very complex and cannot be explained as easily [...]".* 

Therefore, in the next paragraph, it said that studying a simplified version (SDES) would enhance understanding of DES, and I can guarantee that it actually does. After a couple of hours struggling in the beginning, I got the idea behind one of the most important symmetric ciphers algorithms.    

#The implementation in C.

Throughout the process of creating the presentation (which I did explaining the DES with a block size of 64 bits), I realized that the SDES would be better to make people understand the step-by-step bits manipulation involved, as well as it would help me to check my answers on paper was right. I didn't find anything useful and "simple" enough, so I decided to do it myself.



