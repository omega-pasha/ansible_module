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


