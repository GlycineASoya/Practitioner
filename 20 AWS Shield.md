# AWS Shield

* It protects against DDoS (**D**istributed **D**enial **o**f **S**ervice) attacks
* Standard Shield abilities:
  * UDP reflection attacks - an Attacker creates and sends a UDP request to a server with a Target's IP address as a source IP address. The server recieves it and sends UDP response to the source, which is Target. As UDP response size is several than UDP request that generates unwanted traffic (example, DNS request is 64B, DNS response is 3400B (3KB), which is 53 times more than request)
  * SYN floods attacks - an Attacker uses SYN packets without ACK packets to flood the server and thus causes TCP sessions capacity depletion
  * SSL renegotiation attacks - an Attacker exhausts processing power of the target server by using requesting and renegotiation of SSL connection
  * Slow loris (an animal) attacks - an Attacker uses multiple open and maintained HTTP connections causing DDoS type of attack
  * It's available for free for every AWS user
  * It has additional detection/mitigation of DDoS attacks
  * Barely real-time visibility
  * Integrates with AWS WAF
* Advanced Shiled Abilities:
  * Available Globally on all Amazon CloudFront, AWS Global Accelerator, and Amazon Route 53 edge locations

## Integration

* Amazone CloudFront + Amazon Route 53 - protection against all known infrastructure (Layer 3, 4) attacks