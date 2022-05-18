# helmfile-blog

[![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

Source code for Blog on Helmfile

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contributing](#contributing)
- [License](#license)

## Install

Install kubectl, helm, helmfile
```
brew install helm
brew install helmfile
```
Make sure you have configured ./kube/config file to proper Kubernetes cluster

## Usage

1. Update the ./sops.yaml file to have proper AWS KMS Keys
2. Use this command,
```
helmfile --environment staging --interactive --selector service=microservice-1 apply
helmfile --environment production --interactive --selector service=microservice-2 apply
```

To delete the helm chart,
```
helm delete microservice-1
helm delete microservice-2
```

## Maintainers

[@worldofprasanna](https://github.com/worldofprasanna)

## Contributing

PRs accepted.

Small note: If editing the README, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

MIT © 2022 Prasanna V
