---
title: Fivetran integration
excerpt: >-
  Automate the flow of your Recurly Commerce subscription data into your data
  warehouse with Fivetran’s turnkey ELT pipelines—no custom scripts required.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Easily keep your analytics, BI, and data science teams in sync by piping all your Recurly Commerce objects—accounts, subscriptions, transactions, invoices—straight into Snowflake, BigQuery, Redshift, and more.

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          A Fivetran account with a destination warehouse (Snowflake, BigQuery, Redshift, Azure Synapse, etc.)
        </p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          “Read-only” API credentials for your Recurly Commerce site
        </p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          Access to the Fivetran dashboard to configure connectors
        </p>
        <blockquote className="mt-4 pl-4 border-l-4 border-gray-300 italic">
          <p>
            <strong>Note:</strong> Data sync frequency and retention depend on your Fivetran plan and warehouse capacity
          </p>
        </blockquote>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Fivetran integration lets you leverage a pre-built Recurly Commerce connector that automatically extracts raw subscription data, loads it into your data warehouse, and applies your transformations downstream—so you can focus on analytics, not pipelines.

# Key benefits

* **Zero-maintenance pipelines**: Once configured, Fivetran keeps your data up to date—no manual scripts or cron jobs.
* **Broad warehouse support**: Sync into Snowflake, Google BigQuery, Amazon Redshift, Azure Synapse, and dozens more.
* **Consistent schema**: Gain access to all your subscription objects in a structured, ready‑to‑query format without building your own ELT framework.

***

Need help getting started? Contact <a href="mailto:support@recurly.com" target="_blank">[support@recurly.com](mailto:support@recurly.com)</a> for guidance or troubleshooting.