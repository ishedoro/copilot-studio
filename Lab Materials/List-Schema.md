# EquipmentRequests list

Each learner creates their own copy of this list in Lab 5, Part 0, on the training site `https://iisadmin3innovationinsoftwa.sharepoint.com/sites/cps1015-lab`. The list is named `EquipmentRequests-` followed by the learner's initials, for example `EquipmentRequests-ID`.

## Create the list

1. On the site, select **+ New** → **List** → **Blank list**.
2. Name: `EquipmentRequests-` followed by your initials. Select **Create**.
3. Add the columns below with **+ Add column**.

| Column | Type | Settings |
|---|---|---|
| Title | Single line of text | Exists already; required |
| EquipmentType | Choice | Choices: `Laptop`, `Monitor`, `Headset`; required |
| Office | Choice | Choices: `Vancouver`, `Toronto`; required |
| RequestReason | Multiple lines of text | Plain text; required |
| Status | Choice | Choices: `Submitted`, `Pending approval`, `Approved`, `Rejected`; default `Submitted` |

The built-in **ID** column is the request number returned to the agent. **Created** and **Created By** are added automatically.

## Permissions

Every learner needs to be a member of the site (Edit permission), so they can create their own list. The flow's SharePoint connection uses the learner's own account, so each learner writes only to the list they created.

This is a training design. A production design would also record the requester's identity from sign-in, check for duplicate requests and restrict who can read other people's requests.
