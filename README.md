# cargo-workspace-release-please

This is a demo to figure out what [release-please](https://github.com/googleapis/release-please) does with a cargo workspace. 
The plugin `cargo-workspace` seems will skip some file updates, so we need to manually update the version in the `Cargo.toml` file.

```javascript
# manifest.json
...
"plugins": ["cargo-workspace"],
...
```

If you add `"plugins": ["cargo-workspace"],` to the `config.json` , release-please will skip the `Cargo.lock`'s member updates and `manifest.json`'s version updates.

> if you config release-please `changelog-type` to `github` you need push a version tag because the `release-please` will use the tag to as release api's previous tag.