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
