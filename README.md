Forefront TMG Responsive Authorization Forms
======================

Responsive (Mobile Friendly) Authentication Forms for Microsoft Forefront TMG

#Purpose

This project contains a set of templates for Microsoft Forefront Threat Management Gateway to make logging into
published websites easier on mobile devices.

#Installation

1. Duplicate the existing ISA Templates folder at:
C:\Program Files\Microsoft Forefront Threat Management Gateway\Templates\CookieAuthTemplates\ISA

2. Call the duplicated folder 'Custom' (or whatever takes your fancy). You should now have a folder here:
C:\Program Files\Microsoft Forefront Threat Management Gateway\Templates\CookieAuthTemplates\Custom

3. Copy the usr_pwd.htm and the styles_responsive.css files into the Custom Folder and replace the existing file.

4. In your TMG Management console, edit your desired Web Publishing rule and go to the Listener page. Click Properties.

5. On the Authentication page, ensure HTML Forms Authentication is selected.

6. On the Forms Tab enter 'Custom' (you don't need to enter the entire path, just the word 'Custom' without the quotes)

7. Apply the changes. 

8. Restart the TMG Firewall Service (yeah, I know...  Unfortunately TMG Caches these pages and restarting the service is the only way to clear it as far as I know). 

