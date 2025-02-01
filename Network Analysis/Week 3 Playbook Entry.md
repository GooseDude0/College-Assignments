Logging and interpreting flow traffic using the statistics tools in Wireshark. 

The main tools for analysing flow traffic are Protocol Hierarchy, Conversations, I/O Graphs, and Flow Graph.

Interpretation

Protocol Hierarchy
  This tool shows a breakdown of the protocols in the capture file and how they relate to each other.

Conversations
  This tool provides a detailed summary of all the network conversations (flows) based on various protocols such as TCP, UDP, etc.

I/O Graphs
  This tool provides a graphical representation of packet traffic over time.

Flow Graph
  This tool shows the sequence of packets exchanged between two hosts in a conversation.

Logging

You can do 2 things to log the traffic for later anaylysis.

1. Exporting Packet Data
  After applying relevant filters to identify flows of interest, you can export packets using File -> Export Specified Packets.

2. Capture Options
  You can also set Wireshark to log specific types of flows during live captures by adjusting Capture Options (under Capture → Options) and specifying the relevant filter to capture the traffic you're interested in.
