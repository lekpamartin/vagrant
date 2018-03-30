<h1>ELK</h1>

<h2>Logstash</h2>

<h2>Kibana</h2>

<h2>Elastic search</h2>

<h3>Configuration</h3>
La configuration minimale
<pre><code>
#Renommage cluster
cluster.name: cluster-elasticsearch

#Renommage node
node.name: ${HOSTNAME}

#Affectation IP
network.host: ["192.168.56.50", _local_]

#Detection des nodes du cluster
#scale vertical 1 IP, scale horizontal plusieurs IP/DNS
discovery.zen.ping.unicast.hosts: ["192.168.56.50", "host5"]
</code></pre>

