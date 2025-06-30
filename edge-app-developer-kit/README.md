
### Welcome to the App Developer Kit for DeltaV Edge Environment.

# Developer Kit Reference Guide

This document provides detailed descriptions of the files and folders included in the developer kit. Developers can use it as a central reference when building applications on the platform.


- [README.md](./README.md)


Provides an overview of the dev kit and instructions for getting started. Developers should read this file first to understand the structure and usage of the dev kit.
docs/getting-started.md
Step-by-step guide to help developers set up their environment, obtain API keys, and make their first connection to the platform.


## Coding-related

### How-to's:

- [docs/authentication.md](./docs/authentication.md)

Explains how to authenticate with the platform using API keys or tokens. Includes example headers and token lifecycle.

- [docs/rest-api-reference.md](./docs/rest-api-reference.md)

Details all available REST API endpoints, parameters, expected responses, and example usages. Essential for any integration work.

- [docs/opc-ua-guide.md](./docs/opc-ua-guide.md)

Covers how to connect to the platform's OPC UA endpoints, browse the address space, and subscribe to tag updates.

- [docs/data-model.md](./docs/opc-ua-guide.md)

Describes the structure of available data, including tags, metadata fields, and data types. Useful for understanding what data is available.

- [docs/best-practices.md](./docs/best-practices.md)

Guidelines for optimal performance, including rate limiting, efficient data access, and secure coding practices.

### Code samples: 

- [samples/python/rest-api-quickstart.py](./samples/python/rest-api-quickstart.py)

Basic Python script that demonstrates how to make a REST API call to fetch data from the platform.

- [samples/python/opcua-client.py](./samples/python/opcua-client.py)

Example Python script that connects to an OPC UA endpoint and reads data from specific nodes.

- [samples/javascript/rest-api-quickstart.js](./samples/javascript/rest-api-quickstart.js)

JavaScript version of the REST API example, suitable for use in browser apps or Node.js.

- [samples/javascript/opcua-client.js](./samples/javascript/opcua-client.js)

JavaScript OPC UA client example using a Node-compatible OPC UA library.

- [samples/webapp-template/public/.gitkeep](./samples/webapp-template/public/.gitkeep)

Placeholder to ensure the 'public' directory is retained in version control. No developer action needed.

- [samples/webapp-template/src/App.jsx](./samples/webapp-template/src/App.jsx)

Main component of a sample React-based web app. Developers can use this as a starting point for building their own app.

- [samples/webapp-template/src/api.js](./samples/webapp-template/src/api.js)

Contains helper functions to interact with the REST API. Developers can extend this file to include more endpoints.

- [samples/webapp-template/README.md](./samples/webapp-template/README.md)

## Testing and Debugging

Instructions specific to the web app template, such as installation, running locally, and customizing.

- [tools/postman/my-platform-api.postman_collection.json](./tools/postman/my-platform-api.postman_collection.json)

Postman collection file that can be imported into Postman to quickly test REST API endpoints without coding.

- [tools/opcua/UAExpert-config-file.uax](./tools/opcua/UAExpert-config-file.uax)

Configuration file for the UAExpert OPC UA client, preloaded with platform endpoint and sample nodes.

- [tools/cli/tag-browser.py](./tools/cli/tag-browser.py)

Command-line utility for listing available tags and metadata. Useful for quick inspection or automation.

- [sandbox/mock-data/sample-tags.json](./sandbox/mock-data/sample-tags.json)

Mocked tag data for testing and development purposes. Developers can use this without connecting to the live system.

- [sandbox/credentials/sandbox-api-keys.txt](./sandbox/credentials/sandbox-api-keys.txt)

Sample API keys for use in the sandbox environment. Do not use these in production.

## Deployment-related

- [deploy/docker-compose.yml](./deploy/docker-compose.yml)

Docker configuration for running the app and services locally. Developers can use this to simulate production deployment.

- [deploy/deployment-guide.md](./deploy/deployment-guide.md)

Instructions for deploying an app to the platform or a compatible hosting environment.

## Other info

- [support/faq.md](./support/faq.md)

Frequently asked questions to help developers troubleshoot common issues.

- [support/contact.md](./support/contact.md)


Contact information or links to forums and support channels for help.

## Licensing 

- [LICENSE](./LICENSE)

The license under which the dev kit and examples are provided. Developers must adhere to these terms when using or redistributing the kit.
