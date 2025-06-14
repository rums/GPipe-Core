# GPipe-Core Fork

[![CI](https://github.com/rums/GPipe-Core/workflows/GPipe%20Fork%20CI/badge.svg)](https://github.com/rums/GPipe-Core/actions)

This is a **community-maintained fork** of [GPipe-Core](https://github.com/tobbebex/GPipe-Core), updated for **LTS-21+ compatibility** and ongoing maintenance.

## Why This Fork?

The original GPipe-Core (2.2.5) has been dormant since 2020 and doesn't build on current LTS Haskell due to outdated dependency bounds. This fork provides:

- ✅ **LTS-21+ Compatibility** - Works with GHC 9.2+ and current Stackage LTS
- ✅ **Updated Dependencies** - Modern `base`, `transformers`, and other dependencies
- ✅ **CI Infrastructure** - Comprehensive testing across platforms and GHC versions
- ✅ **Ongoing Maintenance** - Active monitoring and updates

## Quick Start

### With Stack
```bash
# Add to your stack.yaml
extra-deps:
  - git: https://github.com/rums/GPipe-Core.git
    commit: HEAD  # Or specific commit/tag
    subdirs:
      - GPipe-Core
```

### With Cabal
```bash
# Add to your cabal.project
source-repository-package
  type: git
  location: https://github.com/rums/GPipe-Core.git
  subdir: GPipe-Core
```

## Version Strategy

This fork uses the versioning scheme: `upstream.version-forkN`

- **Current Version**: `2.4.1-fork1`
- **Upstream Base**: GPipe-Core 2.2.5
- **Fork Number**: 1 (first fork iteration)

## What's Different?

### Dependency Updates
- `base`: `>= 4.16 && < 5` (was `>= 4.9 && < 5`)
- `transformers`: `>= 0.5 && < 0.7` (was `>= 0.5.2 && < 0.6`)
- `containers`: `>= 0.5 && < 0.8` (was `>= 0.5 && < 0.7`)

### Repository Updates
- Homepage: Points to this fork repository
- Maintainer: Community Fork
- CI: Comprehensive GitHub Actions workflow
- Documentation: Updated for fork status

## Original GPipe Documentation

This fork maintains full API compatibility with the original GPipe. See the [original documentation](https://github.com/tobbebex/GPipe-Core#readme) for usage instructions.

### GPU programming in Haskell using GPipe

* [Part 1](http://tobbebex.blogspot.se/2015/09/gpu-programming-in-haskell-using-gpipe.html): Hello triangle!
* [Part 2](http://tobbebex.blogspot.se/2015/09/gpu-programming-in-haskell-using-gpipe_11.html): Buffers and textures
* [Part 3](http://tobbebex.blogspot.se/2015/10/gpu-programming-in-haskell-using-gpipe.html): Shaders and linear algebra
* [Part 4](http://tobbebex.blogspot.se/2015/10/gpu-programming-in-haskell-using-gpipe_11.html): Textures and samplers
* [Part 5](http://tobbebex.blogspot.se/2015/11/gpu-programming-in-haskell-using-gpipe.html): Framebuffers and render targets

## Maintenance & Support

This fork is maintained as part of the [haskemup](https://github.com/your-org/haskemup) project's graphics migration to GPipe. We welcome:

- 🐛 **Bug Reports** - Issues with the fork-specific changes
- 🔧 **Dependency Updates** - Keeping pace with new LTS releases
- 📝 **Documentation** - Improvements to fork-specific docs

### Not Maintained Here
- ❌ **New GPipe Features** - This fork focuses on maintenance, not feature development
- ❌ **Upstream Issues** - Report original GPipe issues to the [upstream repository](https://github.com/tobbebex/GPipe-Core/issues)

## License

MIT License - Same as original GPipe-Core

## Original Credits

**Original Author**: Tobias Bexelius  
**Original Repository**: https://github.com/tobbebex/GPipe-Core  
**Upstream Version**: 2.2.5 (2020-04-10)

This fork maintains the original licensing and attribution while providing the maintenance needed for modern Haskell development.
