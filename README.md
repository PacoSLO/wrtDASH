# wrtDASH
Openwrt Dashboard - wrtDASH
<p align="left"> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>

## The project is still work in progress...

### Instalation:
Project runs on Flask inv. And it's running with a Gunicorn via a script on a Ubuntu LXC Container 2C/1GB Ram 30GB Disk space. So you need some server or try host it on a openwrt router if you have a beast one :)
If you have any suggetions what more to add join my discord.
I will upload the code soon, when everything is double checked.

### Key Features:
Router Management and Monitoring:

The app connects to multiple routers via SSH to retrieve data such as DHCP lease information and network traffic stats.
Network Grouping by Subnets:

Subnets are predefined, and connected clients are grouped into their respective subnets for easy management.
Latency Measurement:

Measures the network latency to well-known destinations like Google and Cloudflare using the ping command.
Speed Test:

Runs a speed test using speedtest-cli and returns download, upload, and ping results.
Public IP Detection:

Uses an external service to retrieve the public IP address of the WAN interface.
Traffic Monitoring:

Retrieves the incoming and outgoing traffic for all routers in bytes and converts it to gigabytes.
Most Recent Client Detection:

Identifies the most recent client connected to any router based on lease start time.
Web Interface:

Provides a web interface using Flask's render_template to show data such as:
Latency
Traffic statistics
Leased clients grouped by subnet
Most recent client details
CORS Support:
Flask-CORS is used to enable Cross-Origin Resource Sharing.
Usage:

Run the App:
Execute the script, and the app will start on http://0.0.0.0:8080.

Endpoints:
Dashboard with WAN IPs, latency, total clients, and system uptime.
/leases: Displays all clients grouped by subnets.
/speedtest: Runs a speed test and returns the results as JSON.
/traffic: Shows total inbound and outbound traffic across all routers.
/last-client: Displays the most recently connected client.

Templates:
Ensure that corresponding HTML templates (index.html, leases.html) are present in a templates directory.

### Images of the wrtDASH

<img
  src="https://github.com/PacoSLO/wrtDASH/blob/main/dash.png"
  alt="Alt text"
  title="Index Home"
  style="display: inline-block; margin: 0 auto; max-width: 500px">

   <img
  src="https://github.com/PacoSLO/wrtDASH/blob/main/leases.png"
  alt="Alt text"
  title="Index Home"
  style="display: inline-block; margin: 0 auto; max-width: 500px">
