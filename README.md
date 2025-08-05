# Cloud-TAK-Server

This repository is an on-going project to learn, experiment with TAK (Team Awareness Kit) and the CoT (Cursor-on-Target) message standard; specifically, how both can enhance digital interoperability across disaggregated entities (e.g. DoD, first responders, hikers, etc.). TAK is a multi-purpose, open-source geospatial application that faciliates situational awareness amongst teams while CoT is an open-standard XML-based format for sharing real-time location and situational awareness data between devices/systems (that run TAK software). Put simply, CoT messages are exchanged across devices and displayed on a TAK map as NATO symbology (MIL-STD-2525).

Having recently learned about the developmental side of TAK (through the open-source SDK) and cloud technology in general (through AWS/Azure), I decided to deploy an open-source TAK server (OpenTAKServer, developed/maintained by Brian Wallen) to an Azure VM to showcase how to quickly deploy (< 1 hr) an extensible, interoperable Common Operating Picture. The server can be deployed on other physical hardware (e.g. Raspberry Pi); however, a cloud environment allows for quick and scalable configuration of the underlying host environment (Linux/Ubuntu in this case). With the server up and running, I was then able to connect my Galaxy tablet (running ATAK) to the server by scanning a pre-generated QR code from the OpenTakServer WebUI that configured the server IP connection within ATAK. If desired, I can generate multiple QR codes for anyone that I wanted to grant access to my server.

# A brief use case of TAK / CoT

With a TAK server up and running, individual personnel with an end user device (e.g. laptop, phone, tablet running the TAK/ATAK software) can at a minimum transmit/receive their location/status to the TAK server (by line of sight or internet) which then broadcasts this information to all other users that are connected to the server at a pre-determined refresh rate. In situations of disaster relief, search/rescue, this information is critical to providing aid.

Since the CoT XML format has a schema of 12 required fields, the type of information that can be packaged can also include use cases for the exchange of sensor data, line of bearing info, etc. 

Additionally, the broader community can develop custom plug-ins for the TAK software/ecosystem that provide unique capabilities. Some examples include the broadcasting of AIS data, Remote ID (UAS ID), ADS-B, etc.

# Screenshots

