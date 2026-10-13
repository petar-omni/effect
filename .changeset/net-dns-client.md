---
"effect": patch
"@effect/platform-node-shared": patch
"@effect/platform-node": patch
"@effect/platform-bun": patch
"@effect/platform-deno": patch
---

Add an experimental `DnsClient` module to `effect/net` with UDP, TCP, and DNS over HTTPS transports.

Add `Dns.Unknown` records for record types without their own record value and for data that a record type cannot represent.

Breaking change to the experimental `Dns` module: `Dns.Cname` targets are now `string` text names like `Dns.Ptr` hosts, instead of `Host.DomainName`.
