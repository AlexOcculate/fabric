# Technology Stack

This document provides a comprehensive overview of the technologies, frameworks, and tools used in the Fabric project.

## Core Programming Languages

### Go (1.25.1)
- **Purpose**: Primary backend language for the Fabric CLI and REST API server
- **Usage**: Core application logic, API server, CLI commands, pattern management
- **Key Features**: High-performance concurrent processing, cross-platform support

### TypeScript/JavaScript
- **Purpose**: Frontend web application development
- **Usage**: Web UI built with SvelteKit
- **Key Features**: Type-safe development, modern ES modules

### Python
- **Purpose**: Utility scripts and optional UI
- **Usage**: Pattern extraction scripts, Streamlit UI alternative
- **Key Features**: Data processing, scripting automation

### Shell Scripting
- **Purpose**: Installation and setup automation
- **Usage**: 
  - Bash scripts (`.sh`) for Unix-like systems
  - PowerShell scripts (`.ps1`) for Windows
  - Batch scripts (`.bat`) for Windows

## Backend Technologies

### Frameworks & Libraries

#### Go Ecosystem
- **Gin** (v1.11.0) - Web framework for REST API
- **Cobra** (v1.10.2) - CLI framework for command-line interface
- **go-flags** (v1.6.1) - Command-line flag parsing
- **Swaggo** - API documentation generation (Swagger/OpenAPI)

#### Database
- **SQLite3** (v1.14.32) - Embedded database for local storage
- **go-sqlite3** - Go SQLite driver

#### AI/ML Integrations
- **OpenAI SDK** (v1.12.0) - OpenAI API integration
- **Anthropic SDK** (v1.19.0) - Claude AI integration
- **Ollama SDK** (v0.15.1) - Local LLM integration
- **Google Generative AI** (v1.40.0) - Google Gemini integration
- **AWS Bedrock** - Amazon AI services
- **Azure SDK** - Microsoft Azure AI services
- **Perplexity API** (v2.14.0) - Perplexity AI integration
- **GitHub Models** - GitHub-hosted AI models

#### Utilities
- **go-git** (v5.16.4) - Git operations in Go
- **go-readability** - Content extraction
- **go-github** (v66.0.0) - GitHub API client
- **clipboard** (v0.1.4) - Cross-platform clipboard support
- **yaml.v3** - YAML parsing
- **oauth2** - OAuth2 authentication

## Frontend Technologies

### Core Framework
- **Svelte** (v4.2.20) - Reactive UI framework
- **SvelteKit** (v2.49.5) - Application framework for Svelte
- **Vite** (v5.4.21) - Build tool and development server

### UI Libraries & Components
- **Skeleton UI** (v2.11.0) - Svelte component library
- **Tailwind CSS** (v3.4.17) - Utility-first CSS framework
- **Tailwind Forms** (v0.5.10) - Form styling plugin
- **Tailwind Typography** (v0.5.16) - Typography plugin
- **Lucide Svelte** (v0.309.0) - Icon library

### Document Processing
- **pdf-to-markdown-core** - PDF conversion
- **pdfjs-dist** (v5.4.449) - PDF rendering
- **marked** (v15.0.12) - Markdown parsing
- **mdsvex** (v0.11.2) - Markdown in Svelte
- **highlight.js** (v11.11.1) - Syntax highlighting
- **shiki** (v1.29.2) - Code syntax highlighter

### Other Frontend Libraries
- **date-fns** (v4.1.0) - Date manipulation
- **nanoid** (v5.0.9) - Unique ID generation
- **yaml** (v2.8.0) - YAML parsing
- **clsx** (v2.1.1) - Conditional CSS classes
- **youtube-transcript** (v1.2.1) - YouTube transcript extraction

## Build Tools & Package Managers

### Go
- **Go Modules** - Dependency management
- **GoReleaser** - Release automation

### JavaScript/TypeScript
- **npm** - Package manager
- **pnpm** - Alternative package manager (faster, more efficient)
- **Vite** - Build tool
- **Rollup** - Module bundler
- **ESLint** (v9.27.0) - Code linting
- **Prettier** - Code formatting
- **svelte-check** - Svelte type checking

### Python
- **pip** - Package manager

### Nix
- **Nix Flakes** - Reproducible development environments
- **gomod2nix** - Go module to Nix converter
- **treefmt-nix** - Multi-formatter tool

## DevOps & Containerization

### Docker
- **Base Images**: 
  - `golang:1.25-alpine` - For building
  - `alpine:latest` - For runtime
- **Multi-stage builds** - Optimized container size

### Development Containers
- **VS Code Dev Containers** - Containerized development environment
- **Base Image**: `mcr.microsoft.com/devcontainers/universal:2`

## CI/CD

### GitHub Actions
- **Workflows**:
  - `ci.yml` - Continuous integration (Go tests, Nix formatting checks)
  - `release.yml` - Automated releases
  - `patterns.yaml` - Pattern validation
  - `update-version-and-create-tag.yml` - Version management

### Tools Used in CI
- **actions/checkout** (v6) - Repository checkout
- **actions/setup-go** (v6) - Go environment setup
- **DeterminateSystems/nix-installer-action** (v21) - Nix installation
- **Go tooling**: Testing, modernization checks

## Development Tools

### Version Control
- **Git** - Source control
- **GitHub** - Repository hosting, issue tracking, pull requests

### Code Quality
- **Go testing framework** - Unit testing
- **ESLint** - JavaScript/TypeScript linting
- **Prettier** - Code formatting
- **svelte-check** - Svelte type checking
- **CodeQL** - Security analysis (via GitHub)

### IDEs & Editors
- **VS Code** - Recommended editor with configuration files provided
- **GoLand/IntelliJ** - Alternative Go IDE support

## Infrastructure & Services

### External Services Integration
- **OpenAI** - GPT models
- **Anthropic** - Claude models
- **Google AI** - Gemini models
- **AWS Bedrock** - Amazon AI services
- **Azure OpenAI** - Microsoft AI services
- **Ollama** - Local LLM hosting
- **GitHub Models** - GitHub-hosted models
- **Microsoft 365 Copilot** - Enterprise AI integration
- **Digital Ocean GenAI** - Cloud AI services
- **Abacus AI** - RouteLLM APIs
- **Z AI** - AI services
- **Perplexity AI** - Search-based AI

### Media Processing
- **yt-dlp** - YouTube video downloading
- **YouTube API** - Video transcript extraction

## API & Documentation

### API Documentation
- **Swagger/OpenAPI** - REST API documentation
- **Swagger UI** - Interactive API documentation at `/swagger/index.html`

### Documentation Format
- **Markdown** - Primary documentation format
- **YAML** - Configuration files
- **JSON** - Data interchange and configuration

## Internationalization (i18n)

### Supported Languages
- **English** (en)
- **Spanish** (es)
- **German** (de)
- **Persian/Farsi** (fa)
- **French** (fr)
- **Italian** (it)
- **Japanese** (ja)
- **Portuguese** (pt, pt-BR, pt-PT)
- **Chinese** (zh)

### i18n Libraries
- **go-i18n** (v2.6.0) - Go internationalization

## Security

### Dependencies
- **crypto/tls** - TLS/SSL support
- **OAuth2** - Authentication
- **AWS Signature** - AWS request signing

### Security Scanning
- **GitHub Dependabot** - Dependency security alerts
- **GitHub Advanced Security** - Code scanning

## Additional Tools

### Shell Completions
- **Bash** - Shell completion support
- **Zsh** - Shell completion support
- **Fish** - Shell completion support
- **PowerShell** - Shell completion support

### Text Processing
- **go-shellquote** - Shell argument parsing
- **mimetype** - MIME type detection
- **dateparse** - Flexible date parsing

## Project Structure

The project follows a modular architecture:
- **cmd/** - CLI entry points
- **internal/** - Internal packages (server, CLI logic, plugins)
- **web/** - SvelteKit web application
- **data/** - Pattern storage
- **scripts/** - Utility scripts
- **docs/** - Documentation
- **completions/** - Shell completion scripts

## Environment & Configuration

### Configuration Files
- **go.mod/go.sum** - Go dependencies
- **package.json** - Node.js dependencies
- **requirements.txt** - Python dependencies
- **flake.nix/flake.lock** - Nix environment
- **.goreleaser.yaml** - Release configuration
- **devcontainer.json** - Development container configuration
- **.envrc** - direnv configuration

### Environment Variables
- **API Keys** - Various AI service credentials
- **Configuration paths** - `~/.config/fabric`
- **Custom settings** - User preferences and patterns

---

**Last Updated**: January 2026

**Note**: This technology stack is actively maintained and may evolve as the project grows. For the most current dependency versions, refer to `go.mod`, `package.json`, and other package manifest files in the repository.
