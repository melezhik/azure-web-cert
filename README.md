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


# Dry run mode

Set config<dry-run> to true:

    $ cat config.pl  

    {

      dry-run => True,
      # Other params
    }

In this mode ARM templates are generated, but not applied

# Author

Alexey Melezhik
