# AOSP Snapshot Management Library

This project is part of the Android Open Source Project (AOSP) and provides tools and libraries for managing dynamic partitions, snapshots, and related functionality in Android's update system.

## Project Structure

The repository contains the following key components:

- **Dynamic Partition Snapshots**: Implements functionality for managing snapshots of dynamic partitions during OTA updates.
- **Snapshot Metadata**: Handles metadata updates and validation for snapshots.
- **Utility Functions**: Provides helper functions for common operations.

### Key Files

- **Core Implementation**
  - `snapshot.cpp`: Core logic for snapshot management.
  - `partition_cow_creator.cpp`: Handles creation of Copy-On-Write (COW) partitions.
  - `scratch_super.cpp`: Manages temporary super partitions during updates.

- **Headers**
  - `snapshot.h`, `partition_cow_creator.h`, `scratch_super.h`: Corresponding headers for core implementation files.

- **Tests**
  - `partition_cow_creator_test.cpp`: Unit tests for COW partition creation.
  - `snapshot_metadata_updater_test.cpp`: Tests for snapshot metadata updates.
  - `vts_ota_config_test.cpp`: Validation tests for OTA configurations.

- **Utilities**
  - `utility.cpp`: General-purpose utility functions.
  - `test_helpers.cpp`: Helper functions for unit tests.

### Build Configuration

- **Android.bp**: Build configuration file for the AOSP build system.

## How to Build

This project is integrated into the AOSP build system. To build it:

1. Ensure you have a working AOSP build environment set up.
2. Run the following command from the root of the AOSP source tree:

   ```sh
   m libsnapshot
