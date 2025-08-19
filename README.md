# Monitoring-and-Alerting-System-for-Linux-Machines
This project demonstrates an efficient, low-cost monitoring and alerting system for Linux based machines. It leverages Prometheus and Node Exporter for real-time data collection and Grafana for visualizing performance metrics, enabling proactive identification of issues. Alertmanager ensures timely alert for risk and resource management.

Linux System Monitoring: Prometheus, Grafana, and Alertmanager 🚀
This project is a culmination of my thesis work with Baylon Cloud in Rome. It demonstrates the power and efficiency of a low-cost monitoring solution for Linux machines using a stack of powerful open-source tools: Prometheus, Node Exporter, Grafana, and Alertmanager.

The system proves that you don't need to break the bank to get a complete view of your machine's health and performance.

Key Features ✨
Prometheus & Node Exporter: Efficiently collects critical metrics from Linux hosts with minimal overhead.

Grafana Dashboards: Visualize your machine data in beautiful, real-time dashboards to spot performance issues at a glance.

Proactive Alerting: Alertmanager sends crucial alerts via SMTP with TLS encryption directly to your email, complete with troubleshooting tips to minimize downtime and resource loss. 🚨

Scalable Architecture: The system is designed to monitor remote machines using YAML configuration files, making it easy to add new hosts just by providing their IP addresses.

Security-First Mindset: The entire setup was built on the principle of least privilege. Each service runs as a dedicated system user, drastically reducing potential security risks. 🔒

My Journey: Challenges and Successes 💪
This project was a fantastic challenge! From the initial setup, where I implemented a robust security model, to creating a centralized alerting system, every step was a learning experience. The final alert system, which sends alerts directly to my Google account, was a particularly rewarding part of the process.

This project not only met its initial goals but went above and beyond, integrating key security and efficiency improvements. I'm proud of the result and excited to share it with the community!
