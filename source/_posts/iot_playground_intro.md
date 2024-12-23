---

# M5stickC Plus with ZephyrRTOS: IoT Sensor Node in a Wireless MQTT Network  
title: M5stickC Plus with ZephyrRTOS
subtitle: IoT Sensor Node in a Wireless MQTT Network - Intro
date: 2024-12-23
tag: M5stickCPlus
category: DIY
---

## Introduction  

I recently got my hands on an intriguing IoT gadget.  
![M5stickC Plus](https://static-cdn.m5stack.com/resource/docs/products/core/m5stickc_plus/m5stickc_plus_01.webp "M5")  

It’s hard to imagine how so many features fit onto a circuit board the size of a thumb. Its compact body integrates rich hardware resources, such as infrared, RTC, microphone, LED, IMU, buttons, PMU, and more.  

Improvements over the regular StickC include a buzzer, a larger screen (1.14-inch, 135x240 resolution LCD screen), and a 120mAh battery.  

Although this development board is small, it’s undoubtedly powerful. Since I’m currently seeking jobs related to embedded systems, this device is perfect for researching projects and sparked some creative ideas. I plan to connect it with my **Raspberry Pi 3** to collect data from IoT devices and build an IoT project, leading to the idea for this article.  

[M5stickC Plus Documentation](https://docs.m5stack.com/en/core/m5stickc_plus)  

---

## From Arduino to RTOS - Why Use RTOS for This Project?  

The M5stickC Plus supports numerous projects on Arduino and M5Burner, so why use RTOS instead of continuing with Arduino?  

Aside from my personal interest in researching RTOS, there are several significant advantages to using it:  

- **Task Management**: RTOS enables efficient scheduling of multiple tasks with priorities, which is crucial for real-time data processing.  
- **Scalability**: Makes it easier to integrate multiple modules, such as sensors, communication stacks, and networking interfaces.  
- **Stability and Reliability**: Ensures deterministic behavior, reducing the chances of system crashes or latency issues.  

The good news is that ZephyrRTOS already supports this platform, which can reduce development time.  

You can find the official ZephyrRTOS support for M5stickC Plus here:  
[ZephyrRTOS Official Support for M5stickC Plus](https://docs.zephyrproject.org/latest/boards/m5stack/m5stickc_plus/doc/index.html)  
