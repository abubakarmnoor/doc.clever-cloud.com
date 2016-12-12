---
title: Application lifecycle
position: 4
shortdesc: Get informations about your application using the Clever Cloud CLI tool
tags:
- cli-setup
keywords:
- cli
- clever-tools
- logs
- lifecycle
- status
- activity
- list
---

# Informations about your application

### Get continuous logs from your application

You can see logs with the command down below.

    clever logs

You can also add a flag `--before` or `--after` followed by a date (ISO8601 format).

    # Here is an example
    clever logs --before 2016-08-11T14:54:33.971Z

### Listing linked applications

You can list your linked applications with `clever applications`. For each application, the command shows you the alias, the id and the deployment url.

    # List linked applications
    clever applications

    # List only application aliases
    clever applications --only-aliases

### Status of your application

Clever-tools can show you the status of an application on Clever Cloud using `clever status`. This command shows you if the application is running or stopped and informations about the scalability of your application.

### Activity of your application

`clever-tools` can show you the activity of an application. For each deployment, you get :

* date and time of deployment
* status (OK or FAIL)
* action (DEPLOY or UNDEPLOY)
* commit ID
* tool used to deploy (Git/Console/clever-tools/...)

In order to show those informations, use :

    # Show the last 10 deployments
    clever activity

    # Show all deployments
    clever activity --show-all

    # Show deployments and track new ones
    clever activity --follow