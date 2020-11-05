# P U L S A R 

Roava helm chart for Apache Pulsar Helm Chart based on the officially supported Helm Chart for installing Apache Pulsar on Kubernetes.

Read [Deploying Pulsar on Kubernetes](http://pulsar.apache.org/docs/en/deploy-kubernetes/) for more details.

## Pushing to GCR

Commiting to this Repo
Please commit to the repoistory following the instructions below.

The tag used will be applied to the image when pushed to gcr.io

```sh
$ git commit -a -m "msg"
$ git tag -a <semVar-tag> -m <message>     # create a new annotated tag
$ git push origin <semVar-tag>             # push individual tag

# git tag -a 2.6.1 -m "my commit message"
# git push origin 2.6.1
```

## Features

This Helm Chart includes all the components of Apache Pulsar for a complete experience.

- [x] Pulsar core components:
    - [x] ZooKeeper
    - [x] Bookies
    - [x] Brokers
    - [x] Functions
    - [x] Proxies
- [x] Management & monitoring components:
    - [x] Pulsar Manager
    - [x] Prometheus
    - [x] Grafana

It includes support for:

- [x] Security
    - [x] Automatically provisioned TLS certs, using [Jetstack](https://www.jetstack.io/)'s [cert-manager](https://cert-manager.io/docs/)
        - [x] self-signed
        - [x] [Let's Encrypt](https://letsencrypt.org/)
    - [x] TLS Encryption
        - [x] Proxy
        - [x] Broker
        - [x] Toolset
        - [x] Bookie
        - [x] ZooKeeper
    - [x] Authentication
        - [x] JWT
        - [ ] Mutal TLS
        - [ ] Kerberos
    - [x] Authorization
- [x] Storage
    - [x] Non-persistence storage
    - [x] Persistence Volume
    - [x] Local Persistent Volumes
    - [ ] Tiered Storage
- [x] Functions
    - [x] Kubernetes Runtime
    - [x] Process Runtime
    - [x] Thread Runtime
- [x] Operations
    - [x] Independent Image Versions for all components, enabling controlled upgrades

