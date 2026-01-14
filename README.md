# Password-Retrieval
Logic to retrieve and backup credentials in pluto with Zero-knowledge from our side

## Password Backup
The following sequence diagrams show the workflow for creating and receiving a backup, as well as creating the backup master key. 

In general for the backup creation and backup retrieval processes there are five parites: The User, Our Chrome Extention, the users Pluto Device, a backup storage device, and a place to save the (symmetric) encryption key securely when setting up the backup functionality - although this is not specifically added in the diagramme below.

### Creating Backup Masterkey and saving Backup
The Chrome Extentions Password Creation functionality is used for creating the masterkey/ backup password. This key is saved on the users pluto as well as securely at a place of the users whishing. First functionality should be USB-Stick or desktop. 

<img width="2343" height="1686" alt="backup_sequence_UML-MasterKeyCreation_NEW" src="https://github.com/user-attachments/assets/b5be3bad-6d95-43a0-aaa0-b848e7e209d8" />


### Retrieving Backup
The following sequence diagram shows the process of retrieving the backup when Pluto has been lost. Thereby the saved symmetric password is used to reupload the password vault to the new Pluto device. Afterwards a new password is created for any future backup processes.

<img width="2553" height="2961" alt="backup_sequence_UML-RetrieveBackupWorkflow_NEW" src="https://github.com/user-attachments/assets/d953486c-b8d9-4c31-8ed3-1d42120af41c" />
