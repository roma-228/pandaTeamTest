# 1. CI/CD Process Description

## 1.1. Repository Setup
1. Create a repository and build a simple Python web application.
![pipeline](https://drive.google.com/uc?export=view&id=1CmyqX3EfqUsSxbHAynMeWAq4qSv6VcvR)
## 1.2. Jenkins Configuration
1. Install Jenkins on the server and set up the essential plugins.

## 1.3. [Pipeline Stage Configuration](./Scripts/pipeline.yml)
1. **Clone the repository**
   Retrieve the latest version of the source code.

2. **Build the Docker image**
   Create a Docker image from the application code using a Dockerfile.

3. **Deploy the container**
   Run the container either locally or on a remote server.

4. **Testing**
   - Execute tests to ensure the application's functionality.
![pipeline_view](https://drive.google.com/uc?export=view&id=1DiP-f8O5YdubJzycgoR_MGvyCBeldLE6)
# 2. Monitoring Setup

## 2.1. Installing Grafana and Prometheus

### Prometheus
- Download and configure Prometheus to collect metrics from the server and containers.
- Configure [`prometheus.yml`](./Scripts/prometheus.yml) to scrape metrics from Node Exporter.

### Grafana
- Install Grafana for metric visualization.
- Connect Grafana to Prometheus as a data source.

## 2.2. Creating Dashboards in Grafana
1. Import dashboards for monitoring the health of servers and containers.
   - **Server Monitoring**
   ![ServerMonitoring](https://drive.google.com/uc?export=view&id=1SPazv03auZgzJ_USmn0dcwYms9rgMBAP)
   - **Container Monitoring**
    ![ContainerMonitoring](https://drive.google.com/uc?export=view&id=1Jb1llgWzU3aTcq99c3EsG4SPPO0_Pcyf/view?usp=drive_link)

# 3. Alerting Setup

## 3.1. Creating Alert Rules in Prometheus
Define alert rules to monitor important conditions.
![AlertRules](https://drive.google.com/uc?export=view&id=1an84xggSJTvmdBo9LGPvlSURyNc7TrKW)

## 3.2. Configuring Alertmanager
1. **Alertmanager**
   - Set up Alertmanager to receive alerts from Prometheus and send notifications to designated channels.


