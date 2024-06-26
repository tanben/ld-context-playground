# LaunchDarkly Context Playground

The LaunchDarkly Context Playground is a simple tool designed to help developers seamlessly design and validate target audiences and rollout strategies for their feature flags. This tool facilitates the design of flag rules and ensures smooth feature rollouts.

## Key Features:
* **Evaluation of Flag Rules**: Test flag rules and rollout strategies effectively for web or mobile SDKs.
* **Context Simulation**: Simultaneously test multiple context instances to validate rollout strategies.
* **Migration Flags**: Evaluate migration flags at the cohort level, helping in transition phases.
* **Comprehensive Reporting**: Generate detailed reports of contexts and evaluation outcomes.

**NOTE**: This app uses client-side SDK. Client-side availability option must be enabled for the flags in your LaunchDarkly project to allow flag evaluation.


### `Important Notice`
To ensure the integrity of your live production data, it is highly recommended to use separate environments in your LaunchDarkly project for testing purposes. This allows you to safely test with sample data without affecting your production environment.

## Prerequisites
Before getting started with the LaunchDarkly Context Playground, ensure that you have the following:

* [LaunchDarkly account](https://launchdarkly.com/start-trial/)
* [Client Side ID](https://docs.launchdarkly.com/home/organize/environments/?q=clientside+id#finding-and-resetting-an-environments-sdk-key-mobile-key-or-client-side-id)
* NodeJS (version >= 18.x)
* React (version 18.x)
* LaunchDarkly React Client SDK (version >= 3.x)

## Instalation
1. Clone this repository to your local machine.
2. Navigate to the project directory and install the required dependencies by running the following command:
    ```
    npm install
    ```


## Usage

1. Make sure to use a sandbox Project and Environment when testing with sample data to avoid mixing sample data with live/production data.
2. Start the application by running the following command:
    ```
    npm start
    ```
3. Open your web browser and visit http://localhost:3000 to access the LaunchDarkly Context Playground.


### Sample data
Sample data used by this application was generated using *FakerJS* and can be found in `./src/data.js`. If you want to create and use a different or custom schema, follow these steps:

1. Update the generateData.js script with your desired schema.

2. Redirect the output to ./src/data.js by running the following command:
    ```
    node generateData.js > ./src/data.js
    ```

### Capabilities
* Single Context Instance: Display feature flags and values.
* Multiple Context Instances: Evaluate flags for several contexts simultaneously.
* Migration Stages: Show migration stages for users.

#### Screenshots
![Single Context Instance](img/singleContext.jpg)
*Display feature flags and values for a single Context instance*



![Multi Context Instance](img/multiContextInstance.jpg)
*Evaluate a flag for multiple Context instances simultaneously*


![Migration stages](img/migration.jpg)
*Evaluate migration flags by segment of users.*