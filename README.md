# AWS Amplify for Godot Engine - Template

[![GitHub release](https://img.shields.io/github/release/sligh-games/amplify-godot-engine-template)](https://github.com/sligh-games/amplify-godot-engine-template/releases)
[![Open Bugs](https://img.shields.io/github/issues/sligh-games/amplify-godot-engine-template/bug?color=d73a4a&label=bugs)](https://github.com/sligh-games/amplify-godot-engine-template/issues?q=is%3Aissue+is%3Aopen+label%3Abug)
[![Feature Requests](https://img.shields.io/github/issues/sligh-games/amplify-godot-engine-template/feature-request?color=ff9001&label=feature%20requests)](https://github.com/sligh-games/amplify-godot-engine-template/issues?q=is%3Aissue+label%3Afeature-request+is%3Aopen)
[![Closed Issues](https://img.shields.io/github/issues-closed/sligh-games/amplify-godot-engine-template?color=%2325CC00&label=issues%20closed)](https://github.com/sligh-games/amplify-godot-engine-template/issues?q=is%3Aissue+is%3Aclosed+)

A production-ready AWS Amplify project template for Godot Engine game development. This template streamlines the process of taking your Godot game from development to production with minimal configuration, providing a complete cloud infrastructure foundation optimized for game deployment.

### Key Features

- **Full-Stack Solution**: Pre-configured backend and frontend integration for Godot games
- **Authentication System**: Ready-to-use player authentication with customizable login methods
- **Data Modeling**: Flexible schema definitions with relationship support for game data
- **Cloud Deployment**: Automated build and hosting pipeline for web and mobile games
- **Optimized Delivery**: Custom HTTP headers for efficient game asset delivery
- **Developer Friendly**: TypeScript-first approach with Amplify Gen 2

## Getting Started

Jump right into your Godot CI/CD pipeline with our comprehensive resources:
- **Quick Setup**: Follow our [quickstart guides](https://docs.sligh.games/#!/en/amplify-godot/get-started) for step-by-step implementation
- **Advanced Usage**: Explore [interactive labs](https://docs.sligh.games/#!/en/amplify-godot) for deeper integration scenarios

## Project structure

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

### AWS Amplify template

The AWS Amplify portion of this template provides a robust backend infrastructure for your Godot game. This template is built on AWS Amplify Gen 2, which offers a TypeScript-first development experience with improved type safety and developer ergonomics.

For web application development, AWS Amplify also provides templates for popular frameworks:
- [React with Vite template](https://docs.amplify.aws/gen2/start/quickstart/vite/)
- [Next.js template](https://docs.amplify.aws/gen2/start/quickstart/nextjs/)

Learn more about AWS Amplify:
- [AWS Amplify Website](https://aws.amazon.com/amplify/)
- [Amplify Documentation](https://docs.amplify.aws/)
- [Amplify Gen 2 Documentation](https://docs.amplify.aws/gen2/)


### Godot Engine game

This template includes a sample game named [Squash The Creeps](https://github.com/godotengine/godot-demo-projects/tree/master/3d/squash_the_creeps) from the [Godot Demo Projects](https://github.com/godotengine/godot-demo-projects). You can learn how to build this game from scratch in the [Godot Documentation](https://docs.godotengine.org) in the [Your first 3D game](https://docs.godotengine.org/en/stable/getting_started/first_3d_game/index.html) section.

### HTTP custom headers

Custom HTTP headers are configured in the `customHttp.yml` file to optimize the delivery of your Godot game. These headers ensure:

- Proper MIME types for Godot-specific file formats
- Efficient caching strategies for game assets
- Security headers to protect your application
- CORS configuration for API communication
- Compression settings for faster loading times

You can customize these headers based on your specific game requirements and deployment environment.



## Discussions

Join our community to get help, share ideas, and collaborate:

[![join sligh games discord](https://img.shields.io/discord/1371568283307868190?logo=discord&label=Sligh%20Games)](https://discord.gg/qN2q77zNDa)
[![join aws amplify discord](https://img.shields.io/discord/308323056592486420?logo=discord&label=AWS%20Amplify)](https://discord.gg/amplify)
[![join godot engine discord](https://img.shields.io/discord/1235157165589794909?logo=discord&label=Godot%20Engine)](https://discord.gg/godotengine)

For technical questions and feature discussions, visit our [GitHub Discussions](https://github.com/orgs/sligh-games/discussions).
## Security

If you discover a potential security issue, please DO NOT create a public GitHub issue. Instead, send an email directly to [security@sligh.games](mailto:security@sligh.games). This helps us address security vulnerabilities promptly and responsibly.

## Issues

If you have any issue with a custom build image [report a bug](https://github.com/sligh-games/amplify-godot-engine-template/issues/new?assignees=&labels=&projects=&template=bug_report.md&title=) and if you need a new image or something else [create a feature request](https://github.com/sligh-games/amplify-godot-engine-template/issues/new?assignees=&labels=&projects=&template=feature_request.md&title=).

## Contributing

See [CONTRIBUTING](CONTRIBUTING.md) for more information.

## License

This library is licensed under the MIT License. See the [LICENSE](LICENSE.md) file.

## Third Party Licenses

See [THIRD_PARTY_LICENSES](THIRD_PARTY_LICENSES.md) for more information.
