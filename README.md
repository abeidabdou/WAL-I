# WAL-I
![WAL-I](https://github.com/abeidabdou/WAL-I/blob/fd2be38b24b161884e3adb205112836f950f624d/DrawKit%20Vector%20Illustration%20Animal%20%26%20Pets%20(21).png)
**WAL-I is a friendly Discord bot powered by AI and the Discord API, designed to assist you and your moderators by understanding and responding to commands in plain, everyday language.**

> Welcome to the shortest documentation you'll ever read!  
> Before starting, watch the video if you didn't watch it before to understand more about what you will be reading.

## What Can WAL-I Do?

### Commands

Since WAL-I doesn't use any specific command to perform actions but relies on natural language, we will go through examples.

#### 1. Deleting Messages

WAL-I can delete messages based on various criteria: by user, keywords, links, attachments, time intervals, and message IDs. Deletion can also be scoped to specific channels or all channels for server owners.

**1.1 Deleting Messages by ID:**

```diff
- "Delete this message to ensure privacy. 32109876"
- "WAL-I, this message needs to be removed, 23424234, 32109876, user doesn't respect the rules"
```

**1.2 Deleting Messages by Channel:**

```diff
- "delete the last 30 messages in test"
- "delete the last 20 messages"
```
_(WAL-I assumes the current channel if none is specified)_

```diff
- "delete the last 20 messages sent here"
- "delete the last 50 messages in all channels" (Server owner only)
```

**1.3 Deleting Messages by Interval:**

```diff
- "Delete the 10 messages sent before 23423424532 in test"
- "delete the last 10 messages sent after 2375672242"
- "delete the messages sent after 2375672242 and before 23423424532 in channel test"
- "delete the messages sent between 2375672242 and 23423424532 in channel test"
(Notice in the last one I didn't have to specify which one is the before and which one is the after message ID)
```

**1.4 Deleting Messages with Attachments:**

```diff
- "delete all messages with link"
- "delete any message with an image in channel test"
```

**1.5 Deleting Messages with Specific Words or Keywords:**

```diff
- "Delete any message containing this emoji 🫡"
```

**1.6 Deleting Messages by Users:**

```diff
- "delete the last 10 messages Ali sent"
- "delete the last 10 messages Ali sent in test"
- "delete the last 10 messages I sent in channel test"
- "delete the last 10 messages I sent in all channels"
```
_(Server owner only)_

```diff
- "Delete the 20 messages Ali sent before 23423424532 in channel test"
- "delete messages sent by Ali after 23453534536 and before 23423424532"
- "delete messages with stp in channel test sent by Ali before this message 23453534536"
```

**Combining Criteria:**

```diff
- "Delete messages sent by Ali and Sam containing trip"
- "delete messages sent between 2am and 5pm"
```
_(WAL-I uses the international timezone)_

WAL-I provides targeted message deletion capabilities with an emphasis on specificity. If it can't fulfill a request, it will notify you.

#### 2. Moderation Actions

WAL-I can ban, kick, timeout, mute, and unmute one or multiple users.

```diff
- "WAL-I ban Amy"
- "WAL-I ban Amy, Samy, and Ali"
```

#### 3. Role Permissions

WAL-I can assign role permissions in a channel (server owner only).

```diff
- "WAL-I let everyone send messages in test"
```
_(This grants @everyone the permission to send messages in channel test)_

**Important Notes:**

```diff
! Specificity is key.
! You can combine all the creterias listed here when making a request.
! Only a server owner can delete messages in all channels simultaneously.
! If no limit is provided, the default limit is 5 messages for everyone else and none for server owners.
! No limit is needed when using before and after criteria.
! Server owners can delete messages using date and time across all channels.
! Moderators cannot delete messages using date and time.
! A reason must be provided for all deletions, banning, timing out or kicking.
! When timimg out, if there's no specific time provided the limit will be 24h
! You when banning a member you can also delete the messages he sent in the server
```

### Modules

Currently, WAL-I offers a module that allows mods to delete messages, ban, kick, timeout, and mute without giving them those permissions. To create a mod:

1. Invoke the command: `WAL-I create mod`.
2. Specify the user, the number of bans, kicks, timeouts, and messages they can delete.
3. The user will be assigned a `WAL-I mod` role, granting them the ability to use WAL-I request command and do any mod work via Wal-i.
4. Adjust their limits or reset their stats as needed.

Removing a mod is as simple as removing the `WAL-I mod` role or deleting their stats message.

**Disclaimer:**

```diff
! WAL-I does not store mod stats in a database. Deleting the stats message will permanently remove the data.
! WAL-I retains request context for 5 minutes after the last request.
! One of the Goal is to make a bot that will never retain any of your data, so you your data will always live in your server
```

If you have more questions, ask in this [Discord server](#).

## Add WAL-I to Your Server by subscribing and help me add more to what Wal-i can do 

The subscription fee is $5.
