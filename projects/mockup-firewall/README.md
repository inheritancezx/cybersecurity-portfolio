# Mock-up Firewall Program

[Back to portfolio](../../) | [Source repository](https://github.com/inheritancezx/mockupfirewall)

## Objective
Design and build a simulation of an integrated firewall and intrusion detection system to practise packet inspection and rule-based filtering. This was an assignment for the CYBR3000 course at the University of Queensland.

## Environment and tools
- Language: Python
- Traffic types: TCP, UDP, ICMP
- Input: a recorded traffic capture file, so no live network was tested
- Code structure: `appliance.py` (main firewall logic), `support.py` and `translate.py` (helper modules)

## Method
1. Defined 16 rule sets covering TCP, UDP and ICMP packets.
2. Implemented simulated packet capture and validation from the traffic file.
3. Implemented rule-based filtering and traffic control (allow or block).
4. Compared the program output against the expected output file provided with the assignment.
5. Tested DMZ-based and external scenarios.

## Results
- Passed 3 DMZ-based tests, 3 external tests, and all program design constraints.
- program output and report will be presented at the evidence folder

## What I would do differently

- Replace the custom hexadecimal parsing and packet offsets with a tested packet model or a library such as Scapy. Scapy wasn't use as an assignment from lecturer
- Add unit and integration tests covering every rule, packet direction, protocol, malformed packet, and allow/block boundary. Store expected packet fixtures and test the complete `run_appliance()` flow rather than relying only on provided output files.
- Implement connection-state decisions explicitly in a state table rather than combining state checks with individual rule functions. Include a final default-deny rule and make rule priority deterministic.
- Improve runtime reporting with structured allow/drop logs that record timestamp, interface, source and destination, protocol, rule ID, and reason. Replace direct `print()` calls with a configurable logger.
- If expanded beyond the assignment, support multiple capture files, IPv4 fragmentation, ICMP echo/return matching, NAT/PAT translation, and live packet interfaces behind a separate transport abstraction.

## note
this assignment was previously made private per student code of conduct.
However, as it has passed the 10 month mark post-submission, it is allowed to be publicized as a portfolio/own project.