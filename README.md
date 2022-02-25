# Capture Record(s) in current Update Set

My own version of the well-known "Cature record in update set" feature.

Extra features included:

- Toggle on/off property allowing to disable the feature in the production environment.
- Commit/discard changes made in the record before being captured in the update set.
- Capture multiple records from the list view at a time.
- Include/exclude tables extending sys_metadata. Most of them are yet captured by default.

## Installation

- Update set capture_record_in_update_set.xml


## Technical solution

### Script includes

- CaptureRecordInUpdateSet: Backend utilities used by the feature.
- CaptureRecordInUpdateSetAjax: Bridge Client-Server. Necessary to capture multiple records at a time.

### System properties

| Property name | Description |
| ------------- | ----------- |
| _x.capture_file_uset.active | Toggle on/off |
| _x.capture_file_uset.exclude_app_file | Include/exclude tables extending sys_metadata |
| _x.capture_file_uset.commit_before | Commit/discard changes before capturing |

### UI Messages

- _x.capture_file_uset.ok: Displayed as an info message once the record has been captured.

### UI Actions

