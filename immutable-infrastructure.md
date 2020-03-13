# Immutable Infrastructure

You don't change your infrastructure; you replace it. Because infrastructure is now code instead of hardware it is described in scripts and documents. When a change is necessary, the concept of Immutable Infrastructure dictates that you do not change any running code. Instead, you create a new, updated version and push that into production.

This avoids the all-too-common problem of an update skipping some parts of the system. It also provides a clearer path to rolling back if necessary.

Note: Some argue that rolling back should never happen; you create an even newer version and roll forward, even if that new version includes the older code and settings.
