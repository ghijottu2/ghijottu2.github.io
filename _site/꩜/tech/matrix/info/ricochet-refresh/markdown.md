See inline:

best,
-Richard

> 1. Which software license does Ricochet have? It wasn't quite clear for me.

3-Clause BSD : https://github.com/blueprint-freespeech/ricochet-refresh/blob/main/LICENSE

> 2. Does Ricochet use proprietary libraries?

No

> 3. Which cryptographic primitives does Ricochet use?

Apart from the underlying cryptographic primitives of the Tor network to protect traffic contents,
Ricochet-Refresh also uses ed25519 keys (as described in the tor specs) for onion service identity
verification ( see:
https://github.com/blueprint-freespeech/ricochet-refresh/blob/main/doc/protocol.md#proof )

> 4. Is locally saved data (e.g. contacts) encrypted at rest?

No. It is assumed your hard drive is encrypted as a first line defense but perhaps we should suggest
that explicitly. See: https://github.com/blueprint-freespeech/ricochet-refresh/issues/71

> 5. Does Ricochet utilize certificate pinning?

No

> 6. Is there a directory service and if yes can be modified to enable a MITM attack?

In theory yes, in practice not really. Ricochet-Refresh depends on the tor network for its privacy,
anonymity and security guarantees and as such we depend on this network and associated
infrastructure to work. So, we inherit the same risks and threats any other tor-based applications
face which are primarily denial-of-service based rather than MITM. The Tor Project keeps a close eye
on the composition of the network and actively removes malicious/suspicious nodes from the network (
see: https://community.torproject.org/relay/community-resources/bad-relays/ )

> 7. Can a contact be added without needing to trust a directory server?

There is no Ricochet-Refresh specific infrastructure, so again the only trust required is of the tor
network.

> 8. What is the jurisdiction of the devs/organization?

Germany
