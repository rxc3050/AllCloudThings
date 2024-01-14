# Networking/VPC concetps in AWS


## Concepts

- 
- Inbound/Outbound
- Response and Request
    - A request is sent to a server and response is expected based on the inbound and outbound rules of the server. 
- Stateful vs Stateless
    - Stateful : no additional rules are needed for response traffic
        -  think of response and request. Stateful allows outbound if inbound is enabled and vice-versa. 
    - Stateless: rules have to be setup for both response and request traffic(inbound and outbound.) 
        - rules have to enabled for both inbound and outbound.   

## Security Groups

- SG's are Stateful. 

## NACL's

- 