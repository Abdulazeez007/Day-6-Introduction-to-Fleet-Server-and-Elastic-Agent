# Day-6-Introduction-to-Fleet-Server-and-Elastic-Agent

Imagine deploying an Elastic Agent on 100 Windows machines to monitor PowerShell logs. You log into Kibana, ready to search for logs, only to realize you forgot to configure the agents to forward PowerShell logs to your Elasticsearch instance. Now you have a few options to fix this:

- Manually configure the agent on all 100 endpoints.
- Use Group Policy to update all endpoints with the latest configuration.
- Utilize a Fleet Server to manage all agents from a centralized location.

If you’ve ever been in a similar situation or foresee this as a possible future scenario, then this guide is for you. Let’s dive into the components that make centralized management possible:

## Elastic Agents and Fleet Server

![Alt text](https://raw.githubusercontent.com/Virus192/Day-6-Introduction-to-Fleet-Server-and-Elastic-Agent/refs/heads/main/Images/a.png)


### What is an Elastic Agent?

The Elastic Agent is a unified way to add monitoring for logs, metrics, and other types of data in your environment. It works based on policies that you can update, adding integrations and protections. These policies tell the endpoints what logs should be forwarded to your Elasticsearch or Logstash instance.

### Installation Methods for Elastic Agent

There are two primary ways to install and manage Elastic Agents:

- **Managed by Fleet:** This is the preferred method for ease of use. Once the agent is installed, its lifecycle, policy, and configuration can be managed centrally via the Fleet UI.
- **Standalone Mode:** For advanced users, the agent can be installed and configured manually. This method provides granular control over configuration but lacks the convenience of centralized management.

For this project, I’ll focus on the Fleet Managed Mode, as it allows seamless management of agents across multiple endpoints.

![Alt text](https://raw.githubusercontent.com/Virus192/Day-6-Introduction-to-Fleet-Server-and-Elastic-Agent/refs/heads/main/Images/fleet-server-cloud-deployment.png)

### Recap: ELK Stack Introduction

Before we continue, let’s recall the core components of the ELK Stack:

- **Elasticsearch:** A search and analytics engine.
- **Logstash:** A data processing pipeline for ingesting data from multiple sources.
- **Kibana:** A data visualization and exploration tool.

### Beats vs. Elastic Agents: Which Should You Choose?

A common question arises: What is the difference between Beats and Elastic Agents, and which one should you use?

- **Beats** are lightweight, single-purpose data shippers. There are six types of Beats, each specialized for different data types, such as Filebeat for log files or Metricbeat for system metrics.
- **Elastic Agent** is an all-in-one data shipper that can handle multiple types of data, reducing the complexity of managing several Beats agents.

Both Beats and Elastic Agents send data to Elasticsearch or Logstash. The choice between them depends on your specific use case. If you want a simplified and unified approach, Elastic Agent is the way to go.

### What is a Fleet Server?

A Fleet Server is a centralized component that connects your Elastic Agents to a Fleet. This enables you to manage multiple agents from a single location, making it easy to update policies, add new integrations, and handle data ingestion preferences.

### Benefits of Using Fleet Server

- **Centralized Management:** Easily manage and update the agent’s policy across all endpoints. If you want to add new integrations for data ingestion or adjust where data is forwarded (Elasticsearch or Logstash), you can do it all from the Fleet UI.
- **Seamless Updates:** When a new version of the Elastic Agent is released, you can update all agents from one place. No need to manually go to each endpoint.
- **Simplified Unenrollment:** If you want to unenroll a particular agent, it’s as easy as a few clicks, without the hassle of touching each endpoint individually.

Without a Fleet Server, you would need to explore other, more cumbersome options whenever you want to update an agent’s policy. This can be quite painful, especially if your only option is to do it manually on hundreds of endpoints.

## Conclusion

To sum it up, managing Elastic Agents through a Fleet Server can save you a significant amount of time and effort. It simplifies the process of managing multiple endpoints, updating policies, adding integrations, and handling data flows between Elasticsearch and Logstash.

Now that you know the benefits, it’s time to consider leveraging Fleet Server and Elastic Agents in your own environment. Whether you’re dealing with a small cluster or hundreds of machines, this setup will help keep your data collection and monitoring strategy efficient and effective.
