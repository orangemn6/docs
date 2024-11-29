---
title: "A Guide On Links vs. Tags In Obsidian - Knowledge management - Obsidian Forum"
source: "https://forum.obsidian.md/t/a-guide-on-links-vs-tags-in-obsidian/28231"
date: "2024-11-28T23:37:42-05:00"
tags:
  - "clippings"
---


The question “should I use tags or links” is asked regularly in the Obsidian discord.

The prevailing answer seems to be “Well, it depends on what you want to do” or “There’s no correct answer”. Of course, this being the community it is, those are usually followed by helpful people digging into the specifics of the situation. But also, sometimes, the questioner just disappears, and I find myself wondering if they’ve given up over what might well appear to be a non-answer.

Either way, it seems to me like it might be beneficial for us to have a standard response to this question, so I’ve tried to build one. However, I hope this document will continue to be updated (here or elsewhere) with the input of the whole community, so if I have missed relevant \[factual\] differences between links and tags (or made other errors), please call them out in the thread so I can update this!

## Should I Use Tags Or Links?

Hello! Wondering about the nature of tags or links in Obsidian is very common!

The reality is, there isn’t one single answer to this question, but this article is intended to help you understand why one or the other might be better for your situation. We will lay out the facts regarding how tags and links work, so you can make the decision that suits you best.

## Tags and Links Aren’t Actually That Different

In Obsidian, tags are actually a kind of link!

What Obsidian calls a link can be defined as: “A connection from one note to another note”.

In Obsidian, a tag is: “A connection from a note to an idea”.

Every note in your vault is a “node”, as you see when you open the graph view. Every tag is also a node, just with no file behind it! You can see this within the graph view by turning on “Tags” under the “Filters” option!

This means a few things:

1. You don’t actually have to choose between tags and links for organization! They’re complimentary, and we’ll go over why in the next sections.
2. You can’t go *very* wrong in whichever path you choose. The two ideas are so similar that there is almost always a way to make tags or links work *mostly* like the other. In other words: you can achieve nearly all the same functionality with either tags or links… **the differences are almost entirely a matter of convenience!**

## Tags and Links Aren’t Equal, Either

But tags and links aren’t exactly the same, either, and those matters of convenience can become significant over time. Here is a list of factual differences between the two:

### Links auto-refactor by default, and tags do not

This is a big one!

When you change the name of a file within Obsidian, *all* links to that folder will automatically change to be pointing to the right place.

Changing tag names through the entire vault requires the help of a plugin (such as [GitHub - pjeby/tag-wrangler: Rename, merge, toggle, and search tags from the Obsidian tag pane 452](https://github.com/pjeby/tag-wrangler)), or a risky find-and-replace procedure.

### Click behavior is very different for tags and links

Clicking on a tag will open a search for all files that contain that tag.

Clicking on a link will either:

- Open the file the link is pointing to.
- Create the file the link is pointing to, if it does not already exist.

### Tags are implicitly counters

Instances of each tag are automatically counted up by the Obsidian tag pane! This means that ever tag automatically is also a visual counter of how often that tag appears in your vault.

### Tags can be hierarchical

`#level 1/level 2/level 3` is a valid tag!

Tags are effectively a “virtual file system”, meaning they can be organized into a tree just like folders, except without the rigid properties of on-disk folders.

### Links can have aliases

A link can have multiple “names”, in the format of `[[A Note Name|An Alias To The Note Name]]`. This can be handy, and is not something tags can do.

### Tags can be defined in front-matter

Tags can be defined at the top of a note, something like:

```yaml
---
tags: [writing/blog, ideas, blog/status/draft]
---
```

This can be a useful way of adding organization to a note in an invisible way. While links must always be written out in text, front-matter can be hidden in Obsidian.

## Introduction To “Higher-Order Notes”

If you want to organize using links, then eventually you are going to encounter the idea of a “higher-order note”.

You might have heard the term “MoC” used around the Obsidian community. This stands for “map of content”, and they are a kind of “higher-order notes”. A higher-order note is any note that exists to help you navigate to other notes. The naming isn’t 100% agreed on, so don’t let that confuse you. “Indexes”, “MoCs”, “Higher-Order Notes”… They’re all pretty similar.

### What problem do these solve?

HONs solve the problem of navigation between groups of notes *without* the necessity of using tags. A HON fulfills the same function as a tag: A connection from a file to an idea. A HON is what would happen if, when you clicked on a tag, a note opened representing that tag.

HONs are objectively more functional than tags, as they have all the power of a note, including the ability to have their own tags, *but that doesn’t mean they are necessarily “better”.*

#### HON Potential Benefits

A HON:

- Can easily show different “lenses” of data, with the same links displayed in different orders. (Within an “animals” HON you might have “Animals that lay eggs” right alongside a list of “Animals that give live birth”).
- Benefit from the auto-refactoring nature of links. Any change to a note’s name will automatically update the links.
- (Author’s note: This is particularly beneficial when a group of data is not well understood yet, as note names are more likely to change in this period.)
- Can easily contain notes, explaining why the links are the way they are, as opposed to tags which are fully static.

#### HON Potential Downsides

A HON:

- Is more complex than a tag, which might require additional, unnecessary maintenance.
- Has no clear, obvious pattern of construction. Its structure is entirely a matter of convention.
- Must be backed by an actual file on the file system.
- Does not automatically get a counter of any kind.

## Summary

I hope this article has given you a good, basic understanding of how tags and links fundamentally work within Obsidian. There is no reason you need to choose just one or the other! You can mix and match easily, using the unique features of each to benefit your desired workflows.

I also help it gives you a little bit more of a sense of peace going into starting your Obsidian journey, knowing that this isn’t a “choose the wrong path and screw everything up” kind of choice. It’ll be fine, no matter what!

Good luck, and have fun making your notes awesome!