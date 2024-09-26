# DDOS_Attack_Sequence.md
sequenceDiagram
    participant Attacker as "Attacker\n(Individual/group orchestrating the attack)"
    participant BotNet as "BotNet\n(Network of compromised devices)"
    participant WebServer as "WebServer\n(Target server/service being attacked)"
    participant Firewall as "Firewall\n(Network defense system filtering traffic)"

    Attacker->>BotNet: Sends command to initiate DDoS attack
    BotNet->>WebServer: Floods with malicious traffic
    WebServer->>Firewall: Receives incoming requests
    Firewall->>Firewall: Analyzes traffic for patterns
    Firewall-->>WebServer: Filters out malicious requests
    Firewall->>WebServer: Blocks suspicious IP addresses
    WebServer->>WebServer: Attempts to process remaining requests (overwhelmed)
    WebServer-->>BotNet: Unable to respond (service degraded)

