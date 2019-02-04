# Configuration files for Solr 7

## Download and unpack Solr

```
curl  http://mirrors.dotsrc.org/apache/lucene/solr/7.6.0/solr-7.6.0.tgz | tar xz
```

## Start Solr and create a collection with the Anserini configuration

```
solr-7.6.0/bin/solr start -m 8g -p 9040
solr-7.6.0/bin/solr create -c anserini -d solr7 -shards 1 -replicationFactor 1 -p 9040
```

## Interact with Solr

Admin GUI available at http://localhost:9040/solr/#/anserini

When indexing, the Solr URL is http://localhost:9040/solr/anserini

## Stop Solr

```
solr-7.6.0/bin/solr stop -p 9040
```
