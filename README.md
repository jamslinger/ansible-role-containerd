Ansible Role: Containerd
=========
This ansible role installs the containerd runtime.

Requirements
------------
None

Variables
------------
Processor architecture:
```
containerd_proc_arch: "arm64"
```

Docker repository url:
```
containerd_docker_repo_url: "https://download.docker.com/linux"
```

Docker release channel:
```
containerd_docker_apt_release_channel: "stable"
```

Docker apt repository:
```
containerd_docker_apt_repository: "deb [arch={{ containerd_proc_arch }}] {{ containerd_docker_repo_url }}/{{ ansible_distribution | lower }} {{ ansible_distribution_release }} {{ containerd_docker_apt_release_channel }}"
```

Containerd apt key:
```
containerd_docker_apt_gpg_key: "{{ containerd_docker_repo_url }}/{{ ansible_distribution | lower }}/gpg"
```

Example Playbook
------------
```
- hosts: all
  roles:
    - jamslinger.containerd
```

License
------------
MIT
