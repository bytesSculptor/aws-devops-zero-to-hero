
# Day-26 | AWS Load Balancers | ALB vs NLB vs GWLB | Detailed Comparison 


## Introduction [(00:00:00)](https://www.youtube.com/watch?v=bCS9m5RVPyo&t=0s)


- Load balancers, such as [[Amazon Web Services | AWS]]'s Application Load Balancer (ALB), Network Load Balancer ([[Network load balancing | NLB]]), and Gateway Load Balancer (GWLB), distribute traffic across multiple servers to ensure high [[Availability | availability]] and scalability of applications.
- ALB operates at the application layer (layer 7) for [[HTTP]] and [[HTTPS]] traffic, NLB operates at the transport layer (layer 4) for [[Transmission Control Protocol | TCP]] and [[User Datagram Protocol | UDP]] traffic, and GWLB operates at the network layer (layer 3) for traffic between VPCs or on-premises networks.
- Load balancers manage incoming requests using techniques like Round Robin to ensure high availability and minimize downtime.
- Different load balancers support various load balancing techniques, such as ratio-based and weight-based load balancing.
- The seven layers of the OSI model describe the journey of a packet from a client to a server and back, covering different stages of data communication.



## Application Layer [(00:07:45)](https://www.youtube.com/watch?v=bCS9m5RVPyo&t=465s)


- Load balancers distribute incoming network traffic across multiple servers.
- Different load balancers operate on different layers of the OSI model:
- Application Load Balancer (ALB) operates at layer 7 (application layer) and is used for [[HTTP]] traffic load balancing based on factors like host, path, or domain.
- Network Load Balancer ([[Network load balancing | NLB]]) operates at layer 4 (transport layer) and is used for load balancing based on IP addresses and ports.
- Global Accelerator (GWLB) is a different service that improves application [[Availability | availability]] and performance by routing traffic through a global network of edge locations.
- ALB can perform various routing mechanisms based on HTTP requests, such as ratio-based routing.
- ALB can perform SSL offloading, initiating a secure connection to servers even if a plain HTTP request is received.
- ALB can perform re-encryption and pass-through of different SSL mechanisms.
- ALB is more expensive and slightly slower than other load balancers due to its advanced capabilities and ability to intercept and analyze [[HTTP]] requests.



## NLB [(00:23:02)](https://www.youtube.com/watch?v=bCS9m5RVPyo&t=1382s)


- Application Load Balancer (ALB) operates at layer 7, allowing for request routing based on HTTP requests.
- Network Load Balancer ([[Network load balancing | NLB]]) operates at layer 4, focusing on transport layer routing for applications like game servers and streaming platforms that require low latency and high data transmission. NLB is cost-effective, fast, and commonly used in game servers, streaming platforms, and video streaming platforms.
- Gateway Load Balancer (GWLB) is suitable for virtual appliances like [[Virtual private network | VPNs]] and firewalls, as it handles specific traffic that ALB and NLB cannot manage. GWLB offers high security by sending encrypted packets to virtual appliances, making it suitable for VPN and firewall applications.
- NLB is ideal when layer 7 load balancing is not required or when minimizing traffic delays is crucial, such as in [[YouTube]] or content streaming platforms. NLB can create sticky sessions, ensuring uninterrupted streaming of long videos by directing all requests from a user to the same server.



## Outro [(00:31:26)](https://www.youtube.com/watch?v=bCS9m5RVPyo&t=1886s)


- Use NLB for content streaming platforms.

