# singbox_config
My sing-box Configs &amp; Scripts
-------
**📋 Overview**
config_box.json: This is a configuration file designed for the sing-box core (bare core).
Recommended Platform: For the best experience on Android, it is highly recommended to use this with the box (Box4Magisk/BoxForMagisk) module.

**⚠️ Important Requirement**
This setup specifically requires the reF1nd fork of sing-box.
**Why reF1nd fork?**
This configuration relies on advanced features like proxy_providers and rule_providers which are essential for subscription management and automated rule updates, features that are currently not available in the upstream sing-box core.

**🚀 How to Use**
Ensure you have the reF1nd fork version of the sing-box binary installed.
If you are using Android, install the box module.
Replace the default config.json with my config_box.json (rename it to config.json if necessary for your specific environment).
Restart the service.

**🛠 Scripts**
The included scripts are helper tools for:
Updating subscription links.
Managing core services.
Automating rule provider refreshes.

**Disclaimer:** These configurations are for personal use and testing purposes only.
