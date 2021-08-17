## WAF - Azure Monitor Scoping

## Three pillars of focus 
### Monitor Applications   
    - Application insights
    - Virtual Machines
    - Networking
    - Applications

### Monitor Infrastructure
    - Log Analytics 
    - Monitoring Agents 
        - Microsoft Monitoring Agent (MMA)
        - System Center Operations Manager (SCOM)
        - DataFlux Telegraph
        - OMS 
### Monitor Network
    - Network Insights
    - Network Watcher
        - Connection Monitor
    - ExpressRoute
    - Application Gateway

## Post-Discovery Scoping 
Below is the information that needs to be collected about the customer.

### Preliminary Questions
Has the customer previously done a Well-Architechted Assessment?
   * If not, then the technical resource will need to complete the SLA pathwise analysis module.
   * Similarly, they will need to complete the failure mode analysis module as well.
### General Infrastructure Questions

What is the customers current infrastructure in Azure?

Where is the log data being sent?

How many Log Analytics Workspaces does the customer have?

Which applicaion is going to be identified as part of the Well-Architechted Assessment? 
 * This is an intergral question for the scoping of this workshop becuase some services have certain requirements in order to monitor them, especially if considering using Insights.
    
What monitoring capabilities does the customer want to add?

What problems is the customer looking to solve?
    * Can Azure policy be used to deploy against whats currently in place?
    
Does the customer have any monitoring pain points?

What monitoring is currently being done in the customers enviroment, if any?
     * On-premises workloads monitoring?
     * Azure workloads monitoring?
     * 3rd party cloud monitoring?

    * If monitoring VMs:
        * Do you have VMs set up they want to monitor?
        * What OS?
            * This will determine the monitoing agent you will use;
            * Log Analytics agent
            * Dependency agent
            * Azure Diagnostic agent
            * Telegraf agent
        * Are they custom, migrated, out of box?
        * What type of data do you want to collect?
        
    * If the customer is using containers:
        * Have the customer's containers been configured for monitoring?
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
