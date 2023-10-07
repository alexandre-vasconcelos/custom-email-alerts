Wazuh

This integration allows the user to send fully customizable email alerts.
Requisite:
Postfix installed and configured follow https://documentation.wazuh.com/4.2/user-manual/manager/manual-email-report/smtp-authentication.html
 
Add an integration in file ossec.conf 
<integration>
<name>custom-email-alerts</name>
   <hook_url>emailrecipient@example.com</hook_url>
   <level>12</level>
   <alert_format>json</alert_format>
</integration>


Create the file   /var/ossec/integrations/custom-email-alerts

Permission:
chmod 750 /var/ossec/integrations/custom-telegram/custom-email-alerts
chown root:wazuh /var/ossec/integrations/custom-email-alerts

Copy the code inside file custom-email-alerts and paste in /var/ossec/integrations/custom-email-alerts

You can customized the subject and a part of body in the generate_msg() function

lines:
