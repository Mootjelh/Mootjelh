## Mootjelh

Backend and request engineering, mostly Go. High-concurrency automation,
low-latency monitoring, and the full-stack tooling that operates it.

### Open source

- [flatread](https://github.com/Mootjelh/flatread) · read FlatBuffers
  buffers when you don't have the schema. Field access by vtable slot
  instead of by generated name, for plain and size-prefixed buffers alike.
  No dependencies, fuzz-tested so it never panics on malformed input.
- [proxypool](https://github.com/Mootjelh/proxypool) · rotating proxy pool
  with cooldowns. Deliberately small: no health checks, because only your
  own traffic can tell you whether an address works.
- [hardiff](https://github.com/Mootjelh/hardiff) · compare two HTTP Archive
  captures. Matches requests by endpoint rather than by full URL, so a cache
  buster does not turn every call into one request removed and one added, and
  compares JSON bodies field by field instead of as a blob.
- [flatschema](https://github.com/Mootjelh/flatschema) · infer a FlatBuffers
  schema from sample buffers. Merges what each sample populated and writes the
  .fbs they imply, keeping the slot numbering right where a field nothing
  populated would otherwise shift every field after it.

### Upstream

- [bogdanfinn/tls-client#266](https://github.com/bogdanfinn/tls-client/pull/266) ·
  a cached transport was reused after the server changed the protocol it
  negotiated, so an HTTP/1 transport read an HTTP/2 SETTINGS frame as a status
  line. Merged, in v1.16.0.
- [bogdanfinn/tls-client#270](https://github.com/bogdanfinn/tls-client/pull/270) ·
  the transport cache was written from a reconnecting dial holding a different
  mutex than the one guarding it, so a read and a write could overlap. Found
  with the race detector. Merged.
- [bogdanfinn/fhttp#27](https://github.com/bogdanfinn/fhttp/pull/27) ·
  a deflate body was sniffed and buffered while the response was still being
  built, so over HTTP/2 the request never returned. gzip and brotli on the same
  host were fine. Merged.

### Stack

Go · TypeScript · Node · React / Next.js · PostgreSQL · MongoDB · Redis ·
Docker · REST & GraphQL

### What I build

Request-based automation in Go: site modules, CLI tooling, and systems that
have to stay fast under heavy concurrency. Real-time Discord tooling,
scraping and database sync. Monitoring with sub-second reaction times.
Dashboards and API backends to drive all of it.

[**field-notes**](https://github.com/Mootjelh/field-notes) · what I learned
from being confidently wrong 74 times while reverse engineering a
bot-protected site. 71 of them were my own bug.

Available for project work and monthly retainers.
Reach me at [info@mh-automation.nl](mailto:info@mh-automation.nl).
