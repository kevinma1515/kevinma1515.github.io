---
layout: page
title: integrating human evaluations into generative design process
description: can we human-in-the-loop train generative design models?
img:
importance: 1
category: work
---

This was for my CS287H Algorithmic Human-AI Interaction (HAI) project during my early stage of the PhD. I decided to publish it on my blog as I find being able to track how how I have grown in my understanding of AI over the years would be interesting. 

The primary goal of this project was to investigate whether we can use humans to help narrow down the latent space of a GAN model. The idea goes that if you train a GAN model with lots of designs, then getting a specific generation with a pre-trained model is hard! Perhaps a method where you can fine-tune the model via human preferences would be possible. A lot of inspiration was taken from the preference based RL algorithm devised by Christiano et. al. in 2017.

The framework I used was a bit naive, and, in hindsight, would never work. But alas, I will present it anyway:
(1) A generator is first pre-traiend on existing datasets through a DCGAN model
(2) The pre-trained generator (G(z)), takes in two random inputs, $z_1$ and $z_2$, which generates 2 designs.
(3) Every thousand iterations, the pairs of generated outputs are sent to human for comparison
(4) The parameters of the reward function estimates are optimized via supervised learning.

How were the results? Not very good. I am sure there has to be a better way of doing a human-in-the-loop training for a generative design model that is not as inefficient as mine, but after this project, I explored this topic no further (and this is still the case as of 03/2024 when I posted this blog). As of right now, given the powerful text-to-image and image-to-text models that are being created by OpenAI and Google, I just do not see any reason to explore this topic again because the need just is not there. As of right now, the demand is for pure (HAI) with proper human factors protocols rather than algorithmic HAI. Maybe one day in the future I will explore this topic again! Algorithms do interest me, and I love tinkering with the math.

CLICK [HERE!](https://kevinma1515.github.io/assets/pdf/cs287h.pdf) for the PDF of the report!





