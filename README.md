# Capture Record(s) in current Update Set

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![license-shield]][license-url]

My own version of the well-known "Cature record in update set" feature.

Features included:

- Toggle on/off property allowing to disable the feature in the production environment.
- Commit/discard changes made in the record before being captured in the update set.
- Capture multiple records from the list view at a time.
- Include/exclude tables extending sys_metadata. Most of them are yet captured by default.

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


[contributors-shield]: https://img.shields.io/github/contributors/AlexAlvarez092/SN-Capture-Records-Update-Set.svg?style=for-the-badge
[contributors-url]: https://github.com/AlexAlvarez092/SN-Capture-Records-Update-Set/graphs/contributors

[forks-shield]: https://img.shields.io/github/forks/AlexAlvarez092/SN-Capture-Records-Update-Set.svg?style=for-the-badge
[forks-url]: https://github.com/AlexAlvarez092/SN-Capture-Records-Update-Set/network/members

[stars-shield]: https://img.shields.io/github/stars/AlexAlvarez092/SN-Capture-Records-Update-Set.svg?style=for-the-badge
[stars-url]: https://github.com/gAlexAlvarez092/SN-Capture-Records-Update-Set/stargazers

[issues-shield]: https://img.shields.io/github/issues/AlexAlvarez092/SN-Capture-Records-Update-Set.svg?style=for-the-badge
[issues-url]: https://github.com/AlexAlvarez092/SN-Capture-Records-Update-Set/issues

[license-shield]: https://img.shields.io/github/license/AlexAlvarez092/SN-Capture-Records-Update-Set.svg?style=for-the-badge
[license-url]: https://github.com/AlexAlvarez092/SN-Capture-Records-Update-Set/blob/master/LICENSE.txt