# WAL-I
**WAL-I is a friendly Discord bot powered by AI and the Discord API, designed to assist you and your moderators by understanding and responding to commands in plain, everyday language**

Welcome to the shortest documentation you'll ever read!

1. Commands
1.1 Deleting Messages
WAL-I can delete one or multiple messages using their IDs, but that’s just the beginning. Let’s dive into the details:

1.1.1 By Users
WAL-I can delete messages sent by a specific user or multiple users. Simply provide the usernames, a limit, and a reason. If a channel isn’t specified, WAL-I assumes the current channel.

Example:
“Could you delete the last 30 messages sent by Sam? He has been disturbing others.”

This command will result in WAL-I deleting Sam’s last 30 messages in the current channel.

1.1.2 With Before and/or After
If you return to your server and find an unwanted discussion, you can delete messages within a specific range using message IDs.

Example:
“WAL-I, could you delete all messages sent between [message ID] and [message ID], [reason].”

You can also specify users:
“WAL-I, delete all messages sent by [user1, user2, etc.] between [message ID] and [message ID], [reason].”

For date and time:
“WAL-I, delete any message sent between 2 am and 5 pm, [reason].”

Keep in mind, WAL-I uses the international timezone.

1.1.3 Messages Containing a Specific Word
To delete messages containing a specific word, provide the word and, optionally, the user’s messages you want to target. This can be combined with a limit or a time range.

1.1.4 Messages with Attachments
WAL-I can delete messages with attachments. Specify the type of attachment (images, documents, etc.), and you can pair this with other criteria like user, limit, or time range.

1.2 Editing Members
WAL-I can manage members with commands such as Ban, Kick, Timeout, Mute, Unmute, MuteSoundboard, and UnmuteSoundboard. You can target one or multiple members and even delete their messages if needed.

Additionally, WAL-I can assign or remove roles and manage role permissions in channels.

2. Modules
Currently, WAL-I has one module: ModManager. This module empowers moderators to perform their duties without the risk of abuse.

ModManager Features
Create a Moderator: Assign a moderator and set limits on the number of bans, kicks, timeouts, and message deletions they can perform.
Limit Reset: Reset or adjust the limits as needed.
Note: Moderators without permissions cannot exceed their limits, ensuring controlled moderation.

Data Privacy
WAL-I only retains data temporarily (for about 5 minutes) to provide context for ongoing requests. After this period, all data is deleted. Your privacy is a priority.

Why Choose WAL-I?
WAL-I simplifies command execution without cluttering your server with numerous commands. It equips your moderators with essential tools while maintaining control to prevent abuse.

What’s Next?
We have plans to introduce new commands and modules, such as password-protected areas and multi-choice question games. Your feedback and suggestions are invaluable.

Do you have ideas for WAL-I? If you can dream it, we might be able to code it. This is just version 0.1, and more features are on the way. If you like the concept and potential, consider subscribing!
