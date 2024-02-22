# CMS Made Simple Version 2.2.19 - Remote Code Execution Exploit

## Overview
- **Exploit Title**: CMS Made Simple Version 2.2.19 - Remote Code Execution
- **Release Date**: 2024-21-02
- **Author**: tmrswrr
- **Vendor Homepage**: [CMS Made Simple](https://www.cmsmadesimple.org/)
- **Software Version**: 2.2.19
- **Environment Tested**: [Softaculous CMS Made Simple Demo](https://www.softaculous.com/demos/CMS_Made_Simple)

## Description
This document describes a remote code execution vulnerability in CMS Made Simple version 2.2.19. The exploit allows an authenticated user with administrative privileges to execute arbitrary PHP code through the User Defined Tags functionality.

## Steps to Reproduce
1. **Log in as Administrator**
   - Access the CMS Made Simple admin panel and log in with administrator credentials.

2. **Navigate to User Defined Tags**
   - Go to `Extensions > User Defined Tags`.

3. **Inject Payload**
   - In the 'Code' text area, input the following payload: 
     ```php
     <?php echo system('id'); ?>
     ```
   - This PHP code, when executed, will display the system user and group IDs.

4. **Execute the Payload**
   - Click on the 'Run' button to execute the payload.

5. **Observe the Output**
   - The output should be similar to:
     ```
     uid=1000(admin) gid=1000(admin) groups=1000(admin) uid=1000(admin) gid=1000(admin) groups=1000(admin)
     ```
   - This indicates successful execution of the code, displaying the server process's user and group IDs.

## Disclaimer
This information is provided for educational and research purposes only. The author is not responsible for any misuse or damage caused by this information.

## Acknowledgements
- Special thanks to the CMS Made Simple team for their continued efforts in maintaining the security of their platform.
- Thanks to all security researchers contributing to open source security.

## Contact Information
For further inquiries or reporting security issues, contact the author at `tmrswrr@email.com`.

