# openvino-repo-syncher

This repository serves as a centralized hub for managing various OpenVINO repositories and automating the merge process between branches or repositories using GitHub Actions.

## Purpose

The primary purpose of this repository is to streamline the management of OpenVINO-related repositories by automating the synchronization of changes and facilitating seamless collaboration among contributors.

## Actions 

The following actions are performed within this repository:

- Auto-Merge Workflow: Automates the process of merging changes between specified repositories and branches based on predefined configurations.

- Source Map (source_map.yaml) : The source map defines the relationships between source and destination repositories for automerging changes.

## Workflow Configuration

The workflow is triggered either manually or on a schedule. It automates the process of syncing changes between upstream and downstream repositories.

## Development
In this repository, we have defined an auto-merge workflow using GitHub Actions. Here's how it works:

- Auto-Merge Workflow: The automerge workflow is configured in automerge.yaml. This workflow is triggered either manually or on a schedule and automates the process of syncing changes between specified repositories and branches.
The workflow performs the following steps:

- Set up variables: Initialization of necessary variables for the workflow.
- Set up git config: Configuration of git settings for the workflow.
- Clone downstream repository: Cloning of the downstream repository where changes will be pushed.
- Fetch upstream repository: Fetching of changes from the upstream repository to incorporate into the downstream repository.
- Attempt rebase if behind: If the downstream repository is behind the upstream repository, an attempt is made to rebase the changes onto the       downstream branch.
- Push changes to downstream: Pushing the merged changes to the downstream repository.

This automated process ensures seamless integration of changes from the upstream repository into the downstream repository, facilitating efficient collaboration and code management.

- Source Map

The source map defines the relationships between source and destination repositories for automerging changes. It is configured in [`source_map.yml`](source_map.yml) and includes details such as the repository names, automerge settings, synchronization modes, source URLs, and branch information.

The source map enables the auto-merge workflow to synchronize changes between repositories according to the defined configurations, ensuring smooth and reliable management of code changes across different branches and repositories.