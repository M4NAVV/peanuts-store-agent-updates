# Store agent updates

Signed update files for an internal store reporting agent. Nothing here is useful outside it.

- `manifest.json` lists the current version for each channel, with the download link and SHA-256 of each file.
- `manifest.json.sig` is an Ed25519 signature over `manifest.json`. The agent installs a file only when this
  signature verifies against the public key built into it AND the download's SHA-256 matches. Changing these files
  without the private key (which is not on GitHub) does nothing.
- The program files are attached to the Releases.
