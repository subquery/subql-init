# SubQuery - Init Package

The Init Package is a scaffold project that you can use as a starting point for developing your SubQuery project. It has the folder structure and key files already created to allow you to focus on defineing your mapping handlers and schemas.

## Preparation

#### Environment

- [Typescript](https://www.typescriptlang.org/) is required to compile projects and define types.  

- Both SubQuery CLI and generated Project have dependencies and require [Node](https://nodejs.org/en/).
     

#### Install the SubQuery CLI

Install SubQuery CLI globally on your terminal by using NPM:

```
npm install -g @subql/cli
```

Run help to see available commands and usage provide by CLI
```
subql help
```

## Initialize the starter package

Inside the directory in which you want to create the SubQuery project, simply replace `project-name` with your project name and run the command:

```
subql init --starter project-name
```
Then you should see a folder with your project name has been created inside the directory, you can use this as the start point of your project. And the files should be identical as in the [Directory Structure](https://doc.subquery.network/directory_structure.html).

## Instal the dependencies
In the project directory, run following command to install all the dependencies.

```shell
# Yarn
yarn

#NPM
npm install
```

## Configure the project

In the project, you will be mainly working on the following files:

- The Manifest in `project.yaml`
- The GraphQL Schema in `schema.graphql`
- The Mapping functions in `src/mappings/` directory

For more information on how to write the SubQuery, 
check out our doc section on [Define the SubQuery](https://doc.subquery.network/define_a_subquery.html) 

## Generate the code

Generate the code with the following command.

```shell
#Yarn
yarn codegen

#NPM
npm run-script codegen
```

## Build the project

In order to index your SubQuery project, it is mandatory to build your project first.
Run this command under the project directory.

```shell
#Yarn
yarn build

#NPM
npm run-script build
```

## Running in Docker

Under the project directory run following command:

```shell
docker-compose pull && docker-compose up
```

## Query the project

Open your browser and head to `http://localhost:3000`. You should see a GraphQL playground open in the browser where you can start to create your own custom queries. For examples on how to create queries please visit our [documention page](https://doc.subquery.network/query/query.html)  
