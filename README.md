# DDOS_Attack_Sequence.md
```mermaid
sequenceDiagram
    participant Attacker as "Attacker\n(Hacker man doing the DDoS attack)"
    participant BotNet as "BotNet\n(The compromised computers sending malicious traffic)"
    participant WebServer as "WebServer\n(The Companies website)"
    participant Firewall as "Firewall\n(The network defence system trying to filter our the malicious traffic)"

    Attacker->>BotNet: Sends command to initiate DDoS attack
    BotNet->>WebServer: Floods with malicious bots
    WebServer->>Firewall: Receives incoming traffic
    Firewall->>Firewall: Analyzes traffic for malicious traffic
    Firewall-->>WebServer: Filters out malicious traffic
    Firewall->>WebServer: Blocks IP addresses sending the traffic
    WebServer->>Firewall: Thanks homie 
 ```
