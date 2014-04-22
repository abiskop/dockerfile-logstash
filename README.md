#Dockerfile for logstash

Trusted build: [abiskop/logstash](https://index.docker.io/u/abiskop/logstash/).

**Build Dependencies**:
- [abiskop/openjdk](https://github.com/abiskop/dockerfile-openjdk)

**Runtime Dependencies**:
- [mirkokiefer/redis](https://github.com/mirkokiefer/dockerfile-redis)
- [abiskop/elasticsearch](https://github.com/abiskop/dockerfile-elasticsearch)

The logstash indexer can be run with:

```
docker run --link redis:redis --link es:es -i -t mirkokiefer/logstash bash /logstash-indexer.sh
```

This requires named instance for redis and elasticsearch.
