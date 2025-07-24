# ProGet Expand Archives

**Description:**
An Ansible role that downloads archives from ProGet repository and expands them into a specified directory.

## Requirements

- `community.windows`
- `chocolatey.chocolatey` 

## Role Variables

```yaml
download_only: false  # Whether to only download files without extracting them
```

You can override these variables in your playbook when including this role.

## Dependencies

None, but you'll need Ansible version >=2.9 to run this role.

## Example Playbook Usage

Here's an example of how to use this role in a playbook:

```yaml
- hosts: all
  roles:
    - name: ccdc.expand_proget_archives
      vars:
        archive_definitions:
          - artefact_path: "my-repo/path/to/folder"
            filename: "my-archive.zip"
            base_destination_directory: "/opt/mydata"
```
## License

MIT / BSD
