Simple Proxy
============

Simple Proxy is a simple .Net web proxy, originally developed with VS 2010 by Diego Vespassassina (https://github.com/vespassassina).

It is born from the need to allow applications to access an authenticated proxy without direct authentication.

In this case i would config SimpleProxy to use a parent proxy with username and password and then configure the client apps to use SimpleProxy.
It is also possible to insert some logging code between Request/Respose and to inspect the passing traffic.
It is also useful to do some logging or to debug webservices calls.

If you use any of this code please let me know if it is useful and give some credits (if possible).


Modification made by Oxyva.nl
=============================

Microsoft made some changes to the web development server of Visual Studio Express 2012 for Web. In Visual Webdeveloper express 2010 it was possible to access the development server from external devices by using a port-forwarding tool like inetd or Fiddler. When used in combination with VSE 2012 this resulted in the error "HTTP Error 400: Bad Request - Invalid Hostname".

It turned out in VSE 2012 Microsoft only allows localhost connections. This limitation makes it very hard to debug web applications on for example the iPad, iPhone and Android based devices, or browsers running other operating systems.

With the modification made by Oxyva.nl it is possible to access the development server of Visual Webdeveloper Express 2012 on any device.


Usage
=====

In order to use the proxy first modify the SimpleProxy.exe.config file and change "development_server_port" to the port your development server is running. You might also want to change "proxy_port" which is the port you use to connect the proxy. You can now run SimpleProxy.exe and connect to the port from your testing device via its ip address e.g. 192.168.178.10:9992.

Known bugs
==========

Sometimes the proxy hangs on a request. The solution is to restart the proxy and try again.