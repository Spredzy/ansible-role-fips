# ansible-role-fips

An Ansible role to turn a machine into FIPS-enabled mode.

## Usage

```yaml
---
- hosts: all
  roles:
    - fips
```

**Warning**: The hosts will be rebooted during this process.

After they come back up one can check the fips status by running:

```bash
$ sysctl crypto.fips_enabled
crypto.fips_enabled = 1
```

On EL8 nodes, one should ensure the following file exists:

```bash
$ cat /etc/system-fips
# FIPS module installation complete
```

## License

Apache 2.0

## Author

Yanis Guenane  <yguenane@redhat.com>
