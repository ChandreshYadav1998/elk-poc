# ELK Stack Proof of Concept

This repository contains a proof of concept (POC) implementation of the ELK Stack (Elasticsearch, Logstash, Kibana).

## Overview

The ELK Stack is a powerful open-source platform for searching, analyzing, and visualizing data in real-time. This project demonstrates how to set up and configure the three main components:

- **Elasticsearch**: A distributed search and analytics engine
- **Logstash**: A data processing pipeline for ingesting data
- **Kibana**: A visualization tool for exploring and analyzing data

## Components

### Elasticsearch
Elasticsearch is a RESTful, distributed search and analytics engine. It's designed for horizontal scalability, high reliability, and fast search response times.

### Logstash
Logstash is a flexible, open-source data processing pipeline. It ingests data from multiple sources simultaneously, transforms it, and sends it out to your favorite stash.

### Kibana
Kibana lets you visualize your Elasticsearch data and navigate the Elastic Stack. Do anything from tracking query load to understanding the way requests flow through your apps.

## Getting Started

### Prerequisites
- Docker and Docker Compose (recommended for quick setup)
- Or individually installed Elasticsearch, Logstash, and Kibana

### Installation

1. Clone this repository:
```bash
git clone https://github.com/ChandreshYadav1998/elk-poc.git
cd elk-poc
```

2. Start the ELK Stack using Docker Compose:
```bash
docker-compose up -d
```

3. Access the services:
- **Kibana**: http://localhost:5601
- **Elasticsearch**: http://localhost:9200
- **Logstash**: Runs on port 5000 (configurable)

## Configuration

### Docker Compose
See `docker-compose.yml` for the service configuration.

### Logstash Configuration
Pipeline configurations are typically stored in the `logstash/pipeline/` directory.

### Elasticsearch Settings
Configuration details can be found in `elasticsearch.yml` or the Docker Compose environment variables.

## Usage

1. **Index Data**: Send data to Logstash or directly to Elasticsearch
2. **Create Index Patterns**: In Kibana, create index patterns to match your data
3. **Build Visualizations**: Use Kibana's visualization tools to explore and analyze data
4. **Create Dashboards**: Combine multiple visualizations into comprehensive dashboards

## Project Structure

```
elk-poc/
├── docker-compose.yml          # Docker Compose configuration
├── elasticsearch/              # Elasticsearch configuration
│   └── elasticsearch.yml
├── logstash/                   # Logstash configuration
│   ├── logstash.yml
│   └── pipeline/
│       └── default.conf
├── kibana/                     # Kibana configuration
│   └── kibana.yml
└── README.md                   # This file
```

## Troubleshooting

### Elasticsearch won't start
- Check system memory availability
- Verify Docker has sufficient resources allocated
- Review logs: `docker-compose logs elasticsearch`

### Logstash connection issues
- Ensure Elasticsearch is running and accessible
- Check Logstash configuration for correct host/port
- Review logs: `docker-compose logs logstash`

### No data in Kibana
- Verify data is being sent to Logstash/Elasticsearch
- Check index patterns are correctly configured
- Review Kibana logs and browser console for errors

## Documentation

- [Elasticsearch Documentation](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
- [Logstash Documentation](https://www.elastic.co/guide/en/logstash/current/index.html)
- [Kibana Documentation](https://www.elastic.co/guide/en/kibana/current/index.html)

## License

This project is provided as-is for educational and demonstration purposes.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for any improvements.

## Support

For issues or questions, please open a GitHub issue in this repository.
