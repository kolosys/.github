# Welcome to Kolosys 🚀

**Building developer-friendly libraries and tools for modern Go applications**

## 🎯 Our Mission

Kolosys creates high-quality, production-ready Go libraries that solve real-world challenges in concurrency, scheduling, and time-based operations. We focus on:

- **Developer Experience** - Simple, intuitive APIs that just work
- **Production Ready** - Battle-tested code with comprehensive testing
- **Performance First** - Optimized implementations with minimal overhead
- **Context-Aware** - Proper cancellation and timeout handling throughout

## 🛠️ Featured Projects

### [TimeCapsule](https://github.com/kolosys/timecapsule)

A lightweight Go library for time-locked value storage - like a "sealed envelope" for your data.

```go
// Store a value that unlocks in 24 hours
capsule.Store(ctx, "promo-code", "HOLIDAY50", time.Now().Add(24*time.Hour))

// Try to open (will fail if still locked)
value, err := capsule.Open(ctx, "promo-code")
```

**Perfect for:**

- Delayed actions and scheduled tasks
- Future-effective configuration changes
- Time-locked features and promotional codes
- Secure value storage with temporal constraints

📖 **[Documentation](https://docs.kolosys.com/timecapsule)** | 🐛 **[Issues](https://github.com/kolosys/timecapsule/issues)**

### [Ion](https://github.com/kolosys/ion)

Robust concurrency and scheduling primitives for Go applications.

```go
// Worker pool with graceful shutdown
pool := workerpool.New(4, 20, workerpool.WithName("api-pool"))

// Fair semaphore for resource limiting
sem := semaphore.NewWeighted(3, semaphore.WithFairness(semaphore.FIFO))

// Token bucket rate limiting
limiter := ratelimit.NewTokenBucket(ratelimit.PerSecond(100), 20)
```

**Includes:**

- **Worker Pools** - Bounded pools with context-aware submission
- **Semaphores** - Weighted fair semaphores with configurable fairness
- **Rate Limiters** - Token bucket and leaky bucket implementations
- **Future**: Circuit breakers, pipelines, and task scheduling

📖 **[Documentation](https://docs.kolosys.com/ion)** | 🐛 **[Issues](https://github.com/kolosys/ion/issues)**

## 🌟 Design Principles

All Kolosys projects follow these core principles:

- **Context-First**: Proper cancellation and timeout handling
- **No Panics**: Libraries return errors instead of panicking
- **Minimal Dependencies**: Core functionality with zero external deps
- **Thread-Safe**: All public APIs safe for concurrent use
- **Pluggable Observability**: Optional logging, metrics, and tracing

## 📚 Documentation & Resources

### 🎯 Centralized Documentation

All our projects now feature comprehensive documentation hosted on **GitBook**:

- **📖 [TimeCapsule Docs](https://docs.kolosys.com/timecapsule)** - Complete API reference, examples, and guides
- **📖 [Ion Docs](https://docs.kolosys.com/ion)** - Detailed documentation for all concurrency primitives
- **🏠 [Main Site](https://docs.kolosys.com)** - Organization overview and project navigation

### 🔧 Development Resources

- **API Reference**: Auto-generated from Go code with examples
- **Getting Started**: Step-by-step guides for each library
- **Examples**: Real-world usage patterns and best practices
- **Benchmarks**: Performance comparisons and optimization targets

## 🤝 Contributing

We welcome contributions from the community! Here's how to get involved:

1. **📖 Read the docs** - Start with our comprehensive documentation
2. **🐛 Find issues** - Look for "good first issue" labels in repositories
3. **📋 Follow guidelines** - Each repo has detailed CONTRIBUTING.md files
4. **💬 Join discussions** - Use GitHub Discussions for questions and ideas

### Quick Start for Contributors

```bash
# Clone any project
git clone https://github.com/kolosys/<project-name>
cd <project-name>

# Run tests
go test -v ./...

# Check formatting and linting
go fmt ./...
go vet ./...

# Generate documentation (if applicable)
go run .actions/shared/scripts/generate-docs.go
```

## 🚀 CI/CD & Automation

Our projects feature modern CI/CD pipelines with:

- **🔄 Automated Testing** - Comprehensive test suites on every PR
- **📚 Auto-Generated Docs** - Documentation updated automatically from code
- **🏷️ Semantic Releases** - Automated versioning and changelog generation
- **🔍 Code Quality** - Linting, formatting, and security scanning
- **📦 Multi-Platform Builds** - Support for Linux, macOS, and Windows

## 🔗 Quick Links

- 🏠 **[Main Site](https://docs.kolosys.com)** - Organization overview
- 📖 **[Documentation](https://docs.kolosys.com)** - All project docs
- 🐛 **Issues**: Found a bug? Open an issue in the relevant repository
- 💡 **Feature Requests**: Use GitHub Discussions to propose new features
- 🏷️ **Releases**: Check release notes for latest updates and breaking changes

---

_Building reliable software, one library at a time._ ⚡
