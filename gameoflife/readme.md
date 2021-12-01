Example of multi docker build

using mavin container to build
and run application in tomcat container

Run below commends to build the app
```
docker build image -t sampleapp:1 .
docker conainter run -d -P sampleapp:1
```

<url/ipaddress>:gameoflife