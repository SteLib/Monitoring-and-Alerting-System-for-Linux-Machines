# Prometheus Alerting Rules

This directory contains the alerting rules for the Prometheus monitoring system. These rules are used to detect and notify on various system and service-level issues.

The rules are organized to serve two main purposes: verifying the monitoring setup and monitoring real-world application behavior.

## 🚨 Alert Rules Overview

This collection includes two alerts:

### 1. Test Alert (`TestAlert`)
This is a simple, non-critical alert designed to always be active. Its sole purpose is to help you **verify that the entire alerting pipeline is configured correctly**. If you receive a notification for `TestAlert`, it confirms that Prometheus can successfully fire alerts and that Alertmanager can correctly route them to your chosen notification channels (e.g., Slack, email).

### 2. Real-World Alert (`HighDiskUsage`)
This alert is a practical example for a production environment. It monitors...
  
What makes this alert particularly useful is the inclusion of **troubleshooting guidance directly within the alert's annotations**. When the alert is triggered, the notification will contain a set of initial steps and commands that an on-call engineer can immediately execute to diagnose the problem. This helps to reduce the response time and standardize the initial incident response procedure.

## 🔧 Usage

These rules are loaded by Prometheus and evaluated at regular intervals. When the condition of a rule is met for its specified duration, an alert is fired and sent to the configured Alertmanager instance for notification.
