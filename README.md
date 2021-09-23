<h1 align="center">The viadee Process Warehouse </h1>
<h1 align="center">Explore what happens in your BPMN processes </h1>

____________________________


<br>

<p align="center">
The viadee Process Warehouse (vPW) enables the analysis of process data that is generated during the execution of process instances on a process engine (e.g. Camunda). The analyst can define his metrics on a functional level (i.e. based on the process model) and visualize them on the process model. The insights gained by him can be used to optimize the process model (cf. BPM lifecycle).
</p>

<br>

<h3 align="center"><a href="/vpw-backend-parent/GETTING_STARTED_DOCKER.md">See Documentation</a></h3>

<h3 align="center"><a href="https://vpw.bpm2.viadee.cloud/">Discover our showcase</a></h3>

<br>

________________________________

<br>

## Showcase
The username and password are both `demo` for our [showcase environment](https://vpw.bpm2.viadee.cloud/).

## Modules
* **[analyzer](/vpw-backend-parent/analyzer)**
    * Spring-Boot-App
    * Provision of a REST API for the vPW frontend
    * Persistence of inventory data (dashboards, indicators) in PostgreSQL
    * Generation of Elasticsearch requests from the frontend requests and processing/preparation of the results
* **[pipeline](/vpw-backend-parent/pipeline)**
    * Spring-Boot-App
    * Receiving process data from Kafka
    * Data preparation, including "breaking up" JSON objects into flat structures
    * Storage/indexing in Elasticsearch
* **[vpw-shared-elasticsearch-config](/vpw-backend-parent/vpw-shared-elasticsearch-config)**
    * Spring boot AutoConfiguration for the Elasticsearch REST client, used by Analyzer and Pipeline.

## Dependency Report 
All licences of reused components can be found [here](MavenSite/index.htlm). 

## Collaboration

The project is operated and further developed by the viadee Consulting AG.
* Community contributions to the project are welcome: Please open Github-Issues with suggestions (or PR), which we can then edit in the team. For contribution please take account of our [contributing guidelines](Contributing/CONTRIBUTING.md).
* We are also looking for further partners who have interesting process data to refine our tooling as well as partners that are simply interested in a discussion about AI and data warehouses in the context of business process automation.

## Commitments

This library will remain under an open source licence indefinitely.

We follow the semantic versioning scheme (2.0.0).

In the sense of semantic versioning, the resulting JSON outputs are the only public "API" provided here. We will keep these as stable as possible.

## Roadmap
This software is considered to be stable and ready for production use.
However, we plan to extend on it if there is demand or if the APIs change.

## License
This project is licensed under the BSD 3-Clause "New" or "Revised" License - see the [LICENSE](https://github.com/viadee/vPW/blob/master/LICENSE) file for details.

<br>

----------------------------

<h3 align="center"><a href="https://www.viadee.de/en/solutions/business-process-management/process-warehouse">GET IN TOUCH WITH US</a></h3>
