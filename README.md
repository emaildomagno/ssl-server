# ssl-server
A simple SSL server to perform simple and 2-way authentication
This project was refered to https://github.com/pavansolapure/opencodez-samples/tree/master/2-way-ssl-authentication/ssl-server whit some
minor changes
## How to run
To run this, I tried on Tomcat 8.0.x but that's no reason to not run on 8.5.x or other web container.
### Configuration
#### Tomcat
Edit the server.xml and add this connector (for me didn't run on 8443 port...)

    <Connector port="8444" protocol="org.apache.coyote.http11.Http11NioProtocol"
               maxThreads="150" SSLEnabled="true" scheme="https" secure="true"
               clientAuth="true" sslProtocol="TLSv1.2"
                keystoreFile="C:\tmp\chaves\MyServer.jks"
                keystorePass="password"
                truststoreFile="C:\tmp\chaves\MyServer.jks"
                />
