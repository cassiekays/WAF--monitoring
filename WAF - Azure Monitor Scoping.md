## WAF - Azure Monitor Scoping
### Post Discovery scoping 
•	What is your current infrastructure in Azure?
* Where is the logging going?
* Are there multiple log analytics workspaces?
* what applicaion is going to be identified as part of the WAF assessment? (this is an intergral question for the scoping of this workshop becuase certain services have certain requirements in order to monitor them, especially if considering using Insights)
    * If monitoring VMs:
        * do they have VMs set up they want to monitor?
        * what OS?
        * are they custom, migrated, out of box?
        *
    * If monitoring containers:
        * do they containers set up to monitor?
    * If Load Balancers:
        * Do they have load balancers that are set up to monitor?
        * what SKU are they?

•	On premises workloads monitoring?
* Azure workloads monitoring?
* 3rd party cloud monitoring?
* What capabilities are you looking to add, and/or
* What problems are you looking to solve?
    * Can Azure policy be used to deploy against whats currently in place?

## Three pillars of focus 
### Monitor your applications   
    - application insights

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

### important questions to ask
