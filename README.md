# spring_LDAP
in this first i am providing some notes so that, who ever may be working or learning for them easy to understand the ldap structre.
**************************************************************************************************************************************
apache active directory
************************

DIT=Directory information trees
o=Organization
DN=Distigusih Name
OU=Organization Unit
CN= Common Name
SN= SurName


In order to use the apache Active directory

==> first we need to create server and connection
==> in studio there is LDAP Servers tab , using that we can create server.
==> once server is created, right click on the server and click on create connection then connection is created. we can check in the connections tab.
==> with connection, LDAP browser you can find the some other attributes.like DIT, searches and bookmarks.
==> start the server, once server started, docuble click on connection, the under DIT u can find the 2 or 3 sub trees
==> Expand the Root DSE folder. There are two sub-entries: ou=schema,ou=schema and ou=system.These are partitions in the server. Do not modify them unless you know what you're doing. 


crateing a new partitions
***************************

==> Right click on server and selet open configuration. Then configuration panel will be opened.
==> In that tab, bottom side there will be 5 tabs will be there. Select partitions tab .
==> To create partition, click on add button , change the ID value to MOJO, cache size to 100(if not  100) and suffix value o=MOJO
==> Restart the server and refresh the ldap browser.
==> Double click on ROOT DSE. one panel opend in that u can find "namingcontexts: o=MOJO".
==> To see MOJO under ROOT node, we need to add organization.


Creating Organation:(O)
***************************

==> Right Click on ROOT DSE,click on new and new entry. 
==> Select create from scratch and click on next, Object classed window will be opened.
==> Type or select the Organization and click on add to add it, then click next button. Distingushed name window will be opened.
==> In RDN type o and value is MOJO and click on next, now attributes of the organization will come and click in finish.
==> Then see the ROOT DSE you can see the MOJO as a organization.

creating Organization units::(OU)
***********************************
==> Goto DIT, right click on "o=MOJO", click on new and new entry.
==> Select create from scratch and click on next, Object classed window will be opened.
==> Type or select the OrganizationalUnit and click on add to add it, then click next button. Distingushed name window will be opened.
==> In RDN type ou and value is users and click on next, now attributes of the organizationUnit(users) will come and click in finish.
==> Then see under ="MOJO", one unit users with will be appear.(ou=users).


creating users under the organization:
**************************************

==> Goto Root DSE,and select one OU, under which u want to create the users.
==> Right click on the users(OU),  click on new and new entry. 
==> Select create from scratch and click on next, Object classed window will be opened.
==> Type or select the inetOrgPerson and click on add to add it, then click next button. Distingushed name window will be opened.
==> Observe the window that, parent will contains ou=users,o=MOJO.
==> In RDN type cn and value is username and click on next, now attributes of the person of (users) will come and enter SN(sur name)click in finish.
==> Then see under ="users", one unit person with will be appear.(ou=users).

==> 




******************************************************************************************************
