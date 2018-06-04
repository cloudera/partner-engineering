# Cloudera Enterprise Storage Device Acceptance Criteria Guide - Toolkit
## storage-validation-toolkit

This repository hosts the scripts and samples needed to validate non-direct attached storage options for use with Cloudera Enterprise.  The guide, prerequisites, and instructions for use of these scripts can be found at: http://tiny.cloudera.com/storage-guide

---
### Included files
#### Scripts:
* test-config - Script snippet to defines variables for cluster description and test configuration
* generate-test-configs - Consumes test-config and generates nodegroup specific workload test configuration files
* on-each-do - Utility script to run a command on all hosts listed in a configuration file
* pre-fio-dir-all - Script to read test-config and install fio on all hosts, and make an fio directory in each data location to house test files for fio
#### Directories:
* fio-test-templates/ - Template files used to generate fio test config files using different combinations of work and storage config
* test-files/ - Generated cluster-specific fio and utility configuration files.  **Any files in this directory may be deleted by scripts in this toolset.**
* results/ - Data from workload test runs will be placed here.  **Any files in this directory may be deleted by scripts in this toolset.**
#### Cloudera Manager Samples:
* StorageMonitoringOverview.json - Example Cloudera Manager Dashboard to chart cluster-wide storage latency measurement to determine performance of storage (Requires regex match for naming conventions to differentiate worker and master nodes)
* StorageMonitoringDetails.json - Example Cloudera Manager Dashboard to chart end-to-end storage lacency per disk for every host
* StorageLatencyTriggers.json - Example host trigger to alert concerning health when a node's reported storage latency is too high (Requires regex match for naming conventions to differentiate worker and master nodes)

---
Copyright (C) 2018 Cloudera, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.