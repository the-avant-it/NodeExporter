# Common.NodeExporter

Role for installing prometheus VM metrics exporter

# Changelog

## V2.0.0

- Do not run the role if it executed recently
- [BREAKING CHANGE] Add node_exporter. prefix to variables

# Documentation for V2.0.0

## Variables

### Non-secret

All variables are set by default

```yaml
node_exporter: 
  exporter_port: 9100
  binaries_file_name: node_exporter-1.1.2.linux-amd64
  # If the role already succeeded recently, do not execute task in it for an hour
  enable_cache: yes
  # When cache_key changes the cache wil reset
  cache_key: default  
```  

### Secret

```yaml

```