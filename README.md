packetbeat Dockerfile
=======

[Packetbeat](https://www.elastic.co/products/beats/packetbeat) ships the network traffic data to Elasticsearch to be analyzed via Kibana in a ***real-time*** fashion. 


---------------

## Usage  ##
Modify the pakcetbeat.yml file based on the scenario (device, protocol, ports, etc) of your usage.

 - Start the [ELK](https://github.com/opiuman/elk) container:
   
    `docker run -d --name=elk -p 9200:9200 -p 5601:5601 -v ~/elk:/workspace opiuman/elk`

 - Start the beat container:

 `docker run -d --name=beats --net=host -v ~/beats/conf:/conf opiuman/beats`

 - View the traffic data from Kibana -- http://dockerip:5601