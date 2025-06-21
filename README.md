# GitHub Actions Mirror

A private mirror repository for commonly used GitHub Actions, maintained for use in private projects with consistent versioning, security review and the ability to apply custom patches when necessary.

> **Note**: Original action names have been preserved.

## Included Actions

| Action | Original Repository | Current Version | Status | Modified |
|--------|-------------------|-----------------|---------|-----------|
| `action-gh-release` | [Link](https://github.com/softprops/action-gh-release) | v1.0.0 | ✅ | No |
| `action-zip` | [Link](https://github.com/vimtor/action-zip) | v1.0.0 | ✅ | No |
| `actions-status-discord` | [Link](https://github.com/sarisia/actions-status-discord) | v1.0.0 | ✅ | No |
| `cache` | [Link](https://github.com/imnotverygood/cache) | v4.1 | ✅ | No |
| `unity-builder` | [Link](https://github.com/game-ci/unity-builder) | v1.0.0 | ✅ | No |

### Status
> ✅ Up to date | ⚠️ Update available

## Usage

Replace the original action references in your workflows with the mirrored versions:

### Example: GitHub Release Action

```yaml
# Instead of: softprops/action-gh-release@v1
# Use:
- uses: imnotverygood/actions-mirror/action-gh-release@v1.0.0
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  with:
    tag_name: ${version}
    name: ${version}
    body: ${changelog}
    prerelease: false
    make_latest: true
    files: |
      dist/*.zip
      dist/*.tar.gz
```

## 📄 License

Individual actions retain their original licenses. See each action directory for specific license information.

---


*Last checked: 2025-06-21 11:38 UTC*
