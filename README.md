# DDOS_Attack_Sequence.md
sequenceDiagram
    participant Attacker as "Attacker\n(Individual/group orchestrating the DDoS attack)"
    participant BotNet as "BotNet\n(Network of compromised devices sending malicious traffic)"
    participant WebServer as "WebServer\n(Target server/service being attacked)"
    participant Firewall as "Firewall\n(Network defense system filtering and analyzing traffic)"

    Attacker->>BotNet: Sends command to initiate DDoS attack
    BotNet->>WebServer: Floods with malicious requests
    WebServer->>Firewall: Receives incoming traffic
    Firewall->>Firewall: Analyzes traffic for anomalies
    Firewall-->>WebServer: Filters out malicious requests
    Firewall->>WebServer: Blocks IP addresses identified as malicious
    WebServer->>WebServer: Attempts to process remaining legitimate requests (overwhelmed)
