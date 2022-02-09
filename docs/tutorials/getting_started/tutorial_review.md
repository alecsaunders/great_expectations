---
title: 'Review and next steps'
---

<table class="borderless center">
<tr>
    <td>
        <img
          src={require('../../images/universal_map/Gear-active.png').default}
          alt="Setup"
        />
    </td>
    <td>
        <img
          src={require('../../images/universal_map/Arrow.png').default}
          alt="Arrow"
        />
    </td>
    <td>
        <img
          src={require('../../images/universal_map/Outlet-active.png').default}
          alt="Connect to Data"
        />
    </td>
    <td>
        <img
          src={require('../../images/universal_map/Arrow.png').default}
          alt="Arrow"
        />
    </td>
    <td>
        <img
          src={require('../../images/universal_map/Flask-active.png').default}
          alt="Create Expectations"
        />
    </td>
    <td>
        <img
          src={require('../../images/universal_map/Arrow.png').default}
          alt="Arrow"
        />
    </td>
    <td>
        <img
          src={require('../../images/universal_map/Checkmark-active.png').default}
          alt="Validate Data"
        />
    </td>
</tr>
</table>

:::note Prerequisites

- Completed [Step 4: Validate Data](./tutorial_validate_data.md) of this tutorial.

:::

### Review
In this tutorial we've taken you through the four steps you need to be able to perform to use Great Expectations.

Let's review each of these steps and take a look at the important concepts and features we used.

<table class="borderless">
    <tr>
        <td><img src={require('../../images/universal_map/Gear-active.png').default} alt="Setup" /></td>
        <td>
            <h3>Step 1: Setup</h3>
            <p>You installed Great Expectations and initialized your Data Context.</p>
        </td>
    </tr>
</table>

- **Data Context**: The folder structure that contains the entirety of your Great Expectations project.  It is also the entry point for accessing all the primary methods for creating elements of your project, configuring those elements, and working with the metadata for your project.
- **CLI**: The Command Line Interface for Great Expectations.  The CLI provides helpful utilities for deploying and configuring Data Contexts, as well as a few other convenience methods.

<table class="borderless">
    <tr>
        <td><img src={require('../../images/universal_map/Outlet-active.png').default} alt="Connect to Data" /></td>
        <td>
            <h3>Step 2: Connect to Data</h3>
            <p>You created and configured your Datasource.</p>
        </td>
    </tr>
</table>

- **Datasource**: An object that brings together a way of interacting with data (an Execution Engine) and a way of accessing that data (a Data Connector). Datasources are used to obtain Batches for Validators, Expectation Suites, and Profilers.
- **Jupyter Notebooks**: These notebooks are launched by some processes in the CLI.  They provide useful boilerplate code for everything from configuring a new Datasource to building an Expectation Suite to running a Checkpoint.

<table class="borderless">
    <tr>
        <td><img src={require('../../images/universal_map/Flask-active.png').default} alt="Create Expectations" /></td>
        <td>
            <h3>Step 3: Create Expectations</h3>
            <p>You used the automatic Profiler to build an Expectation Suite.</p>
        </td>
    </tr>
</table>

- **Expectation Suite**: A collection of Expectations.
- **Expectations**: A verifiable assertion about data. Great Expectations is a framework for defining Expectations and running them against your data. In the tutorial's example, we asserted that NYC taxi rides should have a minimum of one passenger.  When we ran that expectation against our second set of data Great Expectations reported back that some records in the new data indicated a ride with zero passengers, which failed to meet this expectation.
- **Profiler**: A tool that automatically generates Expectations from a Batch of data.

<table class="borderless">
    <tr>
        <td><img src={require('../../images/universal_map/Checkmark-active.png').default} alt="Validate Data" /></td>
        <td>
            <h3>Step 4: Validate Data</h3>
            <p>You created a Checkpoint which you used to validate new data.  You then viewed the Validation Results in Data Docs.</p>
        </td>
    </tr>
</table>

- **Checkpoint**: An object that uses a Validator to run an Expectation Suite against a batch of data.  Running a Checkpoint produces Validation Results for the data it was run on.
- **Validation Results**: A report generated from an Expectation Suite being run against a batch of data.  The Validation Result itself is in JSON and is rendered as Data Docs.
- **Data Docs**: Human readable documentation that describes Expectations for data and its Validation Results.  Data docs can be generated both from Expectation Suites (describing our Expectations for the data) and also from Validation Results (describing if the data meets those Expectations).

### Going forward

Your specific use case will no doubt differ from that of our tutorial.  However, the four steps you'll need to perform in order to get Great Expectations working for you will be the same.  Setup, connect to data, create Expectations, and validate data.  That's all there is to it!  As long as you can perform these four steps you can have Great Expectations working to validate data for you.

For those who only need to know the basics in order to make Great Expectations work our documentation includes Core Concepts for each step.

For those who prefer working from examples, we have "How to" guides which show working examples of how to configure objects from Great Expectations according to specific use cases.

Finally, we have Deployment Patterns.  These show you how to perform all four steps for implementing Great Expectations with a specific environment and data type.
