## New Features

- Provisioning should work better now, since there is a daemon
  process watching the box and "patching things up"

- Per-user setup is now handled on a per-user basis, via a
  one-time setup script embedded in their ~/.bashrc / ~/.zshrc
  profiles.  This should greatly speed up provisioning.

- Accounts that were built by previous jumpbox manifests, but are
  not currently in the manifest, will be disabled, and their home
  directories renamed.  This allows administrators to manage
  account lifecycles more easily.

- A new `jumpbox.delete` property allows accounts to be deleted
  from the jumpbox, but only those that had been provisioned by
  the manifest.

- You can now set the jumpbox login banner, via `jumpbox.banner`
  It's got a spiffy default too!

## Improvements

- Default `$PATH` now puts the jumpbox package bin directory
  first, so that release-provided software like `curl` and `vim`
  takes precedence over system versions.

##### spruce
Bumped spruce to v1.8.2

##### safe
Bumped safe to v0.0.26

##### cf
Bumped cf to v6.22.2