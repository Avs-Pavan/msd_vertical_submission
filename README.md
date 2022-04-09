# Devil
Real time logger for android.<br>
Built up on Mqtt - primarily designed for low speed networks.


## Features

- Devil - Class provides main API's to use Devil. 
- RemoteDevil - Processes and manages sending messages to server.
- Devil Store - Managing message queing when Devil is not connected to server.  
- DevilNetworkInterceptor - Intercept network calls in the application and produce logs and push to Devil.
- Hermes - A messaging module used to send and receive messages.
- Hermes Async - Module to implement Push notifications in the application.



## Deployment

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


## Completed modules till now:

- Devil
- RemoteDevil
- Devil store
- DevilNetworkInterceptor

## Devil heavily relies on below libraries.

 - [Paho mqtt for android by eclipse](https://github.com/eclipse/paho.mqtt.android)
 - [RxJava by Reactive](https://github.com/ReactiveX/RxJava)





