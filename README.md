# Devil
Real time logger for android.<br>
Built up on Mqtt - primarily designed for low speed networks.


# Debug - Error - Verbose - Info - Logger
Project that demonstrates Realtime logging in android application.These logs can be monitored in 
a partner app called DevilBoard. This can really be useful while submitting the application for 
tester/client. As we can see the logs in realtime, the communication gap between the tester and 
developer can be decreased exponentially, which will decrease the development time. 
Also if something goes wrong while the tester is testing we have all the logs we need to debug the 
situation and pinpoint the cause of issue then and there. We can u use the same logs to identify 
bottle necks in api server and solve them efficiently. 
A Custom interceptor specially designed to work with retrofit to give accurate timestamps of 
request and response. The complete Devil logger will intercept all the network call in the 
application with only 2 lines of code. 


# Pros
Light weight<br>
Light speed<br>
Low data usage<br>
Can provide the details about log code location<br>
Intercepts all api calls in android with 2 lines of code<br>
Rule based - Local logs + Remote logs - each can be disabled and enabled individually<br>
Can monitor realtime user - online user count / offline user count<br>
Can give more data on api bottle necks. <br>
Filtering out individual user logs in realtime<br>
Can be easily implemented for other platforms as well.<br>


## Features

- Devil - Class provides main API's to use Devil. 
- RemoteDevil - Processes and manages sending messages to server.
- Devil Store - Managing message queing when Devil is not connected to server.  
- DevilNetworkInterceptor - Intercept network calls in the application and produce logs and push to Devil.
- Hermes - A messaging module used to send and receive messages.
- Hermes Async - Module to implement Push notifications in the application.



## Deployment

To use Devil import the SDK and initialize in your Application class.

Devel need some configuration to start.
- isLocalEnabled - Enable and disable Local logs.
- isRealTimeEnabled -  Enable or disable Remote logging in real time.
- UserId - Used to identifiy a specific user.

![App Screenshot](https://raw.githubusercontent.com/kevinOcconer/msd_vertical_submission/main/Screenshot%202022-03-21%20at%208.32.27%20PM.png)

## Enable Devil network monitoring

Devil has a custom inbuild network interceptor that can be plugged into your Netwokting library.<br>
A simple usage example with Retrofit and OkHttClient is shown below.
![App Screenshot](https://raw.githubusercontent.com/kevinOcconer/msd_vertical_submission/main/Screenshot%202022-03-21%20at%209.55.42%20PM.png)

Once your plugin the DevilNetworkInterceptor into your Network it will monitor the network and log events to console and server.




## Devil heavily relies on below libraries.

 - [Paho mqtt for android by eclipse](https://github.com/eclipse/paho.mqtt.android)
 - [RxJava by Reactive](https://github.com/ReactiveX/RxJava)





