# Zabbix Seatalk Webhook Script

This script allows you to send Zabbix alerts to the Seatalk API via a webhook. It is designed to send a custom message with alert details to a specific Seatalk group based on the provided parameters.

## Parameters

The script uses two main parameters:

- **ALERT_MESSAGE**: The message content that you want to send to Seatalk.
- **GROUP_ID**: The unique identifier for the Seatalk group where the message will be sent.

### Example Usage

To use this script, you need to provide the following parameters:

- `ALERT_MESSAGE`: The message you want to send to the group.
- `GROUP_ID`: The identifier of the Seatalk group where the alert will be posted.

### Example Command

Here's an example of how to use the script:

```bash
curl -i -X POST -H 'Content-Type: application/json' -d '{
    "ALERT_MESSAGE": "Disk usage is over 90%",
    "GROUP_ID": "pv84sS8nTxqHfMfKuCvpQg"
}' https://openapi.seatalk.io/webhook/group/{GROUP_ID}
