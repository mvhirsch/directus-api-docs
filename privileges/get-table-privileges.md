# Get Table Privileges

> **Note:** Table names are case-sensitive

<span class="request">`GET` **/api/1/privileges/_group-id_/_table-name_**</span>

<span class="description">Get the table privileges for a specific user group</span>

### Example Request

```bash
$ curl https://instance--key.directus.io/api/1.1/privileges/1/projects \
  -u [user-token]:
```

## Response

Table privilege for the specified table and user-group.

<span class="attributes">Attribute</span> | Description
-------|------------
**meta** _Meta Object_ | The Directus system metadata object that provides useful information not contained within the dataset itself <a class="object">**Meta Object**: View Nested Attributes</a>
<span class="custom">**data**</span> _Privilege Object_ | <span class="custom">This data and its architecture is based on Directus Privileges's schema</span>

### Example Response

```json
{
  "meta": {
    "type": "item",
    "table": "directus_privileges"
  },
  "data": {
    "id": 1,
    "table_name": "projects",
    "group_id": 1,
    "read_field_blacklist": null,
    "write_field_blacklist": null,
    "nav_listed": 1,
    "status_id": 0,
    "allow_view": 2,
    "allow_add": 1,
    "allow_edit": 2,
    "allow_delete": 2,
    "allow_alter": 1
  }
}
```