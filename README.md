# Logstash demo

Uses [willdurand/docker-elk](/willdurand/docker-elk)

## Getting started

OS X and Homebrew assumed.

    brew install boot2docker
    boot2docker init
    boot2docker start
    $(boot2docker shellinit)

    docker-compose up
    open http://$(boot2docker ip):8080

In Kibana UI:

1. `[X] Use event times to create index names`
1. `Time-field name: @timestamp`
1. `Create`
1. `Discover`

Send some sample messages to the logger:

    nc $(boot2docker ip) 22000
