# IPLD Team Planning, Management & Coordination

IPLD is a set of standards and implementations for creating decentralized persistent data-structures that are universally addressable and linkable.

This repo tracks project management issues like our calls or quarterly [OKRs](okr) planning. For general information about IPLD, refer to the [IPLD website](https://ipld.io/) or [the main repo](https://github.com/ipld/ipld).

# Weekly call

We run a an IPLD call every week **Monday 21:00–22:00 UTC**. You also find it on the [IPFS community calendar](https://calendar.google.com/calendar/embed?src=ipfs.io_eal36ugu5e75s207gfjcu0ae84@group.calendar.google.com&ctz=UTC)

Link to join the call: https://protocol.zoom.us/j/935904840 (note: it’s recorded, [live streamed](https://www.youtube.com/c/IPFSbot/live) and public)

Anyone is welcome to join! If it’s fine to come if you just want to learn about IPLD.

The meeting notes are taken on HackMD: https://hackmd.io/PjKSfch8QNOY4uNrnrRbDA

Feel free to add agenda item for the next meeting.

We also archive [the meeting notes of the previous calls](https://github.com/ipld/team-mgmt/tree/master/meeting-notes) for anyone interested (to archive the notes you can use [this helper](https://ipld.github.io/team-mgmt/docs/index.html)).

# Other ways to get involved in IPLD

* Explore the [ipld.io](https://ipld.io/) website

# The Team

This is a list of what people are working on **right now** and also work items that are "on deck" or have been bumped
down each person's priority list. It also captures some of the ongoing responsibilities each person has across the projects.

You'll notice that nobody has more than one high priority item at a time. That's not because they don't work on other things,
but every person on the team is a maintainer of numerous ongoing efforts and as a result only has time for one high priority mid to
long term project effort at a time.

*Last Updated: 10/08/2020*

* @mikeal
  * **`[P0]`** Managing the team (this never changes or gets bumped)
  * *`[maintainership]`* [js-multiformats](https://github.com/multiformats/js-multiformats), [@ipld/block](https://github.com/ipld/js-block), [ipjs](https://github.com/mikeal/ipjs)
  * *`[research-engineering]`* [dagdb](https://github.com/mikeal/dagdb), [ZDAG](https://github.com/mikeal/ZDAG), [simple-dag](https://github.com/mikeal/simple-dag), [ipmd](https://github.com/mikeal/ipmd), [dkv](https://github.com/mikeal/dkv)
* @rvagg
  * **`[P0]`** Fixtures and compliance tests for IPLD protocols.
  * *`[maintainership]`* formats: bitcoin, zcash, eth, [dag-pb](https://specs.ipld.io/block-layer/codecs/dag-pb.html), [dag-cbor](https://specs.ipld.io/block-layer/codecs/dag-cbor.html)
  * *`[maintainership]`* [CAR](https://specs.ipld.io/block-layer/content-addressable-archives.html), [HAMT](https://specs.ipld.io/data-structures/hashmap.html)
  * *`[research-engineering]`* Explore and define how JS IPLD applications are structured.
* @warpfork
  * **`[P0]`** Docs and Specifications.
  * **`[P1]`** self-hosted go codegen emitting types for its own type info; aiming for codegen tool CLI
  * *`[ongoing]`* Interface changes to go-ipld-prime ([notes](https://hackmd.io/g_wnjCq6R265Dz3yoU1j4w))
  * *`[maintainership]`* [go-ipld-prime](https://github.com/ipld/go-ipld-prime), [IPLD Schemas](https://specs.ipld.io/schemas/), [IPLD Selectors](https://specs.ipld.io/selectors/selectors.html)
* @ribasushi
  * **`[P0]`** End-to-end testing and fixes in Lotus for a complete and working [Discovery UI](https://filecoin.io/blog/intro-filecoin-discover/).
  * *`[maintainership]`* aws lotus client infra
  * *`[ongoing]`* numerous filecoin launch related tasks
* @chafey
  * **`[P0]`** [js-graphsync](https://github.com/chafey/js-graphsync)
  * *`[maintainership]`* [dumbo-drop](https://github.com/filecoin-shipyard/dumbo-drop)
* @mvdan
  * **`[P0]`** go HAMT ADL (using go codegen)
  * **`[P1]`** support Rod's fixture and compliance test work
  * **`[P1]`** write a handbook section to outline Go development at PL
* @vmx
  * **`[P0]`** Upstream Rust Multihash/CID efforts and make downstream users ([libp2p](https://github.com/libp2p/rust-libp2p/), [libipld](https://github.com/ipfs-rust/rust-ipld), [Forest](https://github.com/ChainSafe/forest/)) use them.
  * **`[P1]`** Read-only WASM codecs (WASM can be used to traverse formats not natively supported).
  * *`[maintainership]`* rust-ipld, rust-multiformats, js-ipld legacy libaries

## Q4 2020

We expect that most team members this quarter will end up having to shift some of their priorities to support
the Filecoin Launch. As such, we've kept the list of high priority tasks slated for the quarter to a minimum.

The theme this quarter, which we expect to extend into 2021, is "Protocols > Projects." Over the last few years we've
invested a lot of time in libraries that implement IPLD protocols but we've under-invested in the protocols themselves.
Since we've seen a notable number of new implementations, particularly partial implementations, continuing to solve problems strictly
in our implementations is not sufficient to meet the needs of our ecosystem. We'll still be investing in our implementations, 
but we be allocating more time to specifications, test fixtures and compliance suites going forward.

We also need to spend more of our research engineering effort on new protocols, most notably new formats, which can solve
some of the issues we've surfaced with our existing protocols. Some of our protocols are simply not resilient to partial implementations
the way that `multiformats` are and we'd prefer the entire stack to be as resilient as `multiformats`. The easier it is to safely
adopt these protocols the more they'll be adopted and `multiformats` offer us a great example of how this can work when well designed.
