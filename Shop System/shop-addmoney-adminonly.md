
{
  "name": "AddMoney",
  "permissions": "ADMINISTRATOR",
  "restriction": "1",
  "_id": "iXaFc",
  "actions": [
    {
      "member": "0",
      "varName": "",
      "dataName": "money",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "currentBalance",
      "name": "Store Member Data"
    },
    {
      "storage": "0",
      "varName": "",
      "name": "Delete Message"
    },
    {
      "info": "0",
      "infoIndex": "2",
      "storage": "1",
      "varName": "addAmount",
      "name": "Store Command Params"
    },
    {
      "into": "0",
      "vAria": "${tempVars(\"addAmount\")}",
      "storage": "1",
      "varName2": "addConvertedIntAmount",
      "name": "Convert a Variable"
    },
    {
      "condition": "0",
      "comparison": "1",
      "value": "1",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "10",
      "name": "Check Parameters"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "You need to mention a user and the amount of money to add",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "time": "20",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "name": "End Action Sequence"
    },
    {
      "member": "0",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "tempVars(\"addConvertedIntAmount\")",
      "name": "Control Member Data"
    },
    {
      "member": "0",
      "varName": "",
      "dataName": "money",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "currentBalance",
      "name": "Store Member Data"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "You have added ${tempVars(\"addConvertedIntAmount\")} to the user ${mentionedUser} gem account.\n\nCurrent Balance: ${tempVars(\"currentBalance\")}",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "time": "20",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "name": "End Action Sequence"
    }
  ]
}
