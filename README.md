myRepository
============

This is my first repository

I have linked this repository to a NAT forwarded private Windows 10 installation of Jenkins on bare-metal in my home network.
Frankly, I am suprised all of this is working so well at this point :o)


Here are some notes:
$JAVA_HOME/jre/lib/security/cacerts
$JAVA_HOME = C:\Program Files\Java\jdk-17.0.4.1

keytool -list -v -keystore cacerts
keytool -import -trustcacerts -alias updates-jenkins-ic -file updates.jenkins.io.crt -keystore cacerts



C:\Work\Applications\Jenkins\

$COMPUTERNAME = RFGEPEN52R


https://updates.jenkins.io

openssl s_client -showcerts -connect updates.jenkins.io:443
keytool -importcert -keystore cacerts -storepass changeit -file cert1.crt -alias "cert1"
keytool -importcert -keystore cacerts -storepass changeit -file cert2.crt -alias "cert2"
keytool -importcert -keystore cacerts -storepass changeit -file cert3.crt -alias "cert3"


GitHub - WebHooks
URL	http://99.45.147.27:8888/github-webhook/            99.45.147.27 is My Public facing router IP address.  8888 is forwarded, of which is hosting Jenkins.


I am thinking now I just push this back to my Git repository and I should (at least) having something in my Jenkins logs.
NOTE:  This file was edited using Visual Studio Code.
