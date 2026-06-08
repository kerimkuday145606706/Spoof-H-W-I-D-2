# Spoofer HWID PC

[![Download](https://img.shields.io/badge/DOWNLOAD-Release-7C3AED?style=for-the-badge&logo=github)](../../releases/tag/Release)

## A Robust HWID Spoofer for PC Systems

Easily switch hardware identifiers for your PC system with our HWID spoofer. Perfect for testing, development, or production environments. Built with modern C++ for optimal performance and reliability.

### Features
- **Multiple HWID profiles**: Switch between different HWID configurations effortlessly.
- **Customizable identifiers**: Define your own HWID formats and values.
- **Quick setup**: Easy installation and configuration with minimal overhead.
- **Cross-platform compatibility**: Works seamlessly across Windows and Linux systems.
- **Lightweight**: Minimal resource usage ensures smooth operation.

### Why Use Spoofer HWID PC?
In modern computing, hardware identifiers play a crucial role in software licensing, system identification, and compatibility. Our HWID spoofer allows developers and testers to simulate different hardware setups without physical changes, making it ideal for:

- Software licensing and activation testing.
- System compatibility checks.
- Development of hardware-dependent applications.
- Quick setup in CI/CD pipelines.

### Quick Start
1. **Install**: Clone the repository and install dependencies.
2. **Configure**: Edit `config/hwid-profiles.json` to define your HWID profiles.
3. **Run**: Execute the spoofer with your preferred profile.

### Installation
#### From Source
```bash
$ git clone https://github.com/yourusername/spoofer-hwid-pc.git
$ cd spoofer-hwid-pc
$ make install
```

#### Binary Installation
Download the latest release from the [GitHub Releases](https://github.com/yourusername/spoofer-hwid-pc/releases) page and extract the binaries.

### Basic Usage
Run the spoofer with the default profile:
```bash
$ ./bin/spoofer-hwid-pc start
```

To switch profiles:
```bash
$ ./bin/spoofer-hwid-pc switch --profile=my-profile
```

### Configuration
Profiles are defined in `config/hwid-profiles.json`. Example configuration:
```json
{
 "profiles": [
 {
 "name": "default",
 "hwid": "ABC123",
      "manufacturer": "MyCompany",
 "model": "PC1000"
    },
 {
 "name": "test-profile",
      "hwid": "XYZ789",
 "manufacturer": "TestCorp",
 "model": "TestModel"
 }
 ]
}
```

### Example Workflow
1. Start the spoofer with the default profile:
 ```bash
 $ ./bin/spoofer-hwid-pc start
   ```
2. Switch to the test profile:
   ```bash
 $ ./bin/spoofer-hwid-pC switch --profile=test-profile
   ```
3. Verify the current HWID:
   ```bash
   $ ./bin/spoofer-hwid-pc status
   ```

### Project Structure
```
├── bin/
│   ├── spoofer-hwid-pc
├── config/
│ └── hwid-profiles.json
├── src/
│ ├── main.cpp
│ └── hwid_manager.hpp
└── tests/
 └── test_hwid_manager.cpp
```

### Architecture
The spoofer is built with a modular design:
- **Core module**: Manages HWID profiles and configuration.
- **Profile loader**: Loads and validates HWID profiles.
- **Spoofer engine**: Applies the selected HWID to the system.

### Development Guide
Contributors can set up the project with:
```bash
$ make dev-setup
```

### Testing
Run unit tests with:
```bash
$ make test
```

### Security Notes
The spoofer runs with minimal privileges. Ensure proper permissions are set in production environments.

### Performance
Lightweight with minimal CPU and memory usage, making it ideal for resource-constrained systems.

### Roadmap
- Version1.0: Basic spoofer functionality.
- Version 1.1: Support for additional HWID types.
- Version1.2: GUI interface.

### Contributing
Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

### FAQ
**Q:** How do I reset to the default profile?\n**A:** Run `./bin/spoofer-hwid-pc reset`.

### License
MIT License

See [LICENSE](LICENSE) for details.

[![Download](https://img.shields.io/badge/DOWNLOAD-Release-7C3AED?style=for-the-badge&logo=github)](../../releases/tag/Release)
