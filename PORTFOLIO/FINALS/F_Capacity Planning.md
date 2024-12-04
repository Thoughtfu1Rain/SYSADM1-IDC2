+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 67308196f5544571bf955c7bc1fe270f |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: CAYBOEN, KIMI & LAURIANO,  | DATE PERFORMED:        | /50      |
| RYAN                             | 11/28/2024             |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 12/03/2024             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Capacity Management & Planning

# Part 2. Network Scalability Analysis

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

![](vertopal_67308196f5544571bf955c7bc1fe270f/media/image2.webp){width="6.4774300087489065in"
height="4.904000437445319in"}

**NETWORK ANALYSIS**

1)  **Limited Scalability of the Edge Router**

-   The limited scalability of the single edge router poses a
    significant bottleneck, as it may struggle to handle 5x the normal
    traffic during peak times. This can result in traffic spikes
    overwhelming the router, leading to slowdowns or outages.

2)  **Lack of Redundant Links**

-   The absence of redundant links between devices increases the risk of
    downtime in the event of a failure. If the edge router, core switch
    (5500), or any critical link fails, it could cause significant
    disruptions to the network.

3)  **Insufficient Load Balancing**

-   The lack of a load balancer to distribute incoming traffic across
    servers creates a risk of uneven traffic distribution. This could
    lead to some servers becoming overloaded while others remain
    underutilized, reducing overall performance.

4)  **Underutilized VLAN Segmentation**

-   Although VLANs are implemented, their segmentation is underutilized,
    as there is no clear separation for roles like caching, databases,
    and security. This may cause critical traffic, such as database
    queries, to compete with less important traffic, like image loads,
    resulting in increased latency.

5)  **Insufficient Bandwidth per Server**

-   Each server is limited to 1Gbps bandwidth, which may be insufficient
    to handle high volumes of requests during a traffic surge. This
    inadequate bandwidth can cause delays and negatively impact user
    experience.

6)  **Potential for Single Points of Failure**

-   The reliance on a single core switch (5500) creates a potential
    single point of failure. If this switch fails, the entire network
    could become inaccessible, resulting in a complete outage.

7)  **Security Risks**

-   The lack of firewalls, intrusion prevention systems (IPS), or Web
    Application Firewalls (WAF) in the network increases its
    vulnerability to cyber threats. The heightened traffic during peak
    times could attract cyberattacks, such as DDoS or injection attacks,
    leaving the network exposed.

8)  **Lack of Caching and Database Optimization**

-   The absence of caching servers and database replicas adds to the
    network\'s inefficiency. Without these optimizations, servers may
    struggle to handle dynamic requests, leading to slower response
    times and a poor user experience.

**SCALABILITY PLANNING**

**PROPOSED NETWORK DESIGN**

![](vertopal_67308196f5544571bf955c7bc1fe270f/media/image3.png){width="6.627083333333333in"
height="8.389458661417322in"}

1)  **Additional ISP**

-   Added another ISP to enhance network reliability and redundancy.
    This ensures uninterrupted service during ISP outages, improves
    performance through load balancing, and provides increased bandwidth
    for optimized traffic routing.

2)  **Additional Edge Router**

-   Introduced a second edge router to ensure redundancy and efficient
    traffic management. This setup reduces the risk of a single point of
    failure and balances incoming and outgoing traffic.

3)  **Perimeter Firewall**

-   Deployed a perimeter firewall as the first line of defense against
    external threats. It enforces security policies such as IP
    filtering, blocks malicious traffic, and regulates access to and
    from the internet.

4)  **Upgraded Edge Routers**

-   Upgraded the edge routers to support advanced features such as
    Quality of Service (QoS) and improved traffic management.
    Implemented Hot Standby Router Protocol (HSRP) for router redundancy
    to ensure high availability during failures.

5)  **Additional Core Switch**

-   Integrated a second core switch and configured EtherChannel for both
    load balancing and failover. High-speed uplinks (10 Gbps or more)
    were used between the core and access switches for enhanced
    scalability and fault tolerance.

6)  **Layer 2 Switch Enhancements**

-   Upgraded Layer 2 switches with higher bandwidth uplinks (1 Gbps or
    10 Gbps).

-   Introduced redundancy by connecting each switch to multiple core
    switches for failover.

-   Connected each server to its dedicated Layer 2 switch to improve
    fault tolerance and effectively manage traffic.

-   Enabled Link Aggregation Control Protocol (LACP) on uplinks to the
    core switch to handle heavy traffic loads.

7)  **Load Balancer**

-   Added a load balancer to distribute incoming requests evenly across
    servers. This prevents server overload, ensures optimal resource
    utilization, and enhances user experience during traffic surges.

8)  **Failover and Redundancy for Servers**

-   Implemented failover solutions for all critical servers (e.g.,
    database, caching, application, and monitoring servers). Each server
    has a failover pair to ensure seamless operations during hardware or
    software failures.

9)  **Internal Firewall**

-   Placed an internal firewall between the server layer and the core
    network to protect sensitive server traffic. It enforces security
    policies, isolates compromised servers, and prevents lateral
    movement of threats.

10) **Optimized Server Placement**

-   Dedicated servers for specific roles (web, application, database,
    caching, monitoring).

-   Grouped servers into VLANs for role-specific traffic segmentation,
    ensuring efficient resource use and reduced latency.

-   Integrated backup servers to provide redundancy and protect critical
    data.

11) **Monitoring and Threat Detection**

-   Deployed monitoring servers to continuously track network health and
    performance. These servers are paired with intrusion detection and
    prevention systems (IDS/IPS) to proactively identify and mitigate
    threats.

  --------------------------------------------------------------------------------
  Criteria          Excellent \| 10pts      Good \| 7pts      Needs Improvement \|
                                                              4pts
  ----------------- ----------------------- ----------------- --------------------
  **Network         Accurately identifies   Identifies key    Identifies some
  Analysis**        potential bottlenecks,  network           basic network
                    security risks, and     components and    components but lacks
                    capacity limitations.   some potential    a comprehensive
                                            bottlenecks.      analysis.

  **Scalability     Proposes multiple       Proposes some     Proposes limited
  Planning**        relevant solutions and  relevant          scalability
                    provides detailed       scalability       strategies.
                    explanations, including strategies but    
                    potential drawbacks and lacks detail.     
                    benefits.                                 

  **Evaluation of   Proposes comprehensive  Provides a basic  Does not evaluate
  Solutions**       scalability strategies, evaluation of the the proposed
                    including specific      proposed          solutions or
                    recommendations for     solutions, but    provides a
                    hardware upgrades,      lacks depth.      superficial
                    software                                  evaluation.
                    configurations, and                       
                    network optimizations.                    

  **Proposed        Provides a detailed and Provides a basic  Does not provide a
  Design**          well-justified design,  design but lacks  clear and detailed
                    including network       specific details  design.
                    diagrams, configuration and               
                    details, and            justifications.   
                    implementation plans.                     

  **Evaluation and  Provides a thorough     Provides a basic  Does not evaluate
  Justification**   evaluation of the       evaluation of the the proposed
                    proposed solutions,     proposed          solutions or
                    considering factors     solutions, but    provides a
                    like cost, complexity,  lacks depth.      superficial
                    and potential impact.                     evaluation

  Score:                                                      /50
  --------------------------------------------------------------------------------