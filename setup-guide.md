# Setup Guide

## 1. Install Wazuh

* Install Wazuh Manager
* Configure agents

## 2. Configure Webhook Integration

Edit:

```
/var/ossec/etc/ossec.conf
```

Add:

```
<integration>
  <name>shuffle</name>
  <hook_url>https://shuffler.io/api/v1/hooks/WEBHOOK_ID</hook_url>
  <level>5</level>
  <alert_format>json</alert_format>
</integration>
```

Restart:

```
sudo systemctl restart wazuh-manager
```

## 3. Configure Shuffle

* Create workflow
* Add webhook trigger
* Add processing nodes

## 4. Configure TheHive

* Install TheHive
* Configure application.conf
* Connect to Cassandra

## 5. Test Workflow

```
curl -X POST <webhook_url> -d '{"test":"mimikatz"}'
```

Verify in Shuffle Debug tab
