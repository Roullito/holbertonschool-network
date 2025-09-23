# Diagram

```mermaid
flowchart TD
  Browser[Browser] -->|Resolve www.google.com| DNSR[DNS Resolver]
  DNSR -->|A or AAAA record| Browser
  Browser -->|TCP 443 HTTPS| FW[Firewall allowing 443]
  FW --> LB[Load Balancer]
  LB --> WS[Web Server]
  WS --> APP[Application Server]
  APP --> DB[Database]
  note right of Browser: Encrypted via TLS
```
