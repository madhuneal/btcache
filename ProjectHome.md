The idea is to install one part of this software somewhere on the network where it is able to passively collect chunks of BitTorrent data passing by using for example port mirroring, passive optical tap, or transparent bridge.

It does not participate in the conversation and only needs to see one side of the TCP stream. It follows the BitTorrent protocols but obviously cannot read into encrypted packets. It can snoop into PPP/L2TP encapsulated payloads.

It will fill up a big storage array with all the pieces it sees, and will also note the ip/port/infohash of all new handshakes it sees.

A second component can then connect back to whichever of the machines it chooses (i.e. your own customers) and offer whichever pieces you have unsolicited.


---


The first component is written and able to process up to ~800Mbps @ ~200,000pps using ~15% of a Xeon 2.4Ghz CPU.

The rest is to be completed.

It's all very alpha-quality at the moment..