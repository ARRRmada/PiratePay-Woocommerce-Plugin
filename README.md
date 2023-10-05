# PiratePay-Woocommerce-Plugin
 
## How to Setup PiratePay WooCommerce Plugin.

Introduction - The PiratePay WooCommerce Plugin for Wordpress.

Step #1: Download and install the PiratePay WooCommerce Plugin.
Step #2: Generate Woocommerce & PiratePay API Keys.
Step #3: Adjusting the PiratePay Settings.

Introduction - The PiratePay Payment Gateway Application.

In this guide we will be discussing how to install the WooCommerce Plugin for your Decentralized PiratePay Payment Gateway.

Please note: You will need PiratePay setup and running to use this plugin. Click here for the PiratePay app Setup Guide.


## Step #1: Download and install the PiratePay WooCommerce Plugin.
Download the latest PiratePay WooCommerce Plugin here:
https://github.com/CryptocurrencyCheckout/PiratePay-Woocommerce-Plugin/releases

There are two ways to upload the plugin, choose one of the two options below:

Option 1: Easy - Upload the Plugin inside the Wordpress Dashboard:

``` Login to your Wordpress Admin Dashboard.

Go to the Plugins Section on the left.

Click "Add New" at the top, click "Upload Plugin".

Drag and Drop the Zip file you downloaded from github, and click "Install Now"
```

Option 2: Intermediate - Upload the Plugin using an FTP/SSH backend:

``` Unzip the plugin and place the "piratepay-woocommerce-plugin" folder into your Wordpress Plugins Folder.

This folder is typically located:

Apache:
Public_html/wordpress/wp-content/plugins
Nginx:
var/www/wordpress/wp-content/plugins
```

Now that you've uploaded the plugin with one of the two methods above:

Login to your Wordpress Admin Dashboard.
Click Plugins.
Activate the "PiratePay WooCommerce Plugin".
Then click "Configure" next to the plugin.

Once here you can Enable/Disable the PiratePay plugin in your store,
as well as Enable/Disable the Email Payment Fallback option. (To display the ARRR Payment form in the Buyers Order Emails.)


## Step #2: Generate Woocommerce & PiratePay API Keys.
To get the PiratePay API URL and PiratePay API Token Keys:
Log into your PiratePay Application.

Go to the Settings Tab:
The Required details are located in the "Settings Required for Plugin:" section.
Copy and paste those details into the Woocommerce Plugin Configuration page for the PiratePay Plugin.

Now in Wordpress Admin Dashboard go to WooCommerce Section and click Settings.
Go to the Advanced Tab.
Click "REST API" in the header.

Then press "add key".

Description: PiratePay
User: Admin
Permissions: Read/Write

Click: Generate API Key


## Step #3: Adjusting the PiratePay Settings.
On the PiratePay Dashboards Settings Page:

Paste the "Consumer key" from Woocommerce into the "Platform Client Key" section.
And paste the "Consumer secret" from Woocommerce into the "Platform Client Secret" section.

This will give the PiratePay Application the ability to update the status of an order once the payment is received.

Change the Platform to "WooCommerce".

To get your "Store API Link":
Go to your Woocommerce Stores Home Page, and try to add /wp-json to the end of the url link.

Example:
https://www.MYSTORE.com/wp-json

Note: If your store is not installed as the main directory of your domain it may resemble:
https://www.MYSTORE.com/wordpress/wp-json

Go to the link - If a bunch of JSON API code is returned and Woocommerce is installed, it's safe to assume your Store API Link will be:
https://www.MYSTORE.com/wp-json/wc/v3

(You can test this link in your browser to make sure it also returns a JSON response.)

Once tested, paste the entire link into the "Store API Link" section of PiratePay's Settings Page, ending with the v3:

Example:
https://www.MYSTORE.com/wp-json/wc/v3

Submit

You should now do a low value test order to verify your Store and PiratePay are correctly communicating with each other.
