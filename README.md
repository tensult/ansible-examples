# ansible-examples

### [How to implement own module](https://github.com/tensult/ansible-examples/blob/master/own-module-example)
* [library/test.sh](https://github.com/tensult/ansible-examples/blob/master/own-module-example/library/test.sh) contains a simple test module.
* In [playbook.xml](https://github.com/tensult/ansible-examples/blob/master/own-module-example/playbook.yml), we are calling this module.
* To run:
    ```
    cd own-module-example
    ansible-playbook playbook.yml

### [Passing data between roles](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-roles)
* [input-set](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-roles/roles/input-set) sets fact **foo** to bar.
* [input-get](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-roles/roles/input-get) gets fact **foo** using debug module.
* To run:
    ```
    cd pass-data-between-roles
    ansible-playbook playbook.yml
    ```

### [Passing data between playbooks](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-playbooks)
* [playbook1](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-playbooks/playbook1) sets fact **foo** to bar.
* [playbook2](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-playbooks/playbook2) gets fact **foo** using debug module.
* To run:
    ```
    cd pass-data-between-playbooks
    ansible-playbook masterplaybook.yml
    ```
### [Role output in playbooks](https://github.com/tensult/ansible-examples/tree/master/role-output-in-playbook)
* [masterplaybook](https://github.com/tensult/ansible-examples/blob/master/role-output-in-playbook/masterplaybook.yml) is the main playbook which is used to call a sample role whose output is stored in the variable "output".
* The sample role [echo](https://github.com/tensult/ansible-examples/tree/master/role-output-in-playbook/roles/echo) has a  [task defined](https://github.com/tensult/ansible-examples/blob/master/role-output-in-playbook/roles/echo/tasks/main.yml) which stores the output of the role into the variable in JSON format.
* To run:
    ```
    cd role-output-in-playbook
    ansible-playbook masterplaybook.yml
    ```
