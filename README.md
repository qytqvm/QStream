# QStream benchmarks

QStream compresses live JSON streams using a Smart Builder profile trained on sample messages. Every message is checked to restore byte-for-byte; anything unusual is sent unchanged.

## Reference results

Profile trained on 500 messages, tested on 2,000 different messages. Reference feeds are generated to match common formats, not customer data.

| Feed | JSON bytes | QStream bytes | Reduction |
|---|---:|---:|---:|
| IoT sensor telemetry | 211,984 | 30,737 | 85.50% |
| Payment webhooks | 343,475 | 125,671 | 63.41% |
| Structured application logs | 369,508 | 71,496 | 80.65% |
| Product analytics events | 309,864 | 55,974 | 81.94% |
| E-commerce orders | 415,629 | 66,709 | 83.95% |
| Fleet GPS tracking | 253,593 | 40,805 | 83.91% |
| **Total** | **1,904,053** | **391,392** | **79.44%** |

https://qytte.com/qstream
