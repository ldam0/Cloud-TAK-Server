# Cloud-TAK-Server

This repository is an on-going project to learn, experiment with TAK (Team Awareness Kit) software and the CoT (Cursor-on-Target) message standard; specifically, how both can enhance digital interoperability across disaggregated entities (e.g. DoD, first responders, hikers, etc.). 

* TAK is a multi-purpose, open-source geospatial application that faciliates situational awareness amongst teams
* CoT is an open-standard XML-based format for sharing real-time location and situational awareness data between devices/systems
* Put simply, CoT messages can be exchanged across devices via CoT-compatible software, such as TAK/ATAK, and displayed on a digital map overlay (map sources can be Google Maps, ESRI, Bing, etc.) as NATO symbology (MIL-STD-2525)

Having recently learned about the developmental side of TAK (through the open-source SDK) and cloud technology in general (through AWS/Azure), I decided to deploy an open-source TAK server (OpenTAKServer, developed/maintained by B. Wallen) to an Azure VM to showcase how to quickly deploy (< 1 hr) an extensible, interoperable Common Operating Picture. 

The server can be deployed on other physical hardware (e.g. Raspberry Pi); however, a cloud environment allows for quick and scalable configuration of the underlying host environment (Linux/Ubuntu in this case). With the server up and running, I was then able to connect my Galaxy tablet (running ATAK software) to the server by uploading a data package generated from the OpenTakServer WebUI. 

# A brief use case of TAK / CoT

With a TAK server up and running, individual personnel with an end user device (e.g. laptop, phone, tablet running CoT compatible software) can at a minimum transmit/receive their location/status to the TAK server (by mesh-IP network line of sight or internet) which then broadcasts this information to all other users that are connected to the server at a pre-determined refresh rate. In situations of disaster relief, search/rescue, this information is critical to providing aid.

Since the CoT XML format has a schema of 12 required fields, the type of information that can be packaged can also include use cases for the exchange of sensor data, line of bearing info, etc. 

Additionally, the broader community can develop custom plug-ins for the TAK software/ecosystem that provide unique capabilities. Some examples include the broadcasting of AIS data, Remote ID (UAS ID), ADS-B, etc.

# Some Screenshots

Architecture diagram (credit to B. Wallen of OpenTAKServer):

<img width="628" height="393" alt="Image" src="https://github.com/user-attachments/assets/5cf17d54-ac87-4d13-b23d-f9eebe2d0882" />


OpenTAKServer WebUI:

![Image](https://github.com/user-attachments/assets/363f481d-eb7a-4385-b74e-4ebf5753d32f)


Screenshot of server-provided ADS-B aviation data stream populating into ATAK software on my Galaxy tablet EUD; verifies connection and data transmission between server/EUDs:

![Image](https://github.com/user-attachments/assets/05dbae8a-51e0-4da9-ac43-e28c40b84d76)



