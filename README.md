# Wazuh Kubernetes

[![Slack](https://img.shields.io/badge/slack-join-blue.svg)](https://wazuh.com/community/join-us-on-slack/)
[![Email](https://img.shields.io/badge/email-join-blue.svg)](https://groups.google.com/forum/#!forum/wazuh)
[![Documentation](https://img.shields.io/badge/docs-view-green.svg)](https://documentation.wazuh.com)
[![Documentation](https://img.shields.io/badge/web-view-green.svg)](https://wazuh.com)

Deploy a Wazuh cluster with a basic Elastic stack on Kubernetes .

## Documentation

The *instructions.md* file describes how to deploy Wazuh on Kubernetes.

## Directory structure

    ├── wazuh-kubernetes
    │ ├── base
    │ │ ├── aws-gp2-storage-class.yaml
    │ │ ├── wazuh-ns.yaml
    │
    │ ├── elastic_stack
    │ │ ├── elasticsearch
    │ │ │ ├── cluster
    │ │ │ │ ├── elasticsearch-api-svc.yaml
    │ │ │ │ ├── elasticsearch-data-sts.yaml
    │ │ │ │ ├── elasticsearch-master-sts.yaml
    │ │ │
    │ │ │ ├── single-node
    │ │ │ │ ├── elasticsearch-api-svc.yaml
    │ │ │ │ ├── elasticsearch-sts.yaml
    │ │ │
    │ │ │ ├── elasticsearch-svc.yaml
    │ │
    │ │ ├── kibana
    │ │ │ ├── kibana-deploy.yaml
    │ │ │ ├── kibana-svc.yaml
    │ │ │ ├── nginx-deploy.yaml
    │ │ │ ├── nginx-svc.yaml
    | |
    │ ├── wazuh_managers
    │ │ ├── wazuh-cluster-svc.yaml
    │ │ ├── wazuh-master-conf.yaml
    │ │ ├── wazuh-master-sts.yaml
    │ │ ├── wazuh-master-svc.yaml
    │ │ ├── wazuh-worker-0-conf.yaml
    │ │ ├── wazuh-worker-0-sts.yaml
    │ │ ├── wazuh-worker-1-conf.yaml
    │ │ ├── wazuh-worker-1-sts.yaml
    │ │ ├── wazuh-workers-svc.yaml
    │ │
    │ ├── README.md
    │ ├── VERSION
    │ ├── CHANGELOG.md
    │ ├── LICENSE
    │ ├── cleanup.md
    │ ├── instructions.md
    │ ├── upgrade.md

## Branches

* `master` branch contains the latest code, be aware of possible bugs on this branch.
* `local-environment` branch contains modifications for deploying on local environments.

## Local development

To deploy a cluster on your local environment (like Minikube or Kind) use the branch [local-environment](https://github.com/wazuh/wazuh-kubernetes/tree/local-environment/minikube)

## Contribute

If you want to contribute to our project please don't hesitate to send a pull request. You can also join our users [mailing list](https://groups.google.com/d/forum/wazuh) or the [Wazuh Slack community channel](https://wazuh.com/community/join-us-on-slack/) to ask questions and participate in discussions.

## Credits and Thank you

Based on the previous work from JPLachance [coveo/wazuh-kubernetes](https://github.com/coveo/wazuh-kubernetes) (2018/11/22).

## License and copyright

WAZUH
Copyright (C) 2016-2020 Wazuh Inc.  (License GPLv2)

## References

* [Wazuh website](http://wazuh.com)
