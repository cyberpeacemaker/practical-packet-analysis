# Captured Files
- capture various times, save them, analyze(merge) them all at once
- thin bloated pcap `Export Speficied Packets`
# Packets
- [display filter, Hex, String]
- print for [analysis, report]
- `B, N`
# Time Display Format
- time refrence `T`
- time shift [Time Offset, Clock Skew/Drift]
# Capture Option
- input
- output
- option 
# Filters
- Capture Filter syntax: Berkeley Packet Filter (BPF) | libpcap/WinPcap
    - [Expression, Preimitive, Operator, Qualifier]
    - EX: `dst host 192.168.0.10 && tcp port 80`
    - examine every byte
    - EX: `tcp[13] & 4 == 4`, `icmp[0:2] == 0x0301`
- Display Filer (broadcast suited)
    - protocal.feature.subfeature
    - [and, or, nor, not]
- store fileters (in a configuration profile)