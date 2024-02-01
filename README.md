# Azure commands

## Check Subscription Azure Availability physical - to compare AZs between AZs

Update to your region, e.g. eastus

```
az rest --method get --uri '/subscriptions/{subscriptionId}/locations?api-version=2022-12-01' --query 'value' |jq -c '[ .[] | select( .name == "eastus")]' | jq
```
