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

## 🌟 Design Principles

All Kolosys projects follow these core principles:

- **Context-First**: Proper cancellation and timeout handling
- **No Panics**: Libraries return errors instead of panicking
- **Minimal Dependencies**: Core functionality with zero external deps
- **Thread-Safe**: All public APIs safe for concurrent use
- **Pluggable Observability**: Optional logging, metrics, and tracing

## 🤝 Contributing

We welcome contributions from the community! Here's how to get involved:

1. **Check out our projects** - Browse our repositories and documentation
2. **Start with issues** - Look for "good first issue" labels
3. **Follow our guidelines** - Each repo has detailed CONTRIBUTING.md files
4. **Join discussions** - Use GitHub Discussions for questions and ideas

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
```

## 📚 Resources

- **Documentation**: Each project has comprehensive docs and examples
- **API Reference**: Browse code documentation in each repository
- **Examples**: Real-world usage examples in each repository
- **Benchmarks**: Performance comparisons and optimization targets

## 🔗 Links

- 🐛 **Issues**: Found a bug? Open an issue in the relevant repository
- 💡 **Feature Requests**: Use GitHub Discussions to propose new features
- 📖 **Documentation**: Visit individual project READMEs for detailed guides
- 🏷️ **Releases**: Check release notes for latest updates and breaking changes

---

_Building reliable software, one library at a time._ ⚡
