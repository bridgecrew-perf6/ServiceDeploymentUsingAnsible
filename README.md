# ServiceDeploymentUsingAnsible

Here i am implementing two services : one simple web service and the SNMP daemon.
The basic service is an Nginx webserver which serves one simple PHP page that renders hostname,IP, and the port of the server running it.
And the second service is the standard SNMP daemon.
We need to run multiple web servers on three platforms. So, HAproxy is used to load balance between these services. The site has 5 hosts HAproxy, A, B, C and Bastion.
HAproxy runs as an entry point for acccessing the service from the servers. Bastion acts as an SSH entry point to the internal network.
Create an SSH-keygen and use the public key in the servers.
The SSH config file has to be moodified in terms of your ip addresses of your servers and the ssh private key path.
