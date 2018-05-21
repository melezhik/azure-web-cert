# Azure Update Cert

Create SSL certificate  and bind domain for Azure web application:

1. Create web SSL certificate for certificate taken from key vault SSL certificate ( `kv-id`, `kv-secret-name` )

2. Create domain (`domain`) for app service (`app-service-name`) and certificate ( `thumbprint` ). Thumbprint should be the thumbprint 
of the certificate created by first step.

# Prerequisites

* Az cli

# Usage

    $ nano config.pl6
    
    {
        domain => "app.domain.foo",
        thumbprint => "ABC010101H0A....",
        az-res-group => "my-az-grp",
        kv-id => "my-kv-storage",
        kv-secret-name => "production-cert",
        app-service => "app"
    }
    
    $ sparrowdo --git=https://github.com/melezhik/azure-web-cert.git --local_mode

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

    $ cat config.pl6  

    {

      mode => 'dry-run',
      # Other params
    }

## Validate mode

In this mode ARM templates are generated, validated but not executed.

Set config<mode> to `validate`:

    $ cat config.pl6  

    {

      mode => 'validate',
      # Other params
    }


# Author

Alexey Melezhik
