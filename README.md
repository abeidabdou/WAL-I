# WAL-I
**WAL-I is a friendly Discord bot powered by AI and the Discord API, designed to assist you and your moderators by understanding and responding to commands in plain, everyday language**

> Welcome to the shortest documentation you'll ever read!

> Before Starting you should watch the video to understand more of what you will be reading 

**What can Wal-i do now?**

## Commands

Since wali doesn't use any command to perform actions but natural language, we will go by examples

### 1. Wal-i can delete messages written by a specific user, containing specific keywords, including links, or targeting a specific attachment. Wal-i can also delete messages by intervals, whether these intervals are based on date and time or message IDs. Additionally, he can delete messages by channels or simply by their IDs.

#### 1.2 Deleting messages by id

> "message: Delete this message to ensure privacy. 32109876"

> "message: wal-i this message needs to be removed, 23424234, 32109876, user doesn't respect the rules",

#### 1.2 Deleting messages by channels

> "message: delete the last 30 messages in test",

> "message: delete the last 20 messages" (Notice here I am not specying any channel, which means Wal-i will assume that the channel is where the request is being made)

> "message: delete the last 20 messages sent here"

> "message: delete the last 50 messages in all channels", (The possiblity of deleting messages in all channels is only available to the server owner)

#### 1.3 Deleting messages by intervalles

> "message: Delete the 10 messages sent before 23423424532 in test" (This will delete the 10 messages sent just before that message ID)

> "message: delete the last 10 messages sent after 2375672242." (This will delete the 10 messages sent just after that message ID)

> "message: delete the messages sent after 2375672242 and before 23423424532 in channel test."

> "input: delete the messages sent betwen 2375672242 23423424532 in channel test." (Notice here and didn't have to specify Wal-i will always know which one is the before and which is the after message ID)

#### 1.4 Deleting messages with attachements

> "message: delete all messages with link"

> "message: delete any message with an image in channel test"

#### 1.5 Deleting messages with a specifique word or keyword

> "message: Delete any message containing this emoji 🫡"

#### 1.6 Deleting messages by users

> "message: delete the last 10 messages ali sent" (We already established that if no channel is provided the channel where the command is being invoked is used)

> "message: delete the last 10 messages ali sent in test" (Notice here I didn't have to specify that test is a channel)

> "message: delete the last 10 messages I sent in channel test."

> "message: delete the last 10 messages I sent in all channels" (This is only available to the server owner, still don't know why you would need it)

> "message: Delete the 20 messages ali sent before 23423424532 in channel test" (This will delete the next 10 message the member ali sent after that message ID)

> "message: delete messages sent by ali after 23453534536 and before 23423424532"

> "message: delete messages with stp in channel test sent by ali before this message 23453534536" (This will delete any message the member ali before that message ID containing the word "stp")

And all of that can be combined

This can work:

> "message: Delete messages sent by ali and sam containing trip"

As this can also work

> "message: delete messages sent between 2am and 5pm" (You just need to know that Wal-i uses the international timezone since the discord API doesn't provide any way of getting the user timezone)

You can combine all of that you just need to be specific in your request:

**Here's some few things to keep in mind when deleting messages**

> Specificity is key

> Only a server owner can delete messages in all channels at the same time

> If you are not a server owner and you didn't provide a limit when deleting a message the default limit will be 5

> When deleting messages with before and after you don't need any limit

> When before and after are date time and if you are a server owner you can delete messages in all channels at the same time

> Moderators cannot delete messages using date and time

> Notice that none of the examples give a reason when deleting messages but you will always need one

**Wal-i gives you targeted message deletion capabilities, you just need to remember specificity is key. And if he can't do something he will just tell you**

### 2. Wal-i can also ban, kick, timeout, mute and unmute one or multiple users

Just remember specifity is key

This can work:

> "message: wal-i ban amy"

As this can also work:

> "message: wali ban amy, samy and ali"

### 3. Wal-i can give roles permissions in a channel (Available only to server owners)

> "message: wal-i let everyone send messages in test" (This will give @everyone the permission to send messages in channel test)


**There are more command capabilities to come, you can also suggest yours**

## Modules

For the time being wal-i only modules is a module that gives your mods access to deleting messages, banning, kicking, timimg out and muting without them having any permissions.
To just invoke the command wali create mod, and the command will ask you who you want to make a mod, the messages he number of bans he can have, kicks, timeouts, and the number of messages he delete. Then a role wali mod will be assigned to him that will let him uses the command that invoke Wal-i. You can reset the numbers he used to 0 or adjust his limits. Know that if you assign anyone the mod role he will be able to delete messages in any channel he is member. The moment you decide that you want to remove that mode you can just remove the role wali mod from him or delete the message showing his stats

**More modules are going to be added**

**Just a disclaimer**

Wal-i doesn't store any mod stats in a database which means if you delete the message conataining a mod stats, that data will be lost forever.
The only data wal-i keep is when you are making requests so it can have context, and that's kept for 5 minutes after the last request made.

I know that I didn't do a good a Job of explaining so if you have more questions there's a link to a discord server down below.

## Subscribe and add Wal-i to your server

The Subscribtion fee is 5$
