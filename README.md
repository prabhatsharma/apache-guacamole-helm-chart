# Apache guacamole

A helm chart for apache guacamole. 

This helm chart provides a complete setup of:

- Guacamole server
- Guacd Proxy
- MySQL server

You can get it up ang running by:

1. git clone https://github.com/prabhatsharma/apache-guacamole-helm-chart
2. cd apache-guacamole-helm-chart
3. helm install . -f values.yaml --name=guacamole --namespace=guacamole
4. kubectl --namespace guacamole port-forward svc/guacamole 8080:80
5. visit http://localhost:8080/guacamole in your browser. Default creds are guacadmin/guacadmin

I have not been able to get it to work though for RDP. Have been getting the following error on guacamole server:

```log
03:11:09.440 [http-nio-8080-exec-4] ERROR o.a.g.w.GuacamoleWebSocketTunnelEndpoint - Creation of WebSocket tunnel to guacd failed: java.net.ConnectException: Connection refused (Connection refused)

03:11:09.575 [http-nio-8080-exec-3] ERROR o.a.g.s.GuacamoleHTTPTunnelServlet - HTTP tunnel request failed: java.net.ConnectException: Connection refused (Connection refused)
```