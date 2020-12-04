# ElasticStack with LogStash, Kafka and ElastAlert for log analysis and alerting.


This demo architecture showcases:
- log events classification in Kafka topics per severity level and
- web-hook alerting based on threshold for configurable rate of events.

Implemented by using:
- [Elastic stack](https://www.elastic.co/es/products/)
- [Kafka](https://kafka.apache.org/)
- [ElastAlert](https://github.com/bitsensor/elastalert)

Adapted from [5GEVEmon]( https://github.com/5GEVE/5geve-wp4-monitoring-dockerized-env)
and [ElastAlert Server](https://github.com/bitsensor/elastalert) to be run in a single "docker-compose up" command.

## Implementation Steps:

1. Create new working folder in server
`mkdir ELK2A && cd ELK2A`

1. Clone this demo's from `https://github.com/agustincaparros/ELK2.git`
1. Set your Elastic Stack local parameters
  - Edit ELK2A/.env file vars with your Kafka machine ip address
  - Edit config/kafka-elk with your ElasticStack parameters:
     * ES username and password
     * server IP address
1. Edit config/elastalert.yaml, elastalert-test.yaml and config.json with
  * ES IP, port, es_username and es_password
  * EA rules_folder (this is not needed if rules are going to to be created by using REST API)

1. Run `cd ELK2A && sudo docker-compose up`
