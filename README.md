# Azure Update Cert

Create SSl certificate for Azure web application.

# Prerequisites

* Az cli

# Usage

    $ nano config.pl6

    $ sparrowdo --git=https://github.com/melezhik/azure-web-cert.git

# Config.pl6

## az-res-group

Azure resource group

## thumbprint

SSL certificate thumbprint

## domain

Domain name

## kv-id

Key vault identification

## kv-secret-name

Key vault secret name

## app-service

Azure application service name


# Modes

## Dry run mode

In this mode ARM templates are generated, but not executed.

Set config<mode> to `dry-run`:

    $ cat config.pl  

    {

      mode => 'dry-run',
      # Other params
    }

## Validate mode

In this mode ARM templates are generated, validated but not executed.

Set config<mode> to `validate`:

    $ cat config.pl  

    {

      mode => 'validate',
      # Other params
    }


# Author

Alexey Melezhik
