## Useful Ansible commands

Argument | Description | Notes
:--------: | ----------- | -----
-i | ENVIRONMENT | _e.g. dev, live, etc_
-m | MODULE | _e.g. service, shell_
-s | RUN COMMAND AS SUDO |
-a | MODULE ARGUMENTS |

##### Update sandbox code:
`sudo ansible-playbook -i <ENVIRONMENT> -l <SANDBOX_IP>,localhost sandbox.yml --tags="codeupdate"`

##### Restart a service:
`sudo ansible -i <ENVIRONMENT> app_a -m service -s -a "name=stream-writer state=restarted"`

##### Run a command:
`sudo ansible -i <ENVIRONMENT> app_a -m shell -s -a "ps aux | grep -i stream"`

##### List hosts
`sudo ansible -i <ENVIRONMENT> app_a --list-hosts`
  
