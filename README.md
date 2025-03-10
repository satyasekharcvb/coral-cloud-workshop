# Coral Cloud Resorts

[![CI](https://github.com/trailheadapps/coral-cloud/actions/workflows/ci.yml/badge.svg)](https://github.com/trailheadapps/coral-cloud/actions/workflows/ci.yml)

![App logo](docs/gfx/app-logo.png)

Welcome to Coral Cloud Resorts, a sample hospitality application. Coral Cloud Resorts is a fictional resort that uses Agentforce, Data Cloud, and the Salesforce Platform to deliver highly personalized guest experiences. Explore ways to bring agents into business workflows, including new smart automation capabilities, content generation, and summarization.

The Coral Cloud Resorts app showcases **Data Cloud**, **Agents** and **Prompts**.


## Installation



#### Salesforce CLI

[Install the Salesforce CLI](https://developer.salesforce.com/tools/salesforcecli) or check that your installed CLI version is greater than `2.56.7` by running `sf -v` in a terminal.

If you need to [update the Salesforce CLI](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_update_cli.htm), either run `sf update` or `npm install --global @salesforce/cli` depending on how you installed the CLI.



### Steps: Base metadata deployment

1. Clone this repository:

    ```bash
    git clone https://github.com/trailheadapps/coral-cloud
    cd coral-cloud
    ```

1. Authorize your org with the Salesforce CLI, set it as the default org for this project and save an alias (`coral-cloud` in the command below).

    ```bash
    sf org login web -s -a coral-cloud
    ```

1. Deploy the base app metadata.

    ```bash
    sf project deploy start -d cc-base-app
    ```

1. Assign the Coral Cloud permission set to the default user.

    ```bash
    sf org assign permset -n Coral_Cloud
    ```

1. Import some sample data.

    ```bash
    sf data tree import -p ./data/data-plan.json
    ```


1. If your org isn't already open, open it in the browser now:

    ```bash
    sf org open
    ```


