# Capture Record(s) in current Update Set

My own version of the well-known "Cature record in update set" feature.

Extra features included:

- Toggle on/off property allowing to disable the feature in the production environment.
- Commit/discard changes made in the record before being captured in the update set.
- Capture multiple records from the list view at a time.
- Include/exclude tables extending sys_metadata. Most of them are yet captured by default.

## Installation

- Update set `capture_record_in_update_set.xml`


## Technical solution

### Script includes

- `CaptureRecordUtils()`: Contains the logic of the application. Client callable script.

### System properties

| Property name | Description |
| ------------- | ----------- |
| `u_capture_record.active` | Toggle on/off |
| `u_capture_record.exclude_app_file` | Include/exclude tables extending sys_metadata |
| `u_capture_record.commit_before` | Commit/discard changes before capturing |

### UI Messages

- `u_capture_record.success`: Confirmation message displayed after capturing.

### UI Actions

**`u_capture_record_form`**

Form view action. Shown only to *admin* users and records NOT extending `sys_metadata` table. If the system property `u_capture_record.exclude_app_file` value is `true`, it is displayed also to records extending `sys_metadata` table.

**`u_capture_record_list`**
List view action. Shown only to *admin* users.
