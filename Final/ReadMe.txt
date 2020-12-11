The purpose of this code is to demonstarte the feasibility of transmitting ASI messages over TCP port, as well as decoding, storing, and visualizing these messages.

There are 3 pieces to this system:
NMEA Simulator
DFO-Project.ipynb
AIS_to_Mongo.ipynb

The NMEA simluator and instructions for installing can be found here: https://github.com/panaaj/nmeasimulator

Once installed, you must go into the application settings and select TCP(client) under Server.
You will then input the port number (3002 is standard) and the IP (your own ip)

After this, you will open and run the DFO-Project.ipynb file to intake and decode the messages coming from the simulator, and store them in a data structure for future use.

Since the simulator only generates the position of one vessel, the second part of the system uses dummy ais data for multiple vessels for ease of demonstartion and proper visualization of multiple entities.

You can run the cells in the AIS_to_Mongo.ipynb to demonstrate storing the dummy data (more complex so better for demonstartion than singular vessel, but the singular vessel data generated from DFO-Project.ipynb can still be used with minimal modifications to the code). The MongoDB was hosted on AWS and you will need to put in your own credentials for accessing the database.

Within this same file, you can choose which type of visualization to use: ArcGIS, GoogleMaps, or GoogleMaps+Bokeh
We suggest using GoogleMaps+Bokeh as it is easiest to set up. Other than running the relevant code snippets, you will need your own Google API key.

Visualization includes other releveant data associated with each point and can be further extended if desired to include other freatures of the Data (ex. MMSI number).