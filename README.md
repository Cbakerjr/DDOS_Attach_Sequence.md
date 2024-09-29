# DDOS_Attach_Sequence.md
# DDoS Attack Sequence Diagram

```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall

    Attacker->>BotNet: Send attack command
    BotNet->>WebServer: Send massive traffic
    BotNet->>Firewall: Bypass or overwhelm defenses
    Firewall-->>WebServer: Traffic analysis
    Firewall->>WebServer: Block malicious IPs
    WebServer-->>Firewall: Report unusual activity
    WebServer-->>BotNet: Request timeout/errors
    BotNet->>Attacker: Report success/failure
