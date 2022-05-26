This is the read me file for the Shell permissions tasks.

0-iam_betty
#!/bin/bash 
su betty                   // this script switches the current user to the user betty.//

1-who_am_i
#!/bin/bash 
whoami                     // this script prints the effective username of the current user. //

2-groups
#!/bin/bash 
groups                      //this script prints all the groups the current user is part of. //

3-new_owner 
#!/bin/bash 
chown betty hello          // this script changes the owner of the file hello to the user betty. //

4-empty
#!/bin/bash
touch hello                 //this script creates an empty file called hello.//

5-execute
#!/bin/bash 
chmod u+x hello             //this script adds execute permission to the owner of the file hello.//

6-multiple_permissions
#!/bin/bash 
chmod ug+x,o+r hello       // this script adds execute permission to the owner and the group owner, and read permission to the users, to the file hello. //

7-everybody                 
#!/bin/bash 
chmod a+x hello             //this script adds execution permission to the owner, the group owner and the other users, to the file hello.//

8-James_Bond
#!/bin/bash 
chmod 007 hello            // this script sets the permission to the file hello as no permission at all to owner, no permission at all to group, and all permissions to the other users//

9-John_Doe                
#!/bin/bash 
chmod 753 hello                   //this script sets the mode of the file hello to that.//

10-mirror_permissions
#!/bin/bash 
chmod --reference=olleh hello     //this script sets the mode of the file hello the same as olleh's mode.//

11-directories_permissions
#!/bin/bash 
chmod a+X *                       //this scipt adds execute permissions to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.//

12-directory_permissions
#!/bin/bash 
mkdir -m 751 my_dir               //this script creates a directory called my_dir with permissions 751 in the working directory.//
 
13-change_group
#!/bin/bash 
chgrp school hello                //this script changes the group owner to school for the file hello.//

14 100-change_owner_and_group
#!/bin/bash 
chown vincent:staff *             //this script changes the owner to vincent and the group to staff for all the files and directores in the working directory. //

15 101-symbolic_link_permissions
#!/bin/bash 
chown -h vincent:staff _hello    // This script changes the owner and the group owner to _hello to vincent and staff respectively. //

16 102-if_only 
#!/bin/bash 
chown --from=guillaume betty hello      //This script changes the owner of the file hello to betty only if it is owned by the user guillaume//

17 103-Star_Wars
#!/bin/bash 
telnet towel.blinkenlights.nl           //this script will play the starwarz iv episode in the terminal//

