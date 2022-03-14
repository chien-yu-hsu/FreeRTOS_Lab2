"# lab2-sensor_and_interrupt-chien-yu-hsu" 
# Embedded_OS_Lab2_NE6091116
## Overview

![lab2jpg](https://user-images.githubusercontent.com/80887185/123728830-8d427880-d8c6-11eb-93e1-7a0b5184c44b.png)

Task1_Task : the Green LED blinking

ISR : the Red LED triggered // switch state

HandlerTask_Task : the Orange LED blinking 5 times

Priority : ISR > HandlerTask_Task > Task1_Task

## Motion Sensor Interrupt

<img width="328" alt="lab2motion" src="https://user-images.githubusercontent.com/80887185/123729526-b31c4d00-d8c7-11eb-8bf4-d9da82e0eb06.PNG">

## Task1_Task

使用while迴圈讓綠燈持續閃爍。

<img width="266" alt="lab2_task1" src="https://user-images.githubusercontent.com/80887185/123729686-f7a7e880-d8c7-11eb-8c9f-89f72a40a1b8.PNG">

## HandlerTask_Task

當HandlerTask_Task收到semaphore時，會進入for迴圈，執行五次橘燈閃爍。

<img width="407" alt="lab2hadler" src="https://user-images.githubusercontent.com/80887185/123730187-a2b8a200-d8c8-11eb-8b05-12aa51df2187.PNG">

## ISR

在ISR中我們改變紅燈的狀態，並且「give a semaphore」。

<img width="375" alt="lab2ISR" src="https://user-images.githubusercontent.com/80887185/123730594-32f6e700-d8c9-11eb-96d4-c6a2cc5d7671.PNG">
