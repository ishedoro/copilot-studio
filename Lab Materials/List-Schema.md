# EquipmentRequests list

The instructor (or, in your own tenant, you) creates this SharePoint list before Lab 5, on a training site such as `https://<tenant>.sharepoint.com/sites/ITServiceDesk`.

## Create the list

1. On the site, select **+ New** → **List** → **Blank list**.
2. Name: `EquipmentRequests`. Select **Create**.
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

Every learner needs **Contribute** (Edit) permission on the list, because the flow's SharePoint connection uses the learner's own account. For a large class, create one list per learner (for example `EquipmentRequests-07`) and tell learners which one to use.

This is a training design. A production design would also record the requester's identity from sign-in, check for duplicate requests and restrict who can read other people's requests.
