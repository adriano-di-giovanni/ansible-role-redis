# Ansible Role: Redis

Ansible role for Redis:

* performs an opinionated installation from source code
* tunes OS performance
* configures Redis using include files instead of modifying the `redis.conf`
shipped into the distribution

**IMPORTANT** RDB and AOF are disabled by default. Override configuration
directives using `redis_includes` variable in your tasks.

**IMPORTANT** Don't rename/disable `SHUTDOWN` command. It's used by the init script.

## Requirements

None.

## Role variables

<table>
  <thead>
    <tr>
      <th>variable</th>
      <th>required</th>
      <th>default</th>
      <th>choices</th>
      <th>comment</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>redis_version</td>
      <td>no</td>
      <td>stable</td>
      <td>&nbsp;</td>
      <td>Version of Redis to install</td>
    </tr>
    <tr>
      <td>redis_port</td>
      <td>no</td>
      <td>6379</td>
      <td>&nbsp;</td>
      <td>Redis will accept connections on the specified port</td>
    </tr>
    <tr>
      <td>redis_bind</td>
      <td>no</td>
      <td>127.0.0.1</td>
      <td>&nbsp;</td>
      <td>Redis will listen for connections from selected interfaces.</td>
    </tr>
    <tr>
      <td>redis_maxmemory_percentage</td>
      <td>no</td>
      <td>70</td>
      <td>no</td>
      <td>Redis will use at most this percentage of system memory</td>
    </tr>
    <tr>
      <td>redis_includes</td>
      <td>no</td>
      <td>[]</td>
      <td>no</td>
      <td>Include one or more config files here</td>
    </tr>
  </tbody>
</table>

## Dependencies

None.

## Example playbook

```YAML
- hosts: all
  become: true
  roles:
    - adriano-di-giovanni.redis
```

The `example-*/`` folders contain project files to provision VMs using Vagrant and VirtualBox.

## License

MIT

## Author information

Adriano Di Giovanni
