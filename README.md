# Devil
Real time logger for android.<br>
Built up on Mqtt - primarily designed for low speed networks.

[![](https://jitpack.io/v/kevinOcconer/KDevil.svg)](https://jitpack.io/#kevinOcconer/KDevil)

## Features

- Devil - Class provides main API's to use Devil. 
- RemoteDevil - Processes and manages sending messages to server.
- Devil Store - Managing message queing when Devil is not connected to server.  
- DevilNetworkInterceptor - Intercept network calls in the application and produce logs and push to Devil.
- Hermes - A messaging module used to send and receive messages.
- Hermes Async - Module to implement Push notifications in the application.

## Video demo showing Devil connecting with partner application and showing logs in realtime.
https://user-images.githubusercontent.com/103298288/162556655-004ed161-1265-4084-be5b-24ee07603df8.mp4

## Deployment

Step 1. Add the JitPack repository to your build file

```groovy 
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
 ```
 
 Step 2. Add the dependency

```groovy
dependencies {
	        implementation 'com.github.kevinOcconer:KDevil:Tag'
	}
```

To use Devil import the SDK and initialize in your Application class.

Devil need some configuration to start.
- isLocalEnabled - Enable and disable Local logs.
- isRealTimeEnabled -  Enable or disable Remote logging in real time.
- UserId - Used to identifiy a specific user.

![App Screenshot](https://raw.githubusercontent.com/kevinOcconer/msd_vertical_submission/main/Screenshot%202022-03-21%20at%208.32.27%20PM.png)


## Enable Devil network monitoring

Devil has a custom inbuild network interceptor that can be plugged into your Netwokting library.<br>
A simple usage example with Retrofit and OkHttClient is shown below.
![App Screenshot](https://raw.githubusercontent.com/kevinOcconer/msd_vertical_submission/main/Screenshot%202022-03-21%20at%209.55.42%20PM.png)

Once your plugin the DevilNetworkInterceptor into your Network it will monitor the network and log events to console and server.

## Basic Devil usage to log events.
![App Screenshot](https://raw.githubusercontent.com/kevinOcconer/msd_vertical_submission/main/Screenshot%202022-03-21%20at%208.34.05%20PM.png)

## Basic Hermes usage to send a message to admin - used to make a chat module for client support.
![App Screenshot](https://raw.githubusercontent.com/kevinOcconer/msd_vertical_submission/main/Screenshot%202022-04-18%20at%209.12.05%20PM.png)

## Completed modules till now:

- Devil
- RemoteDevil
- Devil store
- DevilNetworkInterceptor
- Hermes

## Devil heavily relies on below libraries.

 - [Paho mqtt for android by eclipse](https://github.com/eclipse/paho.mqtt.android)
 - [RxJava by Reactive](https://github.com/ReactiveX/RxJava)

## COSC 6362 Mobile Software Development

## Instructor 
 - Dr. Mamta Yadav 

## Team members:
 
 - Venkata Sai Pavan Arepalli
 - Avinash Kotta
 - Vineeth Rao Vemula

 ## ROLES & RESPONSIBILITIES 

 ## Role1
 - Team leader to look over the project for overseeing timely deliverables and submissions in the project. (A.v.s.Pavan)
 ## Role2
 - Communicating with the Instructor (Vineeth Vemula, Avinash Kotta)
## Role3
- The Layout Design (Architecture) (Avinash Kotta)
## Role4
- User interface Design (Vineeth Vemula)
## Role5
- Working on Code (Java, Kotlin) as developer (A.v.s.Pavan)
## Role6
- Web Ad and other services (Avinash Kotta, Vineeth Vemula)
## Role7.    
- Implementation Tasks like Testing (Vineeth & Avinash)
