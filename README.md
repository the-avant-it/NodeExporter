# Common.NodeExporter

Role for installing prometheus VM metrics exporter

# Changelog

## 2.2.3

Fix vars in unitfile 

## 2.2.2

- Fix critical error!

## 2.2.1

- Move parametr  memory_limit to group vars
- Add extra_arguments to start service

```yaml
node_exporter:
  memory_limit: 100M
  extra_arguments: ""
```

## 2.2.0

- Add Create cron for starting node exporter in case if systemd is not available at a time when role is running
- Add optional var ignore_systemd_errors

## 2.1.2

- #T2326 🐫 Доработать роль установки нод экспортеров чтобы они не падали когда сервер перегружен 

## 2.1.1

- Add /bin/sh -c 

## 2.1.0

- Add optional node_exporter.version variable

## 2.0.0

- Do not run the role if it executed recently
- [BREAKING CHANGE] Add node_exporter. prefix to variables

# Documentation for 2.1.0

## Variables

### Non-secret

All variables are set by default

```yaml
node_exporter: 
  # Optional
  exporter_port: 9100
  # Optional
  version: v1.1.2
  # Optional
  binaries_file_name: node_exporter-1.1.2.linux-amd64
  # Optional. If the role already succeeded recently, do not execute task in it for an hour
  enable_cache: yes
  # Optional. When cache_key changes the cache wil reset
  cache_key: default  
  memory_limit: 100M
  extra_arguments: ""
```  

### Secret

```yaml

```
