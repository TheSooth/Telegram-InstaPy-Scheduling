# Telegram-InstaPy-Scheduling v2!
Telegram-InstaPy-Scheduling is bot for telegram which helps user to schedule [*InstaPy*](https://github.com/timgrossmann/InstaPy).

### What's news?
- Run multiple script simultaneous.
- Configure your scripts in easy way!
- Create users list.

### What do you need
- This repo and all _requirements.txt_ installed.
- InstaPy working on your pc/server.
- Telegram bot token.

### How to setup
1. Clone this repo in your InstaPy folder.
2. Create a bot with [@BotFather](https://telegram.me/BotFather).
3. Rename *settings.json.dist* => *settings.json*.
4. Contact [@GiveChatId_Bot](https://telegram.me/GiveChatId_Bot) and get your chat id with */chatid* command
5. Populate *settings.json* with your data. 
```
{
    "telegram_token": "xxxx",
    "allowed_id": [ "chat_id from GiveChatId_Bot", "342342" ]
}
 ```
6. Write your personal scripts:
#### How? 
- Edit *scripts.py*
- Create a function with name as you preferred and put inside an InstaPy script, for example:
```python
def script_for_big_like(username, password, proxy):
    session = instapy.InstaPy(username=username, password=password)
    then put your instapy script.
```
- Save and exit.
9. Launch *main.py*.

### Avaiable commands
#### Users management
| Command      | Parameters                                    | Description           |
|--------------|-----------------------------------------------|-----------------------|
| /add_user    | \<username\> \<password\> \<proxy:optional\>  | Save new user.        |
| /delete_user | \<username\>                                  | Delete an user.       |
| /users       |                                               | Print all users saved |

#### Jobs management
| Command  | Parameters                                             | Description                                      |
|----------|--------------------------------------------------------|--------------------------------------------------|
| /set     | \<username\> \<job_name\> \<script_name\> \<hh:mm:ss\> | Create a new schedule. Select the day from bot.  |
| /unset   | \<job_name\>                                           | Delete a schedule.                               |
| /jobs    |                                                        | Print all setted jobs                            |
| /scripts |                                                        | Print all your scripts                           |
| /status  | \<job_name:optional\>                                  | Print the status of all your thread or single.   |
| /now     | \<username\> \<script_name\>                           | Run immediately.                                 |

