# luststream_config

## Description
A comprehensive Flutter configuration package for managing LustStream application settings and parameters.

## Features
- Dynamic configuration management
- Environment-specific settings
- Secure storage of sensitive data
- Easy integration with Flutter apps
- Runtime configuration updates
- Type-safe configuration access

## Installation
Add this to your `pubspec.yaml`:
```yaml
dependencies:
    luststream_config: ^1.0.0
```

## Usage
```dart
import 'package:luststream_config/luststream_config.dart';

// Initialize configuration
await LustStreamConfig.initialize();

// Access configuration values
final apiKey = LustStreamConfig.get('api_key');
```

## Configuration Structure
- `config/`
    - `development.json`
    - `production.json`
    - `staging.json`

## API Reference

### Core Methods
- `initialize()`: Bootstrap configuration
- `get(String key)`: Retrieve configuration value
- `set(String key, dynamic value)`: Update configuration
- `reload()`: Refresh configuration from source

### Configuration Types
- Network settings
- Cache parameters
- API endpoints
- Feature flags
- Security settings

## Environment Setup
```dart
const environment = String.fromEnvironment('LUSTSTREAM_ENV', defaultValue: 'development');
```

## Error Handling
```dart
try {
    await LustStreamConfig.initialize();
} on ConfigurationException catch (e) {
    print('Configuration error: ${e.message}');
}
```

## Contributing
Please read CONTRIBUTING.md for details on code of conduct and submission process.

## License
This project is licensed under the MIT License - see LICENSE file for details.

## Author
LustStream Team

## Support
For support queries, create an issue on the GitHub repository.