## WAF - Azure Monitor Scoping
### Post Discovery scoping 
* Has the customer previously done a Well Architechted Framework engagement?
   * If not, then the technical resource will need to complete the SLA pathwise analysis module.
   * Similarly, they will need to complete the failure mode analysis module as well.
* What is your current infrastructure in Azure?
* Where is the logging going?
* Are there multiple log analytics workspaces?
* What applicaion is going to be identified as part of the WAF assessment? (This is an intergral question for the scoping of this workshop becuase certain services have certain requirements in order to monitor them, especially if considering using Insights)
    * If monitoring VMs:
        * Do you have VMs set up they want to monitor?
        * What OS?
            * This will determine the monitoing agent you will use;
            * Log Analytics agent
            * Dependency agent
            * Azure Diagnostic agent
            * Telegraf agent
            * 
        * Are they custom, migrated, out of box?
        * What type of data do you want to collect?
        
    * If monitoring containers:
        * Do they containers set up to monitor?
        * If so where are their containers orchestrated? This will determine what solutions to utilize.
            * Docker Swarm 
            * DC/OS
            * Kubernetes
            * Service Fabric
            * Red Hat OpenShift
            
    * If Load Balancers:
        * Do they have load balancers that are set up to monitor?
        * What SKU are they? Basic or Standard?
        * Are there health probe in place?
        * Do they need to be at certain availbility? This gets more into alerting.

* On premises workloads monitoring?
* Azure workloads monitoring?
* 3rd party cloud monitoring?
* What capabilities are you looking to add, and/or
* What problems are you looking to solve?
    * Can Azure policy be used to deploy against whats currently in place?

## Three pillars of focus 
### Monitor your applications   
    - Application insights
    - Virtual Machines
    - Networking
    - Applications

### Monitor your infrastructure
    - Microsoft Monitoring Agent (MMA)
    - System Center Operations Manager (SCOM)
    - DataFlux Telegraph
    - OMS 
### Monitor your network
    - network insights
    - network watcher
    - connection watcher
    - expressroute
