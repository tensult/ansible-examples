# ansible-examples

### [Passing data between roles](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-roles)
* [input-set](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-roles/roles/input-set) sets fact **foo** to bar.
* [input-get](https://github.com/tensult/ansible-examples/blob/master/pass-data-between-roles/roles/input-get) gets fact **foo** using debug module.
* To run:
    ```
    cd pass-data-between-roles
    ansible-playbook playbook.yml
    ```