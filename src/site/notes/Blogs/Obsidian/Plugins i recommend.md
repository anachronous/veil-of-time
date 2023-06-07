---
{"dg-publish":true,"permalink":"/blogs/obsidian/plugins-i-recommend/"}
---


# Dataview
**Link:** https://github.com/blacksmithgu/obsidian-dataview

Allows you to use your Vault similarly to a Database. If you use the minimal theme, you can even use it to display stuff as really good looking cards. On this site, i use it for the aggregating pages like [[Books\|Books]] or [[Music\|Music]]. The result ends up looking like this:

| Title                                                                     | Genre     | Rating | Description                                                                                             | Link                                              |
| ------------------------------------------------------------------------- | --------- | ------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| [[Reviews/Music/Alcest - Écailles de lune\|Alcest - Écailles de lune]] | Blackgaze | 4.5/5  | Very atmospheric and aquatic themed album that manages to be both heavy and beautiful at the same time. | https://alcest.bandcamp.com/album/cailles-de-lune |

{ .block-language-dataview}
On the page [[Reviews/Music/Alcest - Écailles de lune\|Alcest - Écailles de lune]], i put this metadata at the top of the note (ignore dg-publish):
```
---
dg-publish: true
Genre: Post Black Metal
Rating: 4.5/5
Description: Very atmospheric and aquatic themed album that manages to be both heavy and beautiful at the same time.
Link: https://alcest.bandcamp.com/album/cailles-de-lune
---
```

While usually not visible, the different fields end up getting picked up by dataview queries you can simply put into your text like this (though you need to put it into a codeblock and write dataview where you would usually put the programming language used):
```
table without id 
	file.link as Title,
	Genre as Genre,
	Rating as Rating,
	Description as Description,
	Link as Link
from "Reviews/Music"
```

Now obviously, you can go much deeper than this and i heavily encourage you to experiment with this.

# Obsidian Git
**Link:** https://github.com/denolehov/obsidian-git

Well this one should explain itself. Instead of having to pay for obsidian sync (which at the time of writing costs 8 bucks a month if you pay yearly and 10 bucks otherwise) you can use this plugin to very easily sync your vault with websites such as github or gitlab. Obviously you can use this for collaboration too, but you'll almost definitely run into merge conflicts which can get annoying. You'll have to put some stuff into .gitignore for that.
Caveat is that this will completely flood your account with commits which you'll have to keep in mind if you care about your green squares on github.

# Obsidian Tasks
**Link:** https://github.com/obsidian-tasks-group/obsidian-tasks

This one is similar to the Dataview plugin mentioned above but instead for tasks (well obviously). It lets you query tasks in a similar way from all over your vault and is really helpful if you're a messy person like me. The plugin also lets you set due times, repeating tasks and more.

A query for that will look a bit like this:
```
not done
due today
group by priority
```

Again, you'll have to put this into a codeblock and put tasks at the top instead of a programming language. Also obviously again, you can go much deeper than this.

