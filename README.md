TcpProxy
========

Yet another tcp proxy server.


Features
========

  * Simple, small code base
  * Very fast, high performance
  * Totally non-blocking IO operations.
  * Multi IO thread 

  
Simple tutorial
========
####1.Edit application.conf in the release folder to add proxy hosts.
```javascript
tcpProxyServer {
	hosts = [{
				localPort = 465
				remoteHost = smtp.gmail.com
				remotePort = 465
			},{
				localPort = 993
				remoteHost = imap.gmail.com
				remotePort = 993
			},{
				localPort = 995
				remoteHost = pop.gmail.com
				remotePort = 995
		 	},{
				localPort = 25
				remoteHost = smtp.qq.com
				remotePort = 25
			 },{
				localPort = 143
				remoteHost = imap.qq.com
				remotePort = 143
			 }]
	so_backlog = 1000
	connect_timeout_millis = 15000
	so_timeout = 15000
	ioThreadNum = 5
	debug = true
}
```
  
