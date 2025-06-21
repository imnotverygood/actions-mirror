# GitHub Actions Mirror

A private mirror repository for commonly used GitHub Actions, maintained for use in private projects with consistent versioning, security review and the ability to apply custom patches when necessary.

> **Note**: Original action names have been preserved.

## Included Actions

| Action | Original Repository | Current Version | Status | Modified |
|--------|-------------------|-----------------|---------|-----------|
| `action-gh-release` | [softprops/action-gh-release](https://github.com/softprops/action-gh-release) | v2.3.2 | ✅ | No |
| `action-zip` | [vimtor/action-zip](https://github.com/vimtor/action-zip) | error |  ❌  | No |
| `actions-status-discord` | [sarisia/actions-status-discord](https://github.com/sarisia/actions-status-discord) | v1.15.3 | ✅ | No |
| `cache` | [imnotverygood/cache](https://github.com/imnotverygood/cache) | v4.1 |  ⚠️  | No |
| `unity-builder` | [game-ci/unity-builder](https://github.com/game-ci/unity-builder) | v4.5.0 | ✅ | No |

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







*Last checked: 2025-06-21 12:22 UTC*
