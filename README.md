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