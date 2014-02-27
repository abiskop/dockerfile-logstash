#Dockerfile for logstash

Trusted build: [mirkokiefer/logstash](https://index.docker.io/u/mirkokiefer/logstash/).

**Build Dependencies**:
- [mirkokiefer/java](https://github.com/mirkokiefer/dockerfile-java)

**Runtime Dependencies**:
- [mirkokiefer/redis](https://github.com/mirkokiefer/dockerfile-redis)
- [mirkokiefer/elasticsearch](https://github.com/mirkokiefer/dockerfile-elasticsearch)

The logstash indexer can be run with:

```
docker run --link redis:redis --link es:es -i -t mirkokiefer/logstash bash /logstash-indexer.sh
```

This requires named instance for redis and elasticsearch.
