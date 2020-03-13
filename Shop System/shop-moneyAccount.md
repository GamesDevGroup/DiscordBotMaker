{
  "name": "money",
  "permissions": "NONE",
  "restriction": "1",
  "_id": "GUcjO",
  "actions": [
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "defaultVal": "200",
      "storage": "1",
      "varName2": "money-balance",
      "name": "Store Member Data"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "** ********************\nAccount Balance: ${tempVars(\"money-balance\")}\n** ********************\nThis message will disappear after 10 seconds.",
      "storage": "1",
      "varName2": "DelThisMsg",
      "name": "Send Message"
    },
    {
      "time": "10",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "DelThisMsg",
      "name": "Delete Message"
    }
  ]
}