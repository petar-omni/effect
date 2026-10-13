---
"effect": patch
"@effect/platform-node-shared": patch
"@effect/platform-node": patch
"@effect/platform-bun": patch
"@effect/platform-deno": patch
---

Add an experimental `DnsClient` module to `effect/net`, a DNS client with UDP, TCP, and DNS over HTTPS transports.

Add `Dns.Unknown` records and `Schema.DnsUnknownRecord` for record types without their own record value.
