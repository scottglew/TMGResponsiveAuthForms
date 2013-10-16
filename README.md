Forefront TMG Responsive Forms Based Authentication Templates
======================

Forms based authentication templates for Forefront TMG to make logging in easier on mobile devices.

#Purpose

This project contains a set of custom templates you can use when publishing websites using Forefront TMG and Forms Based Authentication. These templates are fully [responsive](http://en.wikipedia.org/wiki/Responsive_web_design) to provide a  nicer experience when logging into your secured sites using a smart phone or tablet.

This default form ![Default Forefront TMG Forms Authentication on iPhone](http://www.fastvue.co/wp-content/uploads/2012/08/ForefrontTMGFormsAuthenticationOniPhone-200x300.png "Default Forefront TMG Forms Authentication on iPhone")
becomes ![Responsive Forefront TMG Forms Authentication on iPhone](http://www.fastvue.co/wp-content/uploads/2012/08/ForefrontTMGMobileFriendlyAuthenticationOniPhone-200x300.png "Responsive Forefront TMG Forms Authentication on iPhone")

The form also scales nicely for tablets and normal desktops / large screens.

![Responsive Forefront TMG Forms Authentication on Desktop](http://www.fastvue.co/wp-content/uploads/2012/09/ForefrontTMGMobileFriendlyAuthenticationOnDesktop-300x187.png "Responsive Forefront TMG Forms Authentication on Desktop")

There is also a template for Exchange OWA, both with and without the Exchange 2013 style. Here's the Exchange 2013 template:

![Forefront TMG Forms Based Authentication Template for Exchange 2013 - Desktop](http://www.fastvue.co/wp-content/uploads/2013/10/Desktop-300x154.png "Forefront TMG Forms Based Authentication Template for Exchange 2013 - Desktop")

![Forefront TMG Forms Based Authentication Template for Exchange 2013 - Mobile](http://www.fastvue.co/wp-content/uploads/2013/10/Mobile-187x300.png "Forefront TMG Forms Based Authentication Template for Exchange 2013 - Mobile")


#Installation

1. For Outlook Web Access, copy the existing Exchange Templates folder on your Forefront TMG Server at:
	`C:\Program Files\Microsoft Forefront Threat Management Gateway\Templates\CookieAuthTemplates\Exchange`

	For all other sites, copy the existing ISA Templates folder at:
	`C:\Program Files\Microsoft Forefront Threat Management Gateway\Templates\CookieAuthTemplates\ISA`

2. Call the duplicated folder 'Custom' (or whatever takes your fancy). You should now have a folder here:
	`C:\Program Files\Microsoft Forefront Threat Management Gateway\Templates\CookieAuthTemplates\Custom`

3. Copy all files under the **HTML** folder of your desired template (either ISA, Exchange or Exchange2013) in this project into the corresponding HTML sub-folder of your **Custom** Folder and replace the existing files. For example, copy all files from **Exchange2013\HTML** into your **Custom\HTML** folder. Use either of the *Exchange* templates for OWA, and the *ISA* versions for everything else. Feel free to replace Logo.png with your own custom logo.

4. In your TMG Management console, edit your desired *Web Publishing rule* and go to the *Listener* page. Click **Properties**.

5. On the **Authentication** tab, ensure *HTML Forms Authentication* is selected.

6. On the **Forms** tab enter 'Custom' (you don't need to enter the entire path, just the word 'Custom' (or whatever you specified in step 2) without the quotes).

7. If you used the Exchange Publishing Wizard in Forefront TMG, you also need to go to the **Application Settings** tab and enter 'Custom' (or whatever you specified in step 2) in the 'Type the custom HTML for set directory' edit box.

7. Apply the changes. 

8. Restart the TMG Firewall Service (yeah, I know...  Unfortunately TMG Caches these pages and restarting the service is the only way to clear it as far as I know). 

Browse to the site and Forefront TMG will present the new authentication page. Try it on a smart phone or tablet and marvel at its beauty. 

#Issues

For now, only the usr_pwd.htm file has been customized. This file is served only when using Windows (Active Directory) authentication (set on the Authentication page in step 5 above). If you're using Radius or SecureID, feel free to contribute to the project! :)

#Credits
1. Responsive goodness is provided mainly by the scaffolding and forms components in [bootstrap](http://twitter.github.com/bootstrap)
2. The inspiration for this project came from a web development request from Etienne Liebetrau of [Fix My IT System](http://fixmyitsystem.com)
3. Thanks to [Richard Hicks](http://tmgblog.richardhicks.com) and [Will Smothers](http://www.linkedin.com/in/willsmothers) for their testing of the Exchange 2013 template.