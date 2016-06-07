# munin-elasticsearch2

A simple Munin plugin for monitoring elasticsearch 2.x nodes in Ruby.

munin-elasticsearch2 is inspired by claygregory's munin-elasticsearch plugin (https://github.com/claygregory/munin-elasticsearch)

## Supported Modes

 * cache - query cache stats
 * docs - document count / deleted document count
 * gc - GC collections/sec (young, old)
 * gc_time - GC collection running time in ms (young, old)
 * jvm - JVM heap stats / survivor, young, old
 * ops - index, get, search, delete, merges operations/sec
 * store - size of index

```
ln -s /usr/share/munin/plugins/elasticsearch_ elasticsearch_jvm
ln -s /usr/share/munin/plugins/elasticsearch_ elasticsearch_docs
```

## Configuration

### Variables

 * host - a elasticsearch node capable of providing stats interface (default localhost)
 * port - elasticsearch HTTP API port (default 9200)
 * node - the name of the node to monitor (required)

### Example

```
[elasticsearch_*]
env.host 127.0.0.1
env.port 9200
env.node foobar
```

## Contributing

1. Fork it ( http://github.com/t-cyrill/munin-elasticsearch2/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
