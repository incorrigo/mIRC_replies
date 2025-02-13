# Message Reply Script for mIRC
### This script adds the message replies feature to channel and query windows in mIRC  
Protocol specification published by IRC v3 e.g. - [specification link](https://ircv3.net/specs/client-tags/reply)

* Client message tag +draft/reply  
Most IRC clients which support this feature use the "draft/" prefix, because currently the reply feature protocol is in the draft phase

* Client message tag +reply  
This script supports the feature _without_ the draft prefix, **(a)** multiple clients support this feature successfully already **(b)** IRCd software has included this already in their source code ready to go

* Chat history playback utilised  
On joining a channel that uses chat history playback, you can reply to messages that were sent prior to joining the channel, and this function is used to reinforce the @reply menu's chronological relevance  

* Adds message reply feature to private conversations  
This script enables message replies in query windows, so you can exchange replies in private messages

* Fully compatible with other IRC clients  
Written on mIRC 7.78, tested on mIRC 7.79, compatible with all clients - regardless whether +draft/reply or +reply is used. Actually, you can even use both! No upgrade is needed and it doesn't need an upgrade any time any of the other users' IRC client developer decides that they want to drop the draft prefix

* Classic mIRC script, no DLL files or external software  
This feature is made using a good old fashioned remote script file, the functionality that enables the message replies has been supported and well documented by mIRC for decades / doesn't require any libraries, client upgrades, or configuration changes

* Protocol specification for inclusion of own messages  
The specification is very particular about how you are able to send replies to the query / channel about your own messages. This has been followed exactly so the way this script works is made in the spirit of the specification

* Messages containing both tags (with and without draft/) are handled accordingly  
If both tags are used legitimately then the value should be identical. Nonetheless, messages utilising both versions of the reply tag are dealt with accordingly - giving your mIRC script's message replies full compatibility

* Functional data structure starts fresh every session, and stays tidy when you're done  
Automatically created functional data structure, which is created in _incorrigo-syx_ directory, starts from fresh when you log in ... and tidies up when you're done with mIRC. Naturally this makes the reply system more optimised for the interests of your privacy, i.e. private conversations aren't left lying around in your filesystem  

* Timeliness of functional session data structure is designed to support long sessions  
If your IRC session continues for a particularly long time, the reply system's functional data structure is designed to maintain consistency. Once the data for a conversation reaches a certain size, the oldest info you are least likely to use will start being trimmed and replaced with new as the conversation goes along; keeping a chronological snapshot consisting of only what is realistically going to be used and stays in the context of a cache instead of turning into a redundant log file  

* Data is cached on file system  
Large data cache can still result from lots of conversations in one session. The functional data structure is maintained on the file system instead of system memory ... so reply support persists even when your buffer is cleared, and data is stored / retrieved from a file on disk rather than device memory

* You can send and receive message replies  
This feature isn't just so that you can send replies. You can receive replies as well from other users - using _any_ IRC client - message replies will also be displayed if a reply is present in chat history playback

If you like this script which has been adapted into a stand-alone version so that it can be used by other people in their own mIRC scripts, you might be interested in _Incorrigo Syx Script_ ... which is the main script this comes from. It is a fully featured mIRC script that's **bespoke** to my IRC network _irc.incorrigo.io_ ... here's the permanent link to the repository: [https://incorrigo.io/script](https://incorrigo.io/script)  

Channel conversations, private query, and **action** messages are all supported by this script, which adds message replies feature to mIRC. If you are going to use this in another fully featured script, please be so kind as to leave me some credit in there so when people look back they will know that awesomeness existed within us before someone decided to make it built-in. Thank you  
