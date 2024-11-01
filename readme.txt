=== Updates to Slack ===
Plugin Name: Updates to Slack
Plugin URI: https://alexpcooper.co.uk/projects/updates-to-slack/
Contributors: Cooperman
Donate link: https://alexpcooper.co.uk/donate/
Tags: slack, alerts, notifications, updates, plugins, themes, core, announcements
Requires at least: 4.0
Tested up to: 6.1
Requires PHP: 5.2
Stable tag: 2.1.0
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html


== Description ==

**Updates to Slack** is a *WordPress plugin* that informs of Core, Plugin and Theme updates, that are required on your WordPress installation, to one or more Slack channels. It does so on a daily, weekly or monthly schedule at a time of your choosing.


= Special Features =

* **Multiple Slack Channels:** Allows you to send notifications to one or more Slack channels, using [Slack's Block Kit](https://api.slack.com/block-kit)
* **Scheduled Updates:** Alerts are triggered at a time you set, on either daily, weekly or monthly intervals
* **Test Option:** Check that your alerts are being sent without waiting on the schedule
* **Ignore Plugins and Themes:** Choose which individual plugins and themes you don't want to know about, when an update is available
* **Content Permissions:** Gives you control over which users (by role) have access to post content.
* **Secure:** [Slack webhooks](https://slack.com/intl/en-gb/help/articles/115005265063-Incoming-webhooks-for-Slack) are sent from your WordPress site, on a secure URL to your Slack channel(s)
* **Reporting:**  See when a notification was last triggered and what the result was

= Support =

If you require support from me, the plugin author, you are welcome to contact me directly and place a request.


= Feedback =

If there is further functionality that would bring additional value to this plugin, please let me know.


## Copyright and License

This project is licensed under the GNU GPL, version 2 or later. 2020&thinsp;&ndash;&thinsp;2023 &copy; [Alex Cooper](https://www.alexpcooper.co.uk).


== Installation ==

Install the plugin via WordPress or by uploading the files to `/wp-content/plugins/`, as you would any other standard WordPress plugin. The directory name of the plugin needs to be "updates-to-slack".
Activate the plugin through the 'Plugins' menu in WordPress.


= How to use Updates to Slack =

Once installed and activated go to *Settings* -> *Updates to Slack*

The following options are available;
* **Slack URL(s):** Create a Slack webhooks](https://slack.com/intl/en-gb/help/articles/115005265063-Incoming-webhooks-for-Slack) for your channel and enter it in here (ie. https:// hooks.slack.com/services/...). For multiple URLs, simply add additional Slack webhooks, one per line, in this field
* **Slack Alerts Enabled?:** *Yes* to enable, *No* to prevent alerts. useful if you're also running a Development installation
* **Site Name:** If left blank, your site name is taken from the one entered in the General Settings of your WordPress site
* **Next Scheduled Run Time:** Enter a date and time of the next trigger
* **Frequency:** How often the trigger will run following the Next Scheduled Run Time; Daily, Weekly or Monthly
* **Last Run:** Tells you the date and time of the last trigger
* **Last Run Slack Response:** The outcome of the last trigger (usually either "No updates available", meaning it had no reason to send a message to your Slack channel, or "OK" if Slack received the message without any issues)
* **Test:** A button that allows you to trigger a check immediately. Useful for testing purposes
* **Ignore Plugins and Themes:** Allows you to select which of your themes and plugins you don't wish to be notified about when there is an update



== Frequently Asked Questions ==
= Where do I get a Slack web hook from? =
See [Slack webhooks](https://slack.com/intl/en-gb/help/articles/115005265063-Incoming-webhooks-for-Slack). You can usually get a URL from your Slack account by going to Settings & Administration -> Manage Apps -> Custom Integrations and creating an Incoming Webhook.

= Why is the automated alert not working? =
This runs off the WordPress scheduler so you would need to make sure that your WordPress cron is set up and running.


= Why Ignore Plugins and Themes? =
The idea behind this was that you may have plugins that, should an update occur, would deprecate functionality on your site and updating it isn't an option then you may not want to hear via every scheduled alert that there's an update out the for it. Similarly, with themes, you may be keeping a native WordPress theme, such as twenty twenty-one for troubleshooting but you don't actually need to immediately address any available updates for it.


= Are there security concerns? =
It isn't advised to keep a WordPress site on a live environment with updates required. The purpose of this plugin is quick notification, straight to your screen, of when updates are needed / available, especially with the Core of WordPress (which is why you're unable to "ignore" a Core update). The purpose behind ignoring plugins and themes is designed to reduce "notification overload" so that you're in control of the alerts you are sent and aren't bombarded with needless information for themes and plugins that you don't need to be informed about.


= What are the plugin's limitations? =
* This plugin has been tested on WordPress core versions 4.0 onwards.
* This plugin has been tested on a WordPress Multisite environment.
* If there's a demand to continue to add further functionality to this plugin then I am open to doing so. In the meantime I intend to keep it working on new versions of WordPress.
* The plugin author accepts no liability for any losses or damage caused as a result of this plugin not alerting to updates.


== Changelog ==
2.1.0, February 2023
* Fix to Cron Scheduler
* Fix to Support Footer

2.0.0, January, 2023
* Whole new rebuild, from the ground up (same interface)
* Fixed bug when removing all ignored plugins or all ignored themes
* Fixed bug in outputting headers during test, if php warnings are enabled
* Backwards compatible

1.4.5, January, 2022
* Tested on WordPress 5.9
* Fixed error shown when setting didn't pre-exist

1.4.4, March, 2021
* Fix for retrieving cron data in the admin settings

1.4.3, April, 2021
* Tested for WordPress 5.7.1

1.4.2, March, 2021
* Tested for WordPress 5.7

1.4.1, February, 2021
* Fixed typo in alert
* Prevented test being triggered until a Slack URL is initially saved
* Improved reporting on test results / trigger feedback

1.4.0, February, 2021
* First public release

1.4.1, February the 3rd 2021
* Corrected typo on the Slack notification for core update ("verson" to "version")
* Disabled "Trigger Slack Alert" button until a Slack URL has been entered and saved


== Upgrade Notice ==
Version 1.4.0 is the first public release of this plugin.


== Screenshots ==
1. Main settings page
2. Ignore Plugins and Themes
3. Menu option
4. Slack alert (version 1)
5. Slack alert (version 2+)
5. Slack alert test (version 2+)