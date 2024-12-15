# maintain own custom VCPKG deps

## packages

- assimp master
  + 2024-12-15

# registry

https://github.com/kikonen/vcpkg-registry


# setup

```bash
git rev-parse HEAD:ports/assimp
```

# Instructions

- https://devblogs.microsoft.com/cppblog/registries-bring-your-own-libraries-to-vcpkg/
- https://learn.microsoft.com/en-us/vcpkg/maintainers/functions/vcpkg_from_github
- https://stackoverflow.com/questions/987372/what-is-the-format-of-a-patch-file
- https://learn.microsoft.com/en-us/vcpkg/reference/vcpkg-configuration-json
- https://github.com/Microsoft/vcpkg-docs/blob/main/vcpkg/consume/git-registries.md
- https://devblogs.microsoft.com/cppblog/vcpkg-updates-static-linking-is-now-available/
- https://learn.microsoft.com/en-us/vcpkg/reference/vcpkg-json#platform-expression

# Test

```powershell
# DLL
vcpkg install assimp --overlay-ports=vcpkg-registry/ports/assimp

# STATIC
vcpkg install assimp:x64-windows-static --overlay-ports=vcpkg-registry/ports/assimp
```
