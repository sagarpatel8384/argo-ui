# Argo UI

![Argo Image](https://github.com/argoproj/argo/blob/master/argo.png?raw=true)

Argo UI is the web-based user interface for the Argo workflow engine. Argo UI allows users to view Argo workflows running in the cluster, view, container, logs, etc.

Some Argo UI components (such as Workflow DAG viewer, Workflow timeline etc.) are available via the [argo-ui npm package](https://www.npmjs.com/package/argo-ui).

## Build, Run, & Release

1. Install Toolset: [NodeJS](https://nodejs.org/en/download/) and [Yarn](https://yarnpkg.com)
2. Install Dependencies: From your command line, navigate to the argo-ui directory and run `yarn install` to install dependencies.
3. Run: `yarn start` - starts API server and webpack dev UI server. API server uses current `kubectl` context to access workflow CRDs.
4. Build: `yarn build` - builds static resources into `./dist` directory.
5. Release: `IMAGE_NAMESPACE=argoproj IMAGE_TAG=latest DOCKER_PUSH=true yarn docker` - builds docker image and optionally push to docker registry.
