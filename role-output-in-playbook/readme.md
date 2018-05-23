## Storing role output to a variable
This playbook can be used to store the output of a role to variable. Usually the output of a role is stored using the "register" module in Ansible. But in case you have multiple playbooks calling the same role to execute a task, the "register" module will not be able to help you out much. This is where the use of this playbook comes into power.

This playbook stores the values of the output of a role in a JSON format with the fields in a key value pair. When the role is called multiple times by different playbooks we can store the different outputs in the same variable, as different keys.

First we initialise the variable (output) in which we want to store the output using "set_facts" under tasks in the playbook. Under tasks we specify the role we want to execute using "include_role". We also specify the name of the key (output_name) under vars.

In the role, after we have executed the module we want, we register the value in a dummy variable (role_output). Then we use the "set_fact" module to store the dummy variable to the variable we have defined using combine in JSON format. You can print the variable after it stores it t view the format of how it being stored.

### Warning!!
When initializing the variable (output) it should be done only in the playbook which will be run first. If you keep initializing it in all the playbooks then the value of the variable will be reset each time and you will not get the desired output. 
