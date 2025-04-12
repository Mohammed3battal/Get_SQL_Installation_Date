## Script: Get `sa` Login Creation Date

**Description**:
This script returns the creation date of the built-in `sa` login in SQL Server. The `sa` login is identified by its unique, fixed SID `0x010100000000000512000000`.

**Use Case**:
- Estimate SQL Server **installation or provisioning date**
- Audit `sa` account existence or modification
- Confirm whether `sa` has been recreated after being dropped

**Requirements**:
- SQL Server 2005 or later
- Access to `sys.server_principals` (typically requires `VIEW ANY DEFINITION` or `sysadmin`)

**Notes**:
- If the `sa` account has been dropped and recreated manually, the `create_date` will reflect that later timestamp.
- If no results are returned, the `sa` login may not exist on the instance.
