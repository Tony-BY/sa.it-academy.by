## 08.Ansible_Workshop

### Output_from_playbook
```bash
root@ubunru22:/home/sergey/08.Ansible.WS/homework# ansible-playbook -i inv.yaml redmine.yaml

PLAY [redmine] **********************************************************************************************************************************************

TASK [Gathering Facts] **************************************************************************************************************************************
Saturday 03 September 2022  11:30:41 +0300 (0:00:00.012)       0:00:00.012 **** 
ok: [redmine_14]

TASK [Show ansible host] ************************************************************************************************************************************
Saturday 03 September 2022  11:30:43 +0300 (0:00:02.122)       0:00:02.134 **** 
ok: [redmine_14] => {
    "msg": "192.168.201.14"
}

TASK [mysql : MySQL.Install MYSQL] **************************************************************************************************************************
Saturday 03 September 2022  11:30:43 +0300 (0:00:00.046)       0:00:02.181 **** 
ok: [redmine_14]

TASK [mysql : MySQL.Create DB] ******************************************************************************************************************************
Saturday 03 September 2022  11:30:46 +0300 (0:00:02.419)       0:00:04.600 **** 
ok: [redmine_14]

TASK [mysql : MySQL.Create DB User] *************************************************************************************************************************
Saturday 03 September 2022  11:30:46 +0300 (0:00:00.667)       0:00:05.268 **** 
ok: [redmine_14]

TASK [redmine : Redmine. Install packages] ******************************************************************************************************************
Saturday 03 September 2022  11:30:47 +0300 (0:00:00.706)       0:00:05.975 **** 
ok: [redmine_14]

TASK [redmine : Redmine. Clone repository] ******************************************************************************************************************
Saturday 03 September 2022  11:30:50 +0300 (0:00:02.509)       0:00:08.484 **** 
ok: [redmine_14]

TASK [redmine : Redmine. Change permissions] ****************************************************************************************************************
Saturday 03 September 2022  11:30:50 +0300 (0:00:00.680)       0:00:09.165 **** 
ok: [redmine_14]

TASK [redmine : Redmine. Change permissions] ****************************************************************************************************************
Saturday 03 September 2022  11:30:51 +0300 (0:00:00.660)       0:00:09.825 **** 
ok: [redmine_14]

TASK [redmine : Redmine. Config database] *******************************************************************************************************************
Saturday 03 September 2022  11:30:51 +0300 (0:00:00.540)       0:00:10.366 **** 
ok: [redmine_14]

TASK [redmine : Redmine. Setup 01] **************************************************************************************************************************
Saturday 03 September 2022  11:30:52 +0300 (0:00:00.964)       0:00:11.330 **** 
changed: [redmine_14]

TASK [redmine : Redmine. Session store secret generation] ***************************************************************************************************
Saturday 03 September 2022  11:30:57 +0300 (0:00:04.747)       0:00:16.078 **** 
ok: [redmine_14]

TASK [redmine : Redmine. Setup 02] **************************************************************************************************************************
Saturday 03 September 2022  11:30:58 +0300 (0:00:00.518)       0:00:16.596 **** 
changed: [redmine_14]

TASK [redmine : Redmine. Configuration files for virtualhost] ***********************************************************************************************
Saturday 03 September 2022  11:31:10 +0300 (0:00:12.552)       0:00:29.150 **** 
ok: [redmine_14]

TASK [redmine : meta] ***************************************************************************************************************************************
Saturday 03 September 2022  11:31:11 +0300 (0:00:00.895)       0:00:30.045 **** 

TASK [add redmine-14.sa to host file] ***********************************************************************************************************************
Saturday 03 September 2022  11:31:11 +0300 (0:00:00.049)       0:00:30.095 **** 
changed: [redmine_14]

TASK [uri] **************************************************************************************************************************************************
Saturday 03 September 2022  11:31:12 +0300 (0:00:00.489)       0:00:30.584 **** 
ok: [redmine_14]

TASK [lineinfile] *******************************************************************************************************************************************
Saturday 03 September 2022  11:31:12 +0300 (0:00:00.794)       0:00:31.378 **** 
changed: [redmine_14]

PLAY RECAP **************************************************************************************************************************************************
redmine_14                 : ok=17   changed=4    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

Saturday 03 September 2022  11:31:13 +0300 (0:00:00.661)       0:00:32.040 **** 
=============================================================================== 
redmine : Redmine. Setup 02 ------------------------------------------------------------------------------------------------------------------------- 12.55s
redmine : Redmine. Setup 01 -------------------------------------------------------------------------------------------------------------------------- 4.75s
redmine : Redmine. Install packages ------------------------------------------------------------------------------------------------------------------ 2.51s
mysql : MySQL.Install MYSQL -------------------------------------------------------------------------------------------------------------------------- 2.42s
Gathering Facts -------------------------------------------------------------------------------------------------------------------------------------- 2.12s
redmine : Redmine. Config database ------------------------------------------------------------------------------------------------------------------- 0.96s
redmine : Redmine. Configuration files for virtualhost ----------------------------------------------------------------------------------------------- 0.90s
uri -------------------------------------------------------------------------------------------------------------------------------------------------- 0.79s
mysql : MySQL.Create DB User ------------------------------------------------------------------------------------------------------------------------- 0.71s
redmine : Redmine. Clone repository ------------------------------------------------------------------------------------------------------------------ 0.68s
mysql : MySQL.Create DB ------------------------------------------------------------------------------------------------------------------------------ 0.67s
lineinfile ------------------------------------------------------------------------------------------------------------------------------------------- 0.66s
redmine : Redmine. Change permissions ---------------------------------------------------------------------------------------------------------------- 0.66s
redmine : Redmine. Change permissions ---------------------------------------------------------------------------------------------------------------- 0.54s
redmine : Redmine. Session store secret generation --------------------------------------------------------------------------------------------------- 0.52s
add redmine-14.sa to host file ----------------------------------------------------------------------------------------------------------------------- 0.49s
redmine : meta --------------------------------------------------------------------------------------------------------------------------------------- 0.05s
Show ansible host ------------------------------------------------------------------------------------------------------------------------------------ 0.05s
Playbook run took 0 days, 0 hours, 0 minutes, 32 seconds
```

### Printscreen my project in application (redmine-14.sa)
![my_project_redmine](https://user-images.githubusercontent.com/49452234/188276350-5b27d0ec-3280-48b6-9a73-22579648a8f5.jpg)

