---
"effect": patch
"@effect/platform-node-shared": patch
"@effect/platform-node": patch
"@effect/platform-bun": patch
"@effect/platform-deno": patch
---

Add an experimental `DnsClient` module to `effect/net`, a DNS client with UDP, TCP, and DNS over HTTPS transports.

Add `Dns.Unknown` records, made with `Dns.makeUnknownRecord`, and `Schema.DnsUnknownRecord` for record types without their own record value.

`Dns.Cname` targets are text names like `Dns.Ptr` hosts, so CNAME records of classless reverse delegations, such as `1.0/25.2.0.192.in-addr.arpa.`, can be represented.
