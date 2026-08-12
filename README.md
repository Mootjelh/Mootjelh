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

### Stack

Go · TypeScript · Node · React / Next.js · PostgreSQL · MongoDB · Redis ·
Docker · REST & GraphQL

### What I build

Request-based automation in Go: site modules, CLI tooling, and systems that
have to stay fast under heavy concurrency. Real-time Discord tooling,
scraping and database sync. Monitoring with sub-second reaction times.
Dashboards and API backends to drive all of it.

Currently reverse engineering binary inventory payloads, and writing up why
nearly every "they're blocking us" diagnosis turned out to be my own bug.

Available for project work and monthly retainers.
