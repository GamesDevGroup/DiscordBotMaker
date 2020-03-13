
{
  "name": "myBackpack",
  "permissions": "NONE",
  "restriction": "1",
  "_id": "iWANd",
  "actions": [
    {
      "storage": "0",
      "varName": "",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "backpackItems",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackItemsCount",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "defaultVal": "200",
      "storage": "1",
      "varName2": "currentBalance",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon1",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "weapon1Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon2",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "weapon2Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon3",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "weapon3Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon4",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "weapon4Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon5",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "weapon5Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus1",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "bonus1Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus2",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "bonus2Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus3",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "bonus3Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus4",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "bonus4Count",
      "name": "Store Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus5",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "bonus5Count",
      "name": "Store Member Data"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "-----------------\n**Your Backpack**\n-----------------\n**Current Balance:**\n${tempVars(\"currentBalance\")}\nYour backpack currently has the following items:\n----------\nWEAPONS\n----------\n``` \n| ${tempVars(\"weapon1Count\")} |- Weapon 1\n| ${tempVars(\"weapon2Count\")} |- Weapon 2\n| ${tempVars(\"weapon3Count\")} |- Weapon 3\n| ${tempVars(\"weapon4Count\")} |- Weapon 4\n| ${tempVars(\"weapon5Count\")} |- Weapon 5\n```\n--------------\nBONUS Items\n--------------\n```| ${tempVars(\"bonus1Count\")} |- Bonus 1\n| ${tempVars(\"bonus2Count\")} |- Bonus 2\n| ${tempVars(\"bonus3Count\")} |- Bonus 3\n| ${tempVars(\"bonus4Count\")} |- Bonus 4\n| ${tempVars(\"bonus5Count\")} |- Bonus 5```\n",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "time": "2",
      "measurement": "2",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    }
  ]
}
