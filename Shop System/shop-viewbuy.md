{
  "name": "shop",
  "permissions": "NONE",
  "restriction": "1",
  "_id": "xJZUG",
  "actions": [
    {
      "storage": "0",
      "varName": "",
      "name": "Delete Message"
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
      "info": "1",
      "storage": "1",
      "varName2": "memberID",
      "name": "Store Member Info"
    },
    {
      "condition": "0",
      "comparison": "1",
      "value": "2",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "13",
      "name": "Check Parameters"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "This is the quick help area, shown when less than 3 parameters used.\n\nparameter is:\n\n**view - to see store category (weapons,bonus)\n buy - to buy an item from selected category (weapons,bonus)\n\n!shop [shop Option] [shop Category] [Category item #]**\n\n   i.e. !shop view weapons\n         !shop buy weapons 1**",
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
      "channel": "0",
      "varName": "",
      "message": "**There is no Category or item found by that name or item #**\nShop Options: View, Buy\nShop Category: Weapon, Bonus\n\ni.e: !shop view weapons\n     !shop buy weapons 1",
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
      "info": "0",
      "infoIndex": "1",
      "storage": "1",
      "varName": "shopOptionSelected",
      "name": "Store Command Params"
    },
    {
      "info": "0",
      "infoIndex": "2",
      "storage": "1",
      "varName": "shopCategorySelected",
      "name": "Store Command Params"
    },
    {
      "info": "0",
      "infoIndex": "3",
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "name": "Store Command Params"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"view\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "50",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"weapons\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "31",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopViewWeapons",
      "name": "Create List"
    },
    {
      "storage": "1",
      "varName": "shopViewWeapons",
      "addType": "0",
      "position": "",
      "value": "\"[1] Weapon 1: 100 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "storage": "1",
      "varName": "shopViewWeapons",
      "addType": "0",
      "position": "",
      "value": "\"[2] Weapon 2: 200 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "storage": "1",
      "varName": "shopViewWeapons",
      "addType": "0",
      "position": "",
      "value": "\"[3] Weapon 3: 300 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "storage": "1",
      "varName": "shopViewWeapons",
      "addType": "0",
      "position": "",
      "value": "\"[4] Weapon 4: 400 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "storage": "1",
      "varName": "shopViewWeapons",
      "addType": "0",
      "position": "",
      "value": "\"[5] Weapon 5: 500 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "list": "7",
      "varName": "shopViewWeapons",
      "start": "🌠",
      "middle": "",
      "end": "\\n",
      "storage": "1",
      "varName2": "viewWeapons",
      "name": "Convert List to Text"
    },
    {
      "title": "${server} Weapon Shop : Current Balance: ${tempVars(\"currentBalance\")} :gem:s",
      "author": "",
      "color": "GREEN",
      "timestamp": "false",
      "url": "",
      "authorIcon": "",
      "imageUrl": "",
      "thumbUrl": "",
      "storage": "1",
      "varName": "viewWeaponsEmbed",
      "name": "Create Embed Message"
    },
    {
      "storage": "1",
      "varName": "viewWeaponsEmbed",
      "message": "${tempVars(\"viewWeapons\")}",
      "name": "Set Embed Description"
    },
    {
      "storage": "1",
      "varName": "viewWeaponsEmbed",
      "channel": "0",
      "varName2": "",
      "name": "Send Embed Message"
    },
    {
      "time": "45",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "viewWeaponsEmbed",
      "name": "Delete Message"
    },
    {
      "name": "End Action Sequence"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"bonus\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopViewBonus",
      "name": "Create List"
    },
    {
      "storage": "1",
      "varName": "shopViewBonus",
      "addType": "0",
      "position": "",
      "value": "\"[1] Bonus Item 1: 100 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "storage": "1",
      "varName": "shopViewBonus",
      "addType": "0",
      "position": "",
      "value": "\"[2] Bonus Item 2: 200 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "storage": "1",
      "varName": "shopViewBonus",
      "addType": "0",
      "position": "",
      "value": "\"[3] Bonus Item 3: 300 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "storage": "1",
      "varName": "shopViewBonus",
      "addType": "0",
      "position": "",
      "value": "\"[4] Bonus Item 4: 400 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "storage": "1",
      "varName": "shopViewBonus",
      "addType": "0",
      "position": "",
      "value": "\"[5] Bonus Item 5: 500 :gem:\"",
      "name": "Add Item to List"
    },
    {
      "list": "7",
      "varName": "shopViewBonus",
      "start": "✨",
      "middle": "",
      "end": "\\n",
      "storage": "1",
      "varName2": "viewBonus",
      "name": "Convert List to Text"
    },
    {
      "title": "${server} Bonus Shop : Current Balance: ${tempVars(\"currentBalance\")} :gem:s",
      "author": "",
      "color": "GREEN",
      "timestamp": "false",
      "url": "",
      "authorIcon": "",
      "imageUrl": "",
      "thumbUrl": "",
      "storage": "1",
      "varName": "viewBonusEmbed",
      "name": "Create Embed Message"
    },
    {
      "storage": "1",
      "varName": "viewBonusEmbed",
      "message": "${tempVars(\"viewBonus\")}",
      "name": "Set Embed Description"
    },
    {
      "storage": "1",
      "varName": "viewBonusEmbed",
      "channel": "0",
      "varName2": "",
      "name": "Send Embed Message"
    },
    {
      "time": "45",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "\"viewBonusEmbed\"",
      "name": "Delete Message"
    },
    {
      "name": "End Action Sequence"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "You do not have enough Gems:gem: to complete the purchase.",
      "storage": "1",
      "varName2": "delThisMessage",
      "name": "Send Message"
    },
    {
      "time": "20",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "\"viewBonusEmbed\"",
      "name": "Delete Message"
    },
    {
      "name": "End Action Sequence"
    },
    {
      "comment": "buy item sequences - Buy Weapons Category - Item #1",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"weapons\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "134",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"1\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "70",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"weapons\", item 1 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "99",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-100",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon1",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon1",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackWeapon1",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Weapon 1\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackWeapon1\")} ",
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
      "channel": "0",
      "varName": "",
      "message": "The purchase has been cancelled",
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
      "comment": "buy item sequences - Buy Weapons Category - Item #2",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"weapons\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "134",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"2\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "86",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"weapons\", item 2 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "199",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-200",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon2",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon2",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackWeapon2",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Weapon 2\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackWeapon2\")} ",
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
      "comment": "buy item sequences - Buy Weapons Category - Item #3",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"weapons\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "134",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"3\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "102",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"weapons\", item 3 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "299",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-300",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon3",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon3",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackWeapon3",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Weapon 3\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackWeapon3\")} ",
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
      "comment": "buy item sequences - Buy Weapons Category - Item #4",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"weapons\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "134",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"4\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "118",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"weapons\", item 4 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "399",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-400",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon4",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon4",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackWeapon4",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Weapon 4\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackWeapon4\")} ",
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
      "comment": "buy item sequences - Buy Weapons Category - Item #5",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"weapons\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "134",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"5\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"weapons\", item 5 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "499",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-500",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon5",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "weapon5",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackWeapon5",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Weapon 5\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackWeapon5\")} ",
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
      "comment": "buy item sequences - Buy Bonus Category - Item #1",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"bonus\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"1\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "150",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"bonus\", item 1 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "99",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-100",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus1",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus1",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackBonus1",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Bonus 1\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackBonus1\")} ",
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
      "comment": "buy item sequences - Buy Bonus Category - Item #2",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"bonus\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"2\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "166",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"bonus\", item 2 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "199",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-200",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus2",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus2",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackBonus2",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Bonus 2\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackBonus2\")} ",
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
      "comment": "buy item sequences - Buy Bonus Category - Item #3",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"bonus\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"3\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "182",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"bonus\", item 3 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "299",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-300",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus3",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus3",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackBonus3",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Bonus 3\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackBonus3\")} ",
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
      "comment": "buy item sequences - Buy Bonus Category - Item #4",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"bonus\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"4\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "198",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"bonus\", item 4 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "399",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-400",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus4",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus4",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackBonus4",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Bonus 4\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackBonus4\")} ",
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
      "comment": "buy item sequences - Buy Bonus Category - Item #5",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "1",
      "varName": "shopOptionSelected",
      "comparison": "1",
      "value": "\"buy\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategorySelected",
      "comparison": "1",
      "value": "\"bonus\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "storage": "1",
      "varName": "shopCategoryItemSelected",
      "comparison": "1",
      "value": "\"5\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "9",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "this is buy category \"bonus\", item 5 stuff\n\nType yes to accept purchase, to cancel do not respond.",
      "storage": "1",
      "varName2": "delThisMsg",
      "name": "Send Message"
    },
    {
      "storage": "0",
      "varName": "",
      "filter": "content==('yes') && ${tempVars(\"memberID\")}",
      "max": "1",
      "time": "15000",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "65",
      "storage2": "0",
      "varName2": "delThisMsgList",
      "name": "Await Response Call Action"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "comparison": "4",
      "value": "499",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "2",
      "iffalseVal": "45",
      "name": "Check Member Data"
    },
    {
      "storage": "1",
      "varName": "delThisMsg",
      "name": "Delete Message"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "money",
      "changeType": "1",
      "value": "-500",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus5",
      "changeType": "1",
      "value": "1",
      "name": "Control Member Data"
    },
    {
      "member": "1",
      "varName": "",
      "dataName": "bonus5",
      "defaultVal": "0",
      "storage": "1",
      "varName2": "backpackBonus5",
      "name": "Store Member Data"
    },
    {
      "member": "1",
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
      "message": "You have purchased Bonus 5\n\nCurrent Balance: ${tempVars(\"currentBalance\")}\n\nItem in Backpack ${tempVars(\"shopCategorySelected\")} ${tempVars(\"shopCategoryItemSelected\")}:${tempVars(\"backpackBonus5\")} ",
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