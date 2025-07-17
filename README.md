# Password-Retrieval
Logic to retrieve and backup credentials in pluto with Zero-knowledge from our side

## Password Backup
The following sequence diagrams show the workflow for creating and receiving a backup, as well as creating the backup master key. 

In general for the backup creation and backup retrieval processes there are five parites: The User, Our Chrome Extention "App", the users Pluto Device, a backup storage device, and a device which randomly creates a key at first usage here named the "Random Key Generator".

### Creating Backup Masterkey
The "Random Key Generator" is used for creating the masterkey, as well as the Pluto Device. Each of them have one partial key which is only complete when combined as shown below. The "Random Key Generator" is then saved in a secure place by the user, only to be needed if the users Pluto is ever lost.

<img width="2343" height="1350" alt="backup_sequence_UML-MasterKeyCreation" src="https://github.com/user-attachments/assets/3c9342b1-f961-4c0d-a924-3de4178869bf" />

### Creating and saving Backup
With a created key we can create a Backup as depicted in the Image below. 

<img width="2553" height="2403" alt="backup_sequence_UML-BackupWorkflow" src="https://github.com/user-attachments/assets/f45fad69-f9b4-4c09-baf7-1b30f3a805f8" />

### Retrieving Backup
The following sequence diagram shows the process of retrieving the backup in one of three ways: Pluto has the Backup Masterkey saved, Pluto did not save Masterkey but is still available, and the user lost pluto and needs a new one. In the last case note that the partial key from Pluto is saved with us if a backup version of Pluto is bought. This though does not enable us to gain insight on any backup as we do not and will not have your second partial key.

<img width="2553" height="3168" alt="backup_sequence_UML-RetrieveBackupWorkflow" src="https://github.com/user-attachments/assets/ea96ceeb-ceee-4df5-8bfe-746418d958ac" />
