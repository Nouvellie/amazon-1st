# ENCRYPT ROOT DEVICE VOLUMES AND SNAPSHOTS
## Encrypt

#### General tips:

- Snapshots of encrypted volumes are encrypted automatically.
- Volumes restored from encrypted snapshots are encrypted automatically.
- Yo can share snapshots, but only if they are unencrypted.
- These snapshots can be shared with other AWS accounts or made public.

#### Steps to encrypt the root device volume:

- Create a snapshot of the unencrypted root device volume.
- Create a copy of the snapshot and select the encrypt option.
- Create an AMI from the encrypted snapshot.
- Use that AMI to launch new encrypted instances.