# Wazuh SIEM Home Lab Architecture

## Overview

This lab consists of the following components:

- Windows Endpoint
- Wazuh Agent
- Wazuh Manager
- Filebeat
- OpenSearch Indexer
- Wazuh Dashboard

## Architecture Diagram

```text
                +------------------+
                |  Windows Client  |
                |   Wazuh Agent    |
                +---------+--------+
                          |
                          |
                          v
                +------------------+
                |  Wazuh Manager   |
                +---------+--------+
                          |
                     alerts.json
                          |
                          v
                +------------------+
                |    Filebeat      |
                +---------+--------+
                          |
                          |
                          v
                +------------------+
                | OpenSearch       |
                |    Indexer       |
                +---------+--------+
                          |
                          |
                          v
                +------------------+
                | Wazuh Dashboard  |
                +------------------+
