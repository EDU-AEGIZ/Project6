# PROJECT 6: WEB SOLUTION WITH WORDPRESS
## In this project I'm to prepare storage infrastructure on two Linux servers and implement a basic web solution using WordPress


`First i created 2 "Red heart" instances i named one "Web Server and the other "Database Server" `

![Servers](./Images/1.ServersDone.JPG)


`Icreated 10gb 3 volumesand attched the volumes to my web-server instnace  `

![Servers](./Images/2b.Createdand%20AttachedVolumes.JPG)

`I connected to my web server instance and confirmed that the volumes were attached using the lsblk command `

![Servers](./Images/3.ConnectedToInstanceandConfirmedAttachedVolumes.JPG)


`I created partitions on the three disk using the gdisk command on the webserver instance `

![Partitions created](./Images/7.iconfirmedMyPrtitionsUsingtheLsblkCommand.JPG)


` i Installed Lvm2 using the Yum Manager `

![Servers](./Images/8.InstalledLvm2UsingTheYumManager.JPG)


`I created physical volume on each Disk using the Pvcreate-Command `

![Servers](./Images/9.IcreatedPhysicalVolumeonEachDiskUsingThePvcreate-Command.JPG)




`I created volume group and but them in the group aftwer which i created two logical volumes with them  `

![Servers](./Images/10.VolGroupWasSuccessfullyCreated.JPG)

![Servers](./Images/11.created.JPG)



`I formatted both volumes `

![Servers](./Images/12FileSystemCreated.JPG)

![Servers](./Images/14.FileSytemcreatedOnApp-lv.JPG)


`I made two directory var/www/html and home/recovery/logs mounted one of the volumes i named app-lv on the var/wwww/html directory `

![Servers](./Images/15.MountedAnditworkedAftercreatingDirectories%20as%20listed%20on%20my%20Documentation.JPG)



`I backed up the second direcrtory (home/recovery/logs) using the Rsync command afterwhich i mounted the second volume log-lv on the directory  `

![Servers](./Images/16Useed%20Rsync%20Command%20To%20back%20up%20all%20files.JPG)


![Servers](./Images/17.FilesCopiedBack.JPG)



`I backed up the second direcrtory (home/recovery/logs) using the Rsync command afterwhich i mounted the second volume log-lv on the directory  `

![Servers](./Images/17.FilesCopiedBack.JPG)


`i edited Fstab to add the path for the files  `

![Servers](./Images/18.EditedFstabToAdd%20The%20path%20for%20the%20files.JPG)


`I initiated FStab update  `

![Servers](./Images/19.FxStabUpdated.JPG)


`I went back to my AWS and created as well attached 3 volumes to my database instance`

![Servers](./Images/20.VolumesCreated%20and%20attached%20to%20database%20server.JPG)

`I connected to my instance and confirmed that the volumes were attached after which i partitioned them using the gdisk command  `

![Servers](./Images/21.Connected%20to%20database%20server.JPG)

![Servers](./Images/22.AttachedVolumes%20Confirmed.JPG)

![Servers](./Images/23.Partitioned%20all%20The%20Disk%20on%20Database%20Server.JPG)


`I installed Lvm2 Using The Yum Manager  after which i created physical volumes on the partitions`

![Servers](./Images/24.Installed%20Lvm2%20Using%20The%20Yum%20Manager.JPG)

![Servers](./Images/25.Icreated%20Physical%20Volume%20on%20Each%20Disk%20Using%20Th%20ePvcreate-Command.JPG)


`I cretaed the volume group which i needed to do before i now created logical volume and formated using "ext4" `

![Servers](./Images/26.Vol%20Group%20Was%20Successfully%20Created.JPG)

![Servers](./Images/27.Logical%20Volume%20Was%20Successfully%20Created.JPG)


![Servers](./Images/28.FileSystemCreated.JPG)


`I mounted it on a new directory i made and it worked as listed on my Documentation `


[Servers](./Images/29.%20.MountedAnd%20it%20workedAftercreatingDirectories%20as%20listed%20on%20my%20Documentation.JPG)



`i edited Fstab to add the path for the files and as well checked to confirm mount was succesful`

![Servers](./Images/30.EditedFstabToAdd%20The%20path%20for%20the%20files.JPG)


![Servers](./Images/31.cHECKED%20TO%20CONFURM%20MOUNT%20WAS%20SUCCESSFUL.JPG)



`I installed PHP and checked to confirm that my http was installed and running. I checked to be sure my apache was up on browser using ip address`

![Servers](./Images/34.%20Installed%20PHP.JPG)

![Servers](./Images/35.%20Httpd%20Installed%20and%20Running.JPG)

![Servers](./Images/36.ApacheWorkingFineUsingPublic%20IP%20Address.JPG)

#Pls kindly note that i changed to a new instance and contionued my documentation from the last place i stopped on my previos instance... Thank you


`I created the wordpress directory and cd'ed into it and downloaded wordpress on the directory after which, i extracted wordpress and copied the contents in Config-sample to a new file "config" on my wordpress`

![Servers](./Images/37.I%20created%20the%20wordpress%20directory%20and%20cd%20into%20it%20and%20downloaded%20wordpress%20on%20the%20directory.JPG)

![Servers](./Images/38.%20I%20extracted%20wordpress.JPG)

![Servers](./Images/39.%20I%20copied%20content%20in%20Config-sample%20to%20config%20on%20my%20wordpress.JPG)


`I copied content of wordpress to html directory after which I  installed and enabled mysql on the webserver and did the same for data base server`

![Servers](./Images/40.%20I%20copied%20content%20of%20wordpress%20to%20html%20directory.JPG)

![Servers](./Images/41.%20I%20%20installed%20and%20enabled%20mysql%20on%20the%20webserver.JPG)

![Servers](./Images/42.%20I%20%20installed%20and%20enabled%20mysql%20on%20the%20database%20server.JPG)


`I crated user,database and granted privileges on mysql`

![Servers](./Images/43.I%20crated%20user%20%2Cdatabase%20and%20granted%20privileges%20on%20my%20sql.JPG)


`I edidted my cnf file to bind adress to red heart allowing traffic from anywhere`

![Servers](./Images/44.%20i%20edidted%20my%20cnf%20file%20to%20bind%20adress%20to%20red%20heart%20allowing%20traffic%20from%20anywhere.JPG)

`I edited the wp-config file and updtaed the database,user name and ip address and confirmed and both servers were communicating ell and connecting using ip address`

![Servers](./Images/45.I%20edited%20the%20wp-config%20file%20and%20updtaed%20the%20database%20%2C%20user%20name%20and%20ip%20address.JPG)

![Servers](./Images/46.%20Both%20servers%20are%20communicating%20ell%20and%20connecting%20using%20ip%20address.JPG)


`I chnaged onwership of html to include apache `

![Servers](./Images/47.I%20chnaged%20onwership%20of%20html%20toinclude%20apache.JPG)


` I set the paramaters to ensure it connects `

![Servers](./Images/48.%20I%20set%20the%20paramaters%20to%20ensure%20it%20connects.JPG)


`Wordpress is installed and working perfectly `

![Servers](./Images/49.%20Wordpress%20is%20installed%20and%20working%20perfectly.JPG)


