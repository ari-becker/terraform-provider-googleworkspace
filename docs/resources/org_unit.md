---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "googleworkspace_org_unit Resource - terraform-provider-googleworkspace"
subcategory: ""
description: |-
  OrgUnit resource manages Google Workspace OrgUnits.
---

# googleworkspace_org_unit (Resource)

OrgUnit resource manages Google Workspace OrgUnits.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String) The organizational unit's path name. For example, an organizational unit's name within the /corp/support/sales_support parent path is sales_support.

### Optional

- **block_inheritance** (Boolean) Determines if a sub-organizational unit can inherit the settings of the parent organization. False means a sub-organizational unit inherits the settings of the nearest parent organizational unit. For more information on inheritance and users in an organization structure, see the [administration help center](https://support.google.com/a/answer/4352075). Defaults to `false`.
- **description** (String) Description of the organizational unit.
- **parent_org_unit_id** (String) The unique ID of the parent organizational unit.
- **parent_org_unit_path** (String) The organizational unit's parent path. For example, /corp/sales is the parent path for /corp/sales/sales_support organizational unit.

### Read-Only

- **etag** (String) ETag of the resource.
- **id** (String) The ID of this resource.
- **org_unit_id** (String) The unique ID of the organizational unit.
- **org_unit_path** (String) The full path to the organizational unit. The orgUnitPath is a derived property. When listed, it is derived from parentOrgunitPath and organizational unit's name. For example, for an organizational unit named 'apps' under parent organization '/engineering', the orgUnitPath is '/engineering/apps'. In order to edit an orgUnitPath, either update the name of the organization or the parentOrgunitPath. A user's organizational unit determines which Google Workspace services the user has access to. If the user is moved to a new organization, the user's access changes. For more information about organization structures, see the [administration help center](https://support.google.com/a/answer/4352075). For more information about moving a user to a different organization, see [chromeosdevices.update a user](https://developers.google.com/admin-sdk/directory/v1/guides/manage-users#update_user).

