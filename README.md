# Project for spring-boot, spring-data-elasticsearch with elasticsearch 2.4.x 

## Install elasticsearch 2.4.x
(for limit spring-data support on elastic search)
>brew versions elasticsearch
>brew install elasticsearch@2.4 
## Add elasticsearch to auto launch in mac
>ln -sfv /usr/local/opt/elasticsearch/*.plist ~/Library/LaunchAgents
>launchctl load ~/Library/LaunchAgents/homebrew.mxcl.elasticsearch.plist
## Add elasticsearch to manual start
>cd /usr/local/opt/
>ln -s elasticsearch ../Cellar/elasticsearch@2.4/2.4.6_1]
>ls -l 
elasticsearch -> ../Cellar/elasticsearch@2.4/2.4.6_1
>vi .bashrc
>add line export ES_HOME=/usr/local/opt/elasticsearch
>add line export PATH=$PATH:$ES_HOME/bin
##Uninstall elasticsearch from MAC plist
### checks to see if running 
>launchctl list | grep elasticsearch
>launchctl unload ~/Library/LaunchAgents/homebrew.mxcl.elasticsearch.plist
>launchctl remove homebrew.mxcl.elasticsearch
>pkill -f elasticsearch
>rm -f ~/Library/LaunchAgents/homebrew.mxcl.elasticsearch.plist
>brew uninstall elasticsearch
### double check existence
>ls -al /usr/local/bin/elasticsearch*
>ls -al ~/Library/LaunchAgents


##Create spring-boot and spring-data-elasticsearch project
### Difference between spring-elasticsearch vs. spring-data-elasticsearch
spring-data-elasticsearch supported elasticsearch version <5.0.0 and provide CRUD interface list JPA of data access, 
instead of using REST API call to elasticsearch, which spring has gone through JREST or TransportClient

##Project content
###elasticdata - spring-boot, spring-data-elasticsearch with elasticsearch 2.4.x 




