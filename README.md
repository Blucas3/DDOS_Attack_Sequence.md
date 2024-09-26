# DDOS_Attack_Sequence.md
```mermaid
sequenceDiagram
    participant Attacker as "Attacker(Hacker man doing the DDoS attack)"
    participant BotNet as "BotNet(The compromised computers sending malicious traffic)"
    participant WebServer as "WebServer(The Companies website)"
    participant Firewall as "Firewall(The network defence system trying to filter our the malicious traffic)"

    Attacker->>BotNet: Sends command to initiate DDoS attack
    BotNet->>WebServer: Floods with malicious bots
    WebServer->>Firewall: Receives incoming traffic
    # Firewall->>WebServer: Analyzes traffic for malicious traffic
    # Firewall->>WebServer: Filters out malicious traffic
    # Firewall->>WebServer: Blocks IP addresses sending the traffic
    WebServer->>Firewall: Thanks homie 
 ```

The Attacker picked out the company they wanted to hit and requested to hit the webserver. The bots went after the webserver and were met with the webserver's firewall. The firewall proceeded to analyze the traffic, determine it was not good, and stop it from continuing. Also blocks the IP address so the webserver can't get attacked by the same IP address. 
