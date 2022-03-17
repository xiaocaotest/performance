docker inspect -f '{{ .Name }} => {{ .NetworkSettings.IPAddress }}' $(docker ps -q)

result=`date +“%Y%m%d%H%M%S”` && jmeter -n -t /data/websocket.jmx -l /data/$result.jtl -j /data/$result.log -e -o /data/$result -R 34.124.230.230