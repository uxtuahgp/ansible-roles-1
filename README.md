## Ansible Roles Homework ##  


### Task 1 ###  
Made a requirements.yml as it's requested, but it does not work, because it's based on  CentOS 7 and dont work at Fedora 37.  
So, created clickhouse my own repo at git@github.com:uxtuahgp/clickhouse-role.git  
```  
---
  - src: git@github.com:uxtuahgp/clickhouse-role.git
    scm: git
    version: "1.0.0"
    name: clickhouse 

```  
### Task 2 ###  
Downloaded my own role from github repo
```  
$ ansible-galaxy role remove clickhouse
- successfully removed clickhouse
$  ansible-galaxy install -r requirements.yml
Starting galaxy role install process
- extracting clickhouse to /home/alex/.ansible/roles/clickhouse
- clickhouse was installed successfully

```  
### Task 3 ###  
Created vector role with  
```  
ansible-galaxy role init vector
```  
### Task 4 ###  
Created dafault and private vars for vector role  
vector_version can be changed by user
### Task 5 ###  
Moved templates from playbook inside of roles  
### Task 6 ###  
Described roles in README.md files  
### Task 7 ###  
Have made the same things for lighthouse role  
### Task 8 ###  

Added version tag for clickhouse role  
```  
$ git tag -a 1.0.0 -m "Set version tag as requested"
$ git push origin 1.0.0
Перечисление объектов: 1, готово.
Подсчет объектов: 100% (1/1), готово.
Запись объектов: 100% (1/1), 178 байтов | 178.00 КиБ/с, готово.
Всего 1 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To github.com:uxtuahgp/clickhouse-role.git
 * [new tag]         1.0.0 -> 1.0.0

```  


### Task 9 ###  
Modified playbook to use roles instead of set of tasks  
```  
---
- hosts: clickhouse
  roles:
    - {role: clickhouse}


- hosts: vector
  roles:
    - {role: vector}

- hosts: lighthouse
  roles:
    - {role: lighthouse}
```  
### Task 10 ###  
Uploaded the playbook to github  
### Task 11 ###  
Vector role:               git@github.com:uxtuahgp/vector-role.git  
Lighthouse role:           git@github.com:uxtuahgp/lighthouse-role.git  
My own clickhouse role:    git@github.com:uxtuahgp/clickhouse-role.git  





