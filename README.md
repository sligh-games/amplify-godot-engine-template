# AWS Amplify for Godot Engine - Template

[![GitHub release](https://img.shields.io/github/release/sligh-games/amplify-godot-engine-template)](https://github.com/sligh-games/amplify-godot-engine-template/releases)
[![Open Bugs](https://img.shields.io/github/issues/sligh-games/amplify-godot-engine-template/bug?color=d73a4a&label=bugs)](https://github.com/sligh-games/amplify-godot-engine-template/issues?q=is%3Aissue+is%3Aopen+label%3Abug)
[![Feature Requests](https://img.shields.io/github/issues/sligh-games/amplify-godot-engine-template/feature-request?color=ff9001&label=feature%20requests)](https://github.com/sligh-games/amplify-godot-engine-template/issues?q=is%3Aissue+label%3Afeature-request+is%3Aopen)
[![Closed Issues](https://img.shields.io/github/issues-closed/sligh-games/amplify-godot-engine-template?color=%2325CC00&label=issues%20closed)](https://github.com/sligh-games/amplify-godot-engine-template/issues?q=is%3Aissue+is%3Aclosed+)

## Introduction

This project contains an AWS Amplify project template to create, build, export and deploy Godot Engine projects on cloud infrastructure. It streamlines the process of taking your Godot game from development to production with minimal configuration.

### What is AWS Amplify?

AWS Amplify is a set of tools and services that enables developers to build full-stack applications with features like authentication, storage, and serverless functions. This template leverages Amplify to provide:

- Automated CI/CD pipeline for your Godot projects
- Simplified cloud deployment with minimal AWS knowledge required
- Scalable hosting for web-based Godot games
- Easy integration with other AWS services when needed

### What is Godot Engine?

[Godot Engine](https://godotengine.org/) is a free and open-source game engine that provides a comprehensive set of tools for game development across multiple platforms. This template is designed to work with Godot 4.x projects.

### Sample Game

This template includes a sample game named [Squash The Creeps](https://github.com/godotengine/godot-demo-projects/tree/master/3d/squash_the_creeps) from the [Godot Demo Projects](https://github.com/godotengine/godot-demo-projects). You can learn how to build this game from scratch in the [Godot Documentation](https://docs.godotengine.org) in the [Your first 3D game](https://docs.godotengine.org/en/stable/getting_started/first_3d_game/index.html) section.

## Quickstart

If you need step by step tutorials you can use our [quicktstarts](https://github.com/sligh-games/amplify-godot-engine/wiki/Create-a-New-Game) or explore [labs](https://github.com/sligh-games/amplify-godot-engine/wiki) on the wiki.

### Prerequisites

Before you begin, make sure you have:

- [Node.js](https://nodejs.org/) (v16 or later)
- [AWS CLI](https://aws.amazon.com/cli/) installed and configured
- [Godot Engine](https://godotengine.org/download) (v4.x recommended)
- An AWS account with appropriate permissions

### Project Structure

```
amplify-godot-engine-template/
├── amplify/               # AWS Amplify configuration files
│   ├── auth/              # Authentication configuration
│   ├── data/              # Data models and API configuration
│   └── backend.ts         # Main backend definition
├── game/                  # Godot game project files
│   ├── art/               # Game assets
│   ├── fonts/             # Game fonts
│   └── ...                # Other game files
├── amplify.yml            # Amplify build configuration
├── customHttp.yml         # Custom HTTP headers for deployment
└── package.json           # Project dependencies
```

### Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/sligh-games/amplify-godot-engine-template.git
   cd amplify-godot-engine-template
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Initialize Amplify:
   ```bash
   npx amplify init
   ```

4. Deploy the backend:
   ```bash
   npx amplify push
   ```

5. Open the Godot project:
   ```bash
   godot game/project.godot
   ```

## How It Works

This template automates several key aspects of game development and deployment:

### Build and Deployment Pipeline

The `amplify.yml` file defines a CI/CD pipeline that:
1. Sets up the AWS Amplify backend resources
2. Builds your Godot game for web deployment
3. Deploys the game to AWS hosting infrastructure

### Authentication and Backend Services

The template includes configuration for:
- User authentication (optional)
- Data storage and API endpoints (optional)
- Serverless functions (optional)

You can enable these features by uncommenting and configuring the relevant sections in the Amplify backend files.

### Custom HTTP Headers

The `customHttp.yml` file configures security headers for your deployed game, including:
- Cross-Origin-Opener-Policy
- Cross-Origin-Embedder-Policy

These headers are essential for certain web features like SharedArrayBuffer that modern web games might require.

## Wiki

The [wiki](https://github.com/sligh-games/wiki) contains everything you want to know about getting started with Sligh Games Amplify with the Godot Engine.

## Discussions

If you have a question or you want to discuss with the Sligh Games community go to the main project [discussions](https://github.com/sligh-games/amplify-godot-engine/discussions) channels.

[![join amplify discord](https://img.shields.io/discord/308323056592486420?logo=discord&label=AWS%20Amplify)](https://discord.gg/jWVbPfC)
[![join godot engine discord](https://img.shields.io/discord/1235157165589794909?logo=discord&label=Godot%20Engine)](https://discord.gg/godotengine)

## Issues

If you have any issue with a custom build image [report a bug](https://github.com/sligh-games/amplify-godot-engine-template/issues/new?assignees=&labels=&projects=&template=bug_report.md&title=) and if you need a new image or something else [create a feature request](https://github.com/sligh-games/amplify-godot-engine-template/issues/new?assignees=&labels=&projects=&template=feature_request.md&title=).

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT License. See the [LICENSE](LICENSE.md) file.

## Third Party Licenses

See [THIRD_PARTY_LICENSES](THIRD_PARTY_LICENSES.md) for more information.
