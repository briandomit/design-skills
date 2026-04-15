# ORCA Table Formatting Reference

Read this file when the define skill needs to produce an ORCA table output (Layer 5: Object Model). This file contains the exact formatting rules, cardinality notation, common mistakes, and a full worked example. The methodology and principles for object identification live in the define skill itself — this file is purely about output formatting.

---

## Absolute Rules

### Rule 1: Objects Are Objects
- An object is a THING, not a perspective
- **WRONG:** "User Profile (Self)" vs "Other Users" — these are the SAME User object
- **WRONG:** "My Licenses" vs "Organization Licenses" — these are the SAME License object
- **RIGHT:** One "User" object, one "License" object — period

### Rule 2: Permissions Are Separate
- What different roles can SEE or DO is a **permissions matrix**, NOT part of the ORCA table
- The ORCA table defines the object itself
- Create a SEPARATE section for role-based permissions AFTER the ORCA table

### Rule 3: Use the Exact Table Format
- ONE table with ALL objects
- Columns: Object | Core Content | Metadata | Relationships | Actions
- Use `•` bullets (not `-`) with `<br>` between items
- Each object is ONE ROW in the table

### Rule 4: Include Cardinality
- Every relationship MUST include cardinality notation
- Format: `(many:1)`, `(1:many)`, `(many:many)`, `(1:1)`, `(many:0-1)`
- Example: `• Belongs to Organization (many:1)`

---

## Cardinality Reference

| Notation | Meaning | Example |
|----------|---------|---------|
| `(1:1)` | Exactly one to exactly one | User Has Account (1:1) |
| `(1:many)` | One to many | Organization Has Users (1:many) |
| `(many:1)` | Many to one | Users Belong to Organization (many:1) |
| `(many:many)` | Many to many | Users Member of Groups (many:many) |
| `(many:0-1)` | Many to zero or one | Licenses Assigned to User (many:0-1) |
| `(1:0-1)` | One to zero or one | Organization Has Geographic Access (1:0-1) |

---

## Common Mistakes to Avoid

| WRONG | RIGHT |
|-------|-------|
| Splitting objects by viewer role | One object definition, separate permissions matrix |
| Using `-` for bullets | Using `•` for bullets |
| Creating nested tables | One flat table with all objects |
| Omitting cardinality | Every relationship has (many:1), (1:many), etc. |
| Putting permissions in ORCA | Permissions are a SEPARATE section |
| Line breaks within cells | Use `<br>` tags only |
| Separate table per object | ALL objects in ONE table |

---

## Complete Worked Example

This is the EXACT format to follow. Match this structure precisely.

# External UMP: User Management Objects — ORCA Mapping

**Scope:** External UMP — User administration, roles, groups, and license assignment
**Status:** Discovery documentation
**Total Objects:** 5 (truncated for reference — real tables include all objects)

---

## User Management Objects

| Object | Core Content | Metadata | Relationships | Actions |
|--------|--------------|----------|---------------|---------|
| **User** | • First Name<br>• Last Name<br>• Email<br>• Job Title<br>• Phone Number | • User ID<br>• Status (Active/Inactive/Pending)<br>• Created Date<br>• Last Login Date<br>• Invitation Status | • Belongs to Organization (many:1)<br>• Has Organizational Role (many:1) [required, exactly 1]<br>• Has Product Roles (many:many) [0 or more]<br>• Member of Groups (many:many)<br>• Assigned Licenses (many:many) | • Invite<br>• Edit<br>• Deactivate<br>• Reactivate<br>• Delete<br>• Assign Role<br>• Assign License<br>• Add to Group |
| **Organization** | • Organization Name<br>• Address<br>• Industry<br>• Company Size<br>• Primary Contact | • Organization ID<br>• Status (Active/Suspended/Trial)<br>• Created Date<br>• Account Type<br>• Renewal Date | • Has Users (1:many)<br>• Has Subscriptions (1:many)<br>• Has Groups (1:many)<br>• Has Roles (1:many) | • View Profile<br>• Edit Profile<br>• View Subscriptions<br>• View Users<br>• View Billing |
| **License** | • License Type<br>• Product Module Name<br>• Features Included<br>• Add-ons | • License ID<br>• Status (Active/Trial/Expired/Unassigned)<br>• Activation Date<br>• Expiration Date | • Belongs to Subscription (many:1)<br>• Assigned to User (many:0-1)<br>• Grants Permissions (1:many)<br>• Part of Product Module (many:1) | • Assign<br>• Unassign<br>• Reassign<br>• Activate<br>• Deactivate |
| **Role** | • Role Name<br>• Description<br>• Permission Set<br>• Scope (Organizational/Product-Specific) | • Role ID<br>• Role Type (Organizational/Product-Specific)<br>• Standard or Custom | • Belongs to Organization (many:1) [if custom]<br>• Assigned to Users (many:many)<br>• Includes Permissions (many:many) | • View<br>• Copy to Custom<br>• Assign to User<br>• Edit Permissions [custom only]<br>• Delete [custom only] |
| **Group** | • Group Name<br>• Description<br>• Purpose<br>• Members List | • Group ID<br>• Group Type (Department/Region/Team/Project)<br>• Status (Active/Archived)<br>• Member Count | • Belongs to Organization (many:1)<br>• Contains Users (many:many)<br>• Has License Pool (1:0-1)<br>• Has Default Roles (many:many) | • Create<br>• Add Member<br>• Remove Member<br>• Allocate License Pool<br>• Delete<br>• Archive |

---

## Object Relationship Diagram

```
ORGANIZATION (Hub)
├── Has Users (1:many) → USER
│   ├── Has Organizational Role (many:1) → ROLE
│   ├── Has Product Roles (many:many) → ROLE
│   ├── Member of Groups (many:many) → GROUP
│   └── Assigned Licenses (many:many) → LICENSE
│
├── Has Subscriptions (1:many) → SUBSCRIPTION
│   └── Contains Licenses (1:many) → LICENSE
│
├── Has Groups (1:many) → GROUP
│   ├── Contains Users (many:many) → USER
│   └── Has Default Roles (many:many) → ROLE
│
└── Has Roles (1:many) → ROLE
    └── Includes Permissions (many:many) → PERMISSION
```

---

## Key Business Rules

### User & Role Rules
- Every user MUST have exactly 1 organizational role (Owner/Admin/Team Member)
- Users can have 0 or more product-specific roles
- Users can belong to multiple groups simultaneously

### License Rules
- Licenses cannot exceed subscription seat count
- Geographic/Category access configured during license assignment

---

## Role-Based Permissions Matrix

**This section is SEPARATE from the ORCA table. Permissions are NOT part of object definitions.**

| Object | Owner | Admin | Team Member |
|--------|-------|-------|-------------|
| **User** (self) | Full | Full | Full |
| **User** (others) | Full | Full | None |
| **Organization** | Full + Billing | Edit (no billing) | View only |
| **License** (pool) | Full + Cost | Manage (no cost) | None |
| **Group** | Full + Delegation | Manage | View own |

---

## END OF EXAMPLE

---

## Checklist Before Delivering

- [ ] All objects in ONE table
- [ ] Using `•` bullets with `<br>` tags
- [ ] Every relationship has cardinality notation
- [ ] Object Relationship Diagram included
- [ ] Key Business Rules section included
- [ ] Permissions matrix is SEPARATE (if included)
- [ ] Format matches the example above EXACTLY
