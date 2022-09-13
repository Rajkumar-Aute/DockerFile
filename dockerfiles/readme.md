run below commends to login dockerhub

echo <password> | docker login --username=rajkumaraute --password-stdin
docker build -t os .
docker tag os rajkumaraute/os
docker push rajkumaraute/os