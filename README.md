# ansible_cephadm

This role installs [cephadm](https://docs.ceph.com/en/quincy/cephadm/) and Docker on Debian.
That is, the packages `cephadm`, `docker-ce` and `docker-ce-cli` will be installed.

## Requirements

[Debian](https://www.debian.org/).
Maybe this role also works on other apt based systems.

## Role Variables

| Name                   | Required | Description                                                                                                                                          |
| :--------------------- | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| `cephadm_release_name` | yes      | Release name for `cephadm add-repo --release`, e.g. `quincy`. For possible release names, see: <https://docs.ceph.com/en/quincy/releases/index.html> |

## Example Playbook

The following example playbook assumes that you cloned this role to `roles/cephadm`
(i.e. the name of the role is `cephadm` instead of `ansible_cephadm`).

```yml
- hosts: kube01
  roles:
    - role: cephadm
      cephadm_release_name: quincy
```

## License

This work is licensed under the [MIT License](./LICENSE).

## Author Information

- [Sebastian Hasler (haslersn)](https://github.com/haslersn) _sebastian.hasler at stuvus.uni-stuttgart.de_