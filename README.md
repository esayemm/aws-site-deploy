aws-site-deploy
===============

Deploy static site to AWS S3 and also creates a cloudfront invalidation. This
CLI is meant to be used with sites that are deployed with Route53 -> CloudFront
-> S3. It does not handle provisioning AWS resources for you.

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/aws-site-deploy.svg)](https://npmjs.org/package/aws-site-deploy)
[![CircleCI](https://circleci.com/gh/esayemm/aws-site-deploy/tree/master.svg?style=shield)](https://circleci.com/gh/esayemm/aws-site-deploy/tree/master)
[![Downloads/week](https://img.shields.io/npm/dw/aws-site-deploy.svg)](https://npmjs.org/package/aws-site-deploy)
[![License](https://img.shields.io/npm/l/aws-site-deploy.svg)](https://github.com/esayemm/aws-site-deploy/blob/master/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
* [Releasing](#releasing)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g aws-site-deploy
$ aws-site-deploy COMMAND
running command...
$ aws-site-deploy (-v|--version|version)
aws-site-deploy/0.0.4 darwin-x64 node-v10.10.0
$ aws-site-deploy --help [COMMAND]
USAGE
  $ aws-site-deploy COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`aws-site-deploy deploy`](#aws-site-deploy-deploy)
* [`aws-site-deploy help [COMMAND]`](#aws-site-deploy-help-command)

## `aws-site-deploy deploy`

Upload a static site to AWS S3 and also create a cloudfront invalidation.

```
USAGE
  $ aws-site-deploy deploy

OPTIONS
  -h, --help                               show CLI help
  --awsAccessKeyId=awsAccessKeyId          aws access key id
  --awsEndpoint=awsEndpoint                aws endpoint
  --awsRegion=awsRegion                    aws region
  --awsSecretAccessKey=awsSecretAccessKey  aws secret access key
  --fqdn=fqdn                              (required) fqdn (fully qualified domain name) of the desire deploy
  --source=source                          (required) source folder for static site
```

_See code: [src/commands/deploy.ts](https://github.com/esayemm/aws-site-deploy/blob/v0.0.4/src/commands/deploy.ts)_

## `aws-site-deploy help [COMMAND]`

display help for aws-site-deploy

```
USAGE
  $ aws-site-deploy help [COMMAND]

ARGUMENTS
  COMMAND  command to show help for

OPTIONS
  --all  see all commands in CLI
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v2.1.4/src/commands/help.ts)_
<!-- commandsstop -->

# Releasing

Just run `npm version patch|minor|major` to cut a release to npm.
