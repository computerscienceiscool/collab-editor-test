Name: mcp-450-cswg-workshop-collaborative-editor-progress
Title: Collaborative Editor Progress
Status: Draft -- anyone can edit. 

See the MCP index to create or find documents, or mcp-0-readme for an overview.  
The headers above are machine-readable; please preserve format.



Text checkins

Steve
progress in promisebase refactoring
 Donaldo
I'm recovering this week, did some catchup, getting back into projects
Rebecca
Returned from trip less than 24 hours ago, still a little tired. Re-adapting to elevation and dry air
Maker Faire was the highlight of the trip
Led a Zoom meeting at the makerspace remotely, there were 1-2 other people attending remotely, and 4 people with major roles in the meeting,  plus a few other people who had some things to say here and there, attending in person. I feel like this is a very challenging situation with a mixed meeting format, especially when leading the meeting. This was an interesting experience. We had a laptop with the main participants on the screen, one of the other people attending who had some input into a major topic, and then the laptop was rotated to show some others who had some input. I don't know entirely how this got arranged but I suspect it was as simple as informing the participants that if they wanted to be on camera they should sit in a certain area. 
Lots of challenging situations to deal with on the trip but I feel like it was very productive,, I will probably need to travel again soon to get the project done. Dates still being finalized for the project completion.
JJ
Learning more about GEO.  This is pretty exciting
Wrote a tool to scrape all web data , then used claude.ai to add tags and meta description.  I have to manually add to site.
Updating site with meta descriptions and new tags.  Google search has been flakey for me, so also trying to update things with MIcrosoft… this has been great
I have free advertising for my site on wordpress… most of the traffic is at 1, 3, and 5 am… i am guessing because it is free.  :\
Wrote a kindle app… pretty cool.  Lots of red tape to get on the app store… This was intended to be a kindle app and I used dart and flutter





Plan lineup for following weeks

Go to workshop schedule & proposals (mcp-369)

Collaborative Editor Progress 

Storage issues on VM; quick fix increased the storage from 70 gb to 100 gb

Collab Editor Demo
Code Repository: https://github.com/computerscienceiscool/collab-editor 
Test Editor Files: https://github.com/computerscienceiscool/collab-editor-test

Rooms are stored in the browser's IndexDB under same name as the URL
IndexDB has access to use about half of available memory
'Pull from Github' window
A bit slow, unsure if its a computer specific issue 
Keyboard shortcuts based on GDocs keybindings; ability to customize but opens a can of worms to avoid conflicts with system keybindings
Github Settings
You enter your Github personal access token
Playwright is a tool to test applications for multiple users
https://playwright.dev/
Multi User Demo
Steve follows the installation.md & building the WASM binary on his machine



Ideas/TODOs:
listener for keystrokes in left pane to update markdown view: done
have user opt into keyboard shortcuts (off by default): DONE (COPY, PASTE AND CUT WORK,BUT THAT IS IT)
Welcome screen with the shortcuts toggle on/off? Keyboard shortcuts are very helpful, unsure if average user will know to toggle them on later : THIS IS IN THE KEYBOARD SHORTCUTS MENU ITEM
have grokker's commit code generate default commit message 
allow user to edit message before commit
Another option that was mentioned about the commit message was that it could say "1st commit since "<prev commit message>" -- would want to increment rather than having a growing list of recursive messages
fix line number toggle
installation.md file: 
Add version numbers on Rust and WASM pack: added
Add make build :added
Perhaps add it to Quickstart Guide as well. Also, move quickstart guide to top and then if people have problems list things out…. :added
Steve/JJ set up containerization and deploy to europa
give everyone the URL
Steve/JJ/everyone work out:
PromiseGrid messages between browsers to sync IndexedDb (POC)
Refactor to use PromiseBase code with IndexedDb as kv store (POC)
Remove Yjs (replace with PromiseGrid messaging)
Commit/pull from PG VCS
References:
https://github.com/stevegt/promisebase/blob/main/x/layers.md 
https://github.com/stevegt/promisebase/blob/main/x/layers.dot 


What can we build now that won't feel 'useless' later
Proof of concept, but less as throwaway code, and more as stepping stones
We're struggling with a deploying stuff issue
Chicken & egg problem, we're trying to build the thing that would make it easier
JJ editor, workadventure, storm tool
Donaldo: maybe system initiative could help in the interim?
Possibly worth learning what they're up to
Funny, now they've drank the AI marketing; "The AI Native Infrastructure Automation Platform - System Initiative is the best way to automate infrastructure with AI."
https://www.systeminit.com/
Kelsey Hightower recent post on BlueSky
https://bsky.app/profile/kelseyhightower.com/post/3m2r23k6xkc2i 
Adam Jacob's response (note that this is a different person than the UC Davis math prof by the same name)
https://bsky.app/profile/adamhjk.me/post/3m2rdytysl22o 
Steve: Unlikely worth the time integrating SysInt, takes time to learn a tool
Avoiding third party tooling forces us to build the stuff we need to build anyway (without creating a dependency on a third party tool that has its own priorities)
Angela heartbot demo
Spins up a Docker container
It only takes a couple files - doesn't need complex tooling
More complex situations (example workadventure), still doable 
brief plan9 analogy with promisegrid
plan9 is bare metal
spun off inferno
rob pike
promisegrid is like plan9 but 2nd level (so users don't have to install a new OS)
