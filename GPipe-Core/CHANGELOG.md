# Changelog for GPipe-Core Fork

## v2.4.1-fork1 (2025-01-27) - Community Fork Release

### 🎉 **Fork Initialization**
This is the first release of the community-maintained GPipe-Core fork, updated for LTS-21+ compatibility.

### ✅ **Dependency Updates** 
- **BREAKING**: Updated `base` bounds from `>= 4.9 && < 5` to `>= 4.16 && < 5`
  - Now requires GHC 9.2+ (LTS-21+)
- **BREAKING**: Updated `transformers` bounds from `>= 0.5.2 && < 0.6` to `>= 0.5 && < 0.7`
- Updated `containers` bounds from `>= 0.5 && < 0.7` to `>= 0.5 && < 0.8`

### 🔧 **Repository Updates**
- Updated homepage URL to point to fork repository
- Updated maintainer information for community fork
- Added comprehensive GitHub Actions CI pipeline
- Updated documentation to reflect fork status

### 📦 **Build System**
- Updated stack.yaml to use LTS-21.25
- Verified compatibility with current Stackage LTS
- Added CI matrix testing across:
  - Platforms: Ubuntu, Windows, macOS  
  - GHC versions: 9.2, 9.4, 9.6
  - Build tools: Cabal and Stack

### 🎯 **Migration Path**
- **From upstream GPipe 2.2.5**: Update dependency bounds in your project
- **API Compatibility**: No breaking API changes - drop-in replacement
- **Version Strategy**: Using `upstream.version-forkN` scheme

### 📖 **Documentation**
- Updated README with fork rationale and setup instructions
- Added maintenance guidelines and support information  
- Preserved original GPipe tutorials and documentation links

---

# Original GPipe-Core Changelog

### 2.2.5

- Support for GHC 8.8.3

### 2.2.4

- Support for GHC 8.6.5 (#63)

### 2.2.3

- Removing an unnecessary optimization that was broken since 2.2

### 2.2.2

- Support for GHC 8.2.1 (#52)
- Fixing errors with hidden contexts
- Fixing GLSL link error on subtracting a negative constant (#55)
- Fixing GLSL ambiguous overload with "clamp" (#51)
- Adding atan2' (#44)

### 2.2.1

- Render monad would crash if using deleted windows, when that should be a no-op. (#41).
- Manually deleting last visible window causes objects to be deleted (#42).

### 2.2

- Windows are now explicit objects dynamically created and deleted with newWindow and deleteWindow, and are sent as parameter to drawWindowColor et al. (#18)
- Each window created can now take their own window manager specific parameters (#19)
- Update to GHC 8.0.2 and gl-0.8.0 (#38)

### 2.1.8

- Update dependencies to make it build with stack resolver nightly-2016-09-24

### 2.1.7

- Runtime optimizations (Use BaseVertex for glDraw* instead of offsetting each attribute)

### 2.1.6

- Adding support for normal Floats, Int32s and Word32s in PrimitiveStreams
- Runtime optimizations

### 2.1.5

- Fixed bug in clear where masks weren't set
- Added up to 7-tuple instances

### 2.1.4

- Fixed bug in dropVertices and dropIndices (#16)
- Added withPointSize (#15)

### 2.1.3

- Fixed bug in clearImage

### 2.1.2

- Fixed bug when nesting while, ifThen, ifThenElse or ifThenElse'.

### 2.1.1

- Made ifB use ifThenElse' instead to avoid unwanted strictness
- Fixed bug where ShaderBaseType for () wasn't lazy enough, causing error in ifThenElse'
- Added missing () instances

### 2.1

- Making dangling finalizers work with shared and unshared contexts (#10)
- Moved orphan instances to separate module (#11)
- Fixing a bug introduced in 2.0.2 when using multiple uniforms
- Fixing exception when using conditionals in the shader (#12)

### 2.0.2

- Linear bumped to 1.20
- Running contextSwap and contextFrameBufferSize on right thread (#7)
- render now throws if rendering to an image from a texture thats used for sampling (#8)
- Added GPipe class instances for all linear types (#9)

### 2.0.1

- Fixed runtime error in simple fragment program when not all uniforms where used (#5)

### 2.0

- Initial release of GPipe 2
