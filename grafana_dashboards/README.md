# System & Performance Monitoring Dashboards for Grafana

This repository contains a collection of pre-configured Grafana dashboards designed to monitor key system performance metrics. These dashboards are built to work with a **Prometheus** data source that scrapes data from the **Node Exporter**.

Whether you're monitoring a single machine (`localhost`) or a whole fleet of remote servers, these dashboards provide a clear and detailed view of your system's health.

---

## 📊 Dashboards Included

The dashboards are categorized by the primary metric they monitor: CPU, Disk, Filesystem, and RAM.

### 🖥️ CPU Monitoring
- **Cpu for all machine.json**: Provides an aggregated overview of CPU utilization across all monitored machines. Ideal for spotting fleet-wide performance issues.
- **Cpu performance by localhost.json**: A detailed dashboard focusing on the CPU performance of the local machine where Grafana/Prometheus might be running.
- **Cpu performance by remote machine.json**: A drill-down view for analyzing the CPU performance of a single, specific remote machine.

### 💾 Disk I/O Monitoring
- **Disk performance for all machines.json**: Aggregated view of disk I/O operations (reads/writes, latency) across your entire infrastructure.
- **Disk performance of localhost.json**: In-depth disk I/O metrics for the local machine.
- **Disk performance by remote machine.json**: Focuses on the disk performance of a selected remote machine, perfect for troubleshooting I/O bottlenecks.

### 📂 Filesystem Monitoring
- **Filesystem for all machines.json**: Monitors filesystem usage (space used, space available) for all partitions across all machines.
- **Filesystem of localhost.json**: Detailed filesystem usage statistics for the local machine.
- **Filesystem by remote machine.json**: A specific view of the filesystem usage on a single remote machine.

### 🧠 RAM Monitoring
- **RAM of all machines.json**: An overview of memory consumption across the entire fleet of monitored machines.
- **RAM of localhost.json**: Detailed memory usage metrics (used, free, cached, swapped) for the local machine.
- **RAM of remote machine.json**: A focused dashboard to analyze the memory usage patterns of a specific remote machine.

---

## ✅ Prerequisites

To use these dashboards, you will need:
1.  **Grafana**: An up-and-running Grafana instance.
2.  **Prometheus**: A configured Prometheus instance to be used as a data source in Grafana.
3.  **Node Exporter**: The [Prometheus Node Exporter](https://github.com/prometheus/node_exporter) must be installed and running on all machines you wish to monitor (including `localhost` and all remote machines). Prometheus must be configured to scrape metrics from these exporters.

---

## ⚙️ How to Use

You can import these dashboards into your Grafana instance using one of the following methods.

### Method 1: Manual Import (Recommended for quick setup)
1.  In the Grafana UI, go to the **Dashboards** section (four squares icon on the left sidebar).
2.  Click on **New** -> **Import**.
3.  Click the **Upload JSON file** button and select the dashboard file you want to import, or simply copy the content of a JSON file and paste it into the text box.
4.  Click **Load**.
5.  On the next screen, you can change the dashboard name and, most importantly, **select your Prometheus data source**.
6.  Click **Import**, and the dashboard will be ready to use.

### Method 2: Provisioning (Recommended for automated setups)
For automated, code-driven Grafana setups, you can use the provisioning feature.
1.  Copy the JSON files from this repository into your Grafana's designated dashboard provisioning directory (e.g., `/etc/grafana/provisioning/dashboards/`).
2.  Update your `dashboards.yaml` configuration file to point to this directory.
3.  Restart your Grafana instance. Grafana will automatically detect and load the dashboards.

For more details, please refer to the [official Grafana provisioning documentation](https://grafana.com/docs/grafana/latest/administration/provisioning/#dashboards).

---

## 🤝 Contributing

Contributions are welcome! If you have an improvement for an existing dashboard or want to add a new one, feel free to create a Pull Request. Please make sure to test your changes before submitting.

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.
