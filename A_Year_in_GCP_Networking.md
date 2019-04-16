# Google Cloud Next 2019: A Year in GCP Networking
#gcp #cloud

- https://www.youtube.com/watch?v=gNx2iMhOm7Q

- Global VPC - 19 regions 1 VPC
	- uses same backbone
	- private connections
	- no VPN or peering connections or external IDs
- Private Google access for on -prem
	- reach google apis through vpn or interconnect connection
- Cloud DNS private zones
	- simple to manage internal DNS solution
	- DNS queries restricted to private networks
- Cloud DNS Forwarding (beta)
	- link on-prem and cloud DNS servers
- Network service tiers
	- premium: traffic over Google’s backbone
	- standard: cheaper but comparable to other clouds backbone
	- premium: all traffic goes through Google backbone as far as it can until it needs to leave to go to the internet; usually in the same town as the external entity
	- premium: 7kbps
	- standard: 4kbps
- Cloud NAT
	- control outbound accèss of your instances in a VPC
- VPC flow logs
	- automatic logging of all network payloads to stackdriver
	- annotated by Google with info such as Geo-location, etc.

