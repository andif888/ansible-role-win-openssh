# ansible-role-win-openssh

Role to install OpenSSH on Windows.

## Table of content

- [Default Variables](#default-variables)
  - [win_openssh_download_url](#win_openssh_download_url)
  - [win_openssh_extract_dir](#win_openssh_extract_dir)
  - [win_openssh_extract_dir_name](#win_openssh_extract_dir_name)
  - [win_openssh_filename_zip](#win_openssh_filename_zip)
  - [win_openssh_install_dir](#win_openssh_install_dir)
  - [win_openssh_server_administrators_authorized_keys](#win_openssh_server_administrators_authorized_keys)
  - [win_openssh_server_firewall_open](#win_openssh_server_firewall_open)
  - [win_openssh_server_set_administrators_authorized_keys](#win_openssh_server_set_administrators_authorized_keys)
  - [win_openssh_server_shell_powershell](#win_openssh_server_shell_powershell)
  - [win_openssh_server_shell_powershell_executable](#win_openssh_server_shell_powershell_executable)
  - [win_openssh_version](#win_openssh_version)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### win_openssh_download_url

#### Default value

```YAML
win_openssh_download_url: https://github.com/PowerShell/Win32-OpenSSH/releases/download/{{
  win_openssh_version }}/{{ win_openssh_filename_zip }}
```

### win_openssh_extract_dir

#### Default value

```YAML
win_openssh_extract_dir: C:\windows\temp\openssh
```

### win_openssh_extract_dir_name

#### Default value

```YAML
win_openssh_extract_dir_name: OpenSSH-Win64
```

### win_openssh_filename_zip

#### Default value

```YAML
win_openssh_filename_zip: '{{ win_openssh_extract_dir_name }}.zip'
```

### win_openssh_install_dir

#### Default value

```YAML
win_openssh_install_dir: C:\Program Files\OpenSSH
```

### win_openssh_server_administrators_authorized_keys

#### Default value

```YAML
win_openssh_server_administrators_authorized_keys: "{{ lookup('env', 'HOME') + '/.ssh/id_rsa.pub'\
  \ }}"
```

### win_openssh_server_firewall_open

#### Default value

```YAML
win_openssh_server_firewall_open: true
```

### win_openssh_server_set_administrators_authorized_keys

#### Default value

```YAML
win_openssh_server_set_administrators_authorized_keys: false
```

### win_openssh_server_shell_powershell

#### Default value

```YAML
win_openssh_server_shell_powershell: true
```

### win_openssh_server_shell_powershell_executable

#### Default value

```YAML
win_openssh_server_shell_powershell_executable: '{{ ansible_env.SystemRoot }}\System32\WindowsPowerShell\v1.0\powershell.exe'
```

### win_openssh_version

#### Default value

```YAML
win_openssh_version: v8.9.1.0p1-Beta
```



## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
