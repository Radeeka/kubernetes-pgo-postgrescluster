# Deploying PostgreSQL Cluster with PGO Operator

This repository contains a Kubernetes manifest file (`postgrescluster.yaml`) that can be used to deploy a PostgreSQL database cluster using the PGO (Postgres Operator) by Crunchy Data. PGO is a Kubernetes operator that simplifies the deployment, management, and scaling of PostgreSQL clusters within a Kubernetes environment.

## Table of Contents

- [Introduction](#introduction)
- [File Description](#file-description)
- [Usage](#usage)
- [Prerequisites](#prerequisites)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Deploying and managing PostgreSQL databases in a Kubernetes environment can be complex. PGO simplifies this process by providing a Kubernetes-native way to manage highly available, fault-tolerant PostgreSQL clusters. With PGO, you can leverage Kubernetes' powerful orchestration capabilities to ensure that your PostgreSQL databases are always available and reliable.

## File Description

- `postgrescluster.yaml`: This Kubernetes manifest file defines the PostgreSQL cluster configuration using the PGO Operator. It specifies how the cluster should be created, the desired state, and any custom settings or configurations.

## Usage

To deploy a PostgreSQL cluster using the provided `postgrescluster.yaml` file, follow these steps:

1. Clone this repository to your local machine:
   ```shell
   git clone https://github.com/radeeka/kubernetes-pgo-postgrescluster.git
   ```

2. Change into the cloned directory:
   ```shell
   cd kubernetes-pgo-postgrescluster
   ```

3. Ensure that you have the necessary prerequisites (see below).

4. Customize the `postgrescluster.yaml` file to match your specific requirements, such as specifying the PostgreSQL version, resources, storage, and any other cluster-specific settings.

5. Deploy the PostgreSQL cluster to your Kubernetes environment:
   ```shell
   kubectl apply -f postgrescluster.yaml
   ```

6. Monitor the deployment progress and verify that the PostgreSQL cluster is running successfully:
   ```shell
   kubectl get postgresclusters
   ```

### Prerequisites

Before using this manifest file to deploy a PostgreSQL cluster with PGO, make sure you have the following prerequisites in place:

- A Kubernetes cluster up and running.
- PGO Operator installed in your Kubernetes cluster. You can find installation instructions in the official PGO documentation.

## Customization

The `postgrescluster.yaml` file can be customized to suit your specific PostgreSQL cluster requirements. Be sure to review the [PGO documentation](https://access.crunchydata.com/documentation/postgres-operator/latest/index.html) for details on available configuration options and best practices.

## Contributing

Contributions to improve and enhance this repository are welcome. If you encounter issues, have suggestions, or want to contribute improvements, please open an issue or submit a pull request following our [contribution guidelines](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](LICENSE), allowing you to use, modify, and distribute the Kubernetes manifest file according to the terms of the license.
