# Gopinath-Narayan
DevOps Engineer 
input {
  tcp {
    port => 5000
    codec => json
  }

  udp {
    port => 5000
    codec => json
  }
}

output {
  elasticsearch { hosts => ["elasticsearch"] }
  stdout { codec => rubydebug }
}
