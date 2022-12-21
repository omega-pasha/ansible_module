# Домашнее задание к занятию "08.04 Создание собственных modules"

## Подготовка 

```
> . venv/bin/activate && . hacking/env-setup

running egg_info
creating lib/ansible_core.egg-info
writing lib/ansible_core.egg-info/PKG-INFO
writing dependency_links to lib/ansible_core.egg-info/dependency_links.txt
writing entry points to lib/ansible_core.egg-info/entry_points.txt
writing requirements to lib/ansible_core.egg-info/requires.txt
writing top-level names to lib/ansible_core.egg-info/top_level.txt
writing manifest file 'lib/ansible_core.egg-info/SOURCES.txt'
reading manifest file 'lib/ansible_core.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
warning: no files found matching 'SYMLINK_CACHE.json'
warning: no previously-included files found matching 'docs/docsite/rst_warnings'
warning: no previously-included files found matching 'docs/docsite/rst/conf.py'
warning: no previously-included files found matching 'docs/docsite/rst/index.rst'
warning: no previously-included files found matching 'docs/docsite/rst/dev_guide/index.rst'
warning: no previously-included files matching '*' found under directory 'docs/docsite/_build'
warning: no previously-included files matching '*.pyc' found under directory 'docs/docsite/_extensions'
warning: no previously-included files matching '*.pyo' found under directory 'docs/docsite/_extensions'
warning: no files found matching '*.ps1' under directory 'lib/ansible/modules/windows'
warning: no files found matching '*.yml' under directory 'lib/ansible/modules'
warning: no files found matching 'validate-modules' under directory 'test/lib/ansible_test/_util/controller/sanity/validate-modules'
adding license file 'COPYING'
writing manifest file 'lib/ansible_core.egg-info/SOURCES.txt'

Setting up Ansible to run out of checkout...

Remember, you may wish to specify your host file with -i

Done!
```

## Задание 1-3
[link  to my_own_module.py](my_own_module.py)

## Задание 4

`python -m ansible.modules.my_own_module payload.json`
```
{"changed": true, "failed": false, "original_message": "", "message": "file was written", "invocation": {"module_args": {"path": "/tmp/text_file", "content": "Hellow world!!!"}}}
```
`python -m ansible.modules.my_own_module payload.json`
```
{"changed": false, "failed": false, "original_message": "", "message": "File exists", "invocation": {"module_args": {"path": "/tmp/text_file", "content": "Hellow world!!!"}}}
```
## Задание 5-7

`ansible-playbook local_pb.yml`
```
PLAY [Test module] *******************************************************************************************************************************************************************

TASK [Gathering Facts] ***************************************************************************************************************************************************************
ok: [localhost]

TASK [Create text file] **************************************************************************************************************************************************************
changed: [localhost]

PLAY RECAP ***************************************************************************************************************************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```

## Задание 8-9

`ansible-galaxy collection init my_own_namespace.yandex_cloud_elk`
```
> tree
.
├── README.md
├── docs
├── galaxy.yml
├── local_pb.yml
├── meta
│   └── runtime.yml
├── my_own_module.py
├── my_own_namespace-yandex_cloud_elk-1.0.0.tar.gz
├── payload.json
├── plugins
│   ├── README.md
│   └── modules
│       └── my_own_module.py
└── roles
```

## Задание 10-12
```
> tree
.
├── README.md
├── defaults
│   └── main.yml
├── files
├── handlers
│   └── main.yml
├── meta
│   └── main.yml
├── tasks
│   └── main.yml
├── templates
├── tests
│   ├── inventory
│   └── test.yml
└── vars
    └── main.yml
```





