# G+ Unsender

A userscript that clears out a Messenger conversation for you. It unsends your own messages, removes the "You unsent a message" leftovers, and can also remove other people's messages from your side. It runs in the browser on messenger.com and facebook.com/messages.

Version 1.0
<img width="492" height="480" alt="Screen Recording 2026-10-21 065637 (online-video-cutter com)" src="https://github.com/user-attachments/assets/21734ff0-e55a-4e76-8080-c4ef2785ed40" />


## Install

1. Install a userscript manager such as Tampermonkey or Violentmonkey.
2. Create a new script, paste in the contents of `gplus-unsender.user.js`, and save.
3. Open Messenger. A **G+** button shows up in the chat header, next to the call buttons.

## Use

1. Open the chat you want to clean.
2. Hover or click the **G+** button to open the panel.
3. Pick your options, then press **Start**.

It starts from the newest messages and works its way up. When it can't load anything older, it stops on its own and shows how many messages it handled. You can press **Pause** and **Resume** whenever you want, or **Stop** to end the run.

## Options

- **Unsend my messages**: unsends your messages for everyone.
- **Remove unsent notices**: deletes the "You unsent a message" placeholders left behind (also the ones from other people).
- **Remove their messages**: removes other people's messages. This only removes them on your side, they still have them.

All three are on by default. Turn off whatever you don't want touched before you press Start.

There is also a theme switch (Auto, Light, Dark). The G+ button copies the color of the conversation information icon, so it matches your chat theme.

## What the panel shows

The top line is the status (Working, Looking for older messages, Finished, and so on) with a running count. The line under it shows the message it is on, like `Unsending · 10/21/2026`, and `Unsend completed · 10/21/2026` once it's done. The date is the day the message was sent. If the script can't work it out, it just leaves the date off.

## Safety

- It only works on the chat that was open when you pressed Start. If you switch to another chat, it stops.
- It never clicks anything about deleting a chat, leaving a group, archiving, blocking or muting. If a dialog looks like one of those, it cancels.
- Unsending can't be undone. Try it on a throwaway chat first if you haven't used it before.

## Troubleshooting

- **The G+ button doesn't show up**: reload the page and make sure a chat is open. The script looks for the call buttons in the header to place itself.
- **It stops early or skips messages**: Messenger changes its page layout now and then, which can break the script. Open the browser console (F12) and look for lines starting with `[G+ Unsender]`. They show what it saw for the first few messages.
- **A message keeps being skipped**: it tries each message twice and then moves on. Usually that's a message type Messenger doesn't allow you to remove.

## Notes

This is an unofficial script and has nothing to do with Meta. It works by clicking through Messenger's own menus, so it may need fixing whenever Messenger changes. Use it on your own account and at your own risk.
