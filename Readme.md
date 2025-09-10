This is my template for using Obsidian as an electronic lab notebook (ELN). Read about the idea behind this template on my website [here](https://swnkls.nl/en/posts/obsidian_as_an_eln), and a bit about ELNs in general [here](https://kagi.com/assistant/feaa8e18-5dd5-446d-8d78-ad8626e52306). If you don’t feel like reading and just want to get started, [[Quick-start guide|go to the quick-start guide]]. If you enjoy reading, you’re on the right page.

Note that this vault is supposed to be read inside of Obsidian! If you are reading this on github or elsewhere, download this vault [at this link](https://github.com/WetenSchaap/ELN-for-obsidian/releases/latest), unzip the vault, and open it in Obsidian.

## Try it out!

The best way to find out if Obsidian (and this template-vault) suits your way of working is just to try it out for a bit. Use it for a few days side-by-side with your current lab notebook and see if you find things easy. If not, maybe Obsidian/this template is not for you. That is fine! Don't worry about it.  
Don't be afraid to try new things and break them. A lab notebook is quite a personal tool, and you should feel comfortable using it - you are probably the person who will profit most from using it properly. Go through the settings! Change stuff you don't like! Install weird plugins! Don't feel constrained.

## Before we start

Below, I assume some basic knowledge about using Obsidian. This is not a general introduction to Obsidian (that would be wayyyy too much work), but an introduction to this template. If you have little/no experience with Obsidian and don't understand something, try just going with the flow; maybe the meaning will reveal itself later. And you can always search the internet - there are many Obsidian enthusiasts online, and you are not the first confused person!

If you have any comments/problems/etc., please let me know! You can leave a comment [here](https://swnkls.nl/en/posts/obsidian_as_an_eln), or contact me [here](https://swnkls.nl/en/contact).

## How to use this template

### Note types

There are a few fixed categories of notes, all with their own template, managed with the [Templater plugin](https://silentvoid13.github.io/Templater/). Everything you write in the template note will automatically appear in any new notes you make.

#### Daily notes

First are your daily notes. This is the first thing you see in the morning when you open Obsidian. Obsidian will automatically open today's daily note when you start it (and create it if it does not exist yet). This is an example daily note, from 29 August 2025, filled with some random information: [[dailynotes/20250829|20250829]].

Every morning, I write my to-dos, things to remember, meetings, etc. in the **To do today** list. You can link to experiments, meeting notes, etc. here.  
With the help of [Obsidian Bases](https://help.obsidian.md/bases), a table showing all the currently ongoing experiments with links for quick access is also shown - more about that later.  
You can also just make random scribbles in it, keep meeting notes, or anything else you want; everything can go here.

#### Experiments

This is (of course) the main business of this template. In an experiment, you write down what you do during an experiment (or a simulation, thought experiment, or whatever you like really). Things written here should ideally be understandable for other people (and yourself) going over your notes, even in 2–3 years' time. An example experiment can be found here: [[experiments/20250901_PJMS01|20250901_PJMS01]]. Instructions for this experimental note can be found there.

The easiest way to create a new experiment is by looking at an experiment and pressing `Ctrl + N`. Obsidian will automatically create an experiment note according to the experiment template. It also automatically names it something like `DATE_PJMS01`. To get your own initials instead of mine, you need to edit the [[__templates/Experiment|experiments template here]]. Don't be scared of the code; just replace `PJMS` in the line `let label = "PJMS"` with your own initials (leave the `"` symbols though!).

#### Stocks & Samples

Preparing simple samples or stocks is routine work and often does not deserve its own experiments. It may still be smart to keep track of samples in case you make some mistake later. Log your samples here and refer to them in your experiments. An example is [[stocks-samples/20250829_Vanilin|20250829_Vanilin]]. Making a new "stocks & samples" note is easiest by opening an existing one and pressing `Ctrl + N`.

#### Meetings

You can also keep track of notes from meetings in Obsidian. There is again a template that auto-generates a note if you create a new file in the daily notes folder. An example is [[meetings/20250829_meeting-with-collaborator|20250829_meeting-with-collaborator]].

#### Literature

If you want to keep notes about your favourite papers in Obsidian, you can of course also do that. I don't want to be too prescriptive about how you do this - some people really go crazy, I prefer to keep things simple. There are many online guides available on how you can manage literature with Obsidian, so just search around. Typically, Obsidian works well together with [Zotero](https://www.zotero.org/); there are a few plugins available for both Zotero and Obsidian to make that easy, like [Zotero Link](https://obsidian.md/plugins?id=zotero-link). A typical literature note in Obsidian would have the title matching the citation key in Zotero, something like [[literature/swinkelsNetworksLimitedValencyPatchy2024|swinkelsNetworksLimitedValencyPatchy2024]], and contain some properties of the paper (title, etc.). You can make notes there, refer to other papers or your own experiments, or add #tags. But this feels very personal, so I encourage you to figure this out yourself a bit.

#### Be creative!

Obsidian is flexible, so do not feel constrained by my selection of notes: if you feel like a note type about, for instance, teaching would be a good addition, add it! If you want to change a note template, go ahead!  
To change a note template, simply open one of the files in the `__templates` folder and change it. The current note types are:

- [[__templates/DailyNote|DailyNote]]
- [[__templates/Experiment|Experiment]]
- [[__templates/Meeting|Meeting]]
- [[__templates/Stock|Stock]]  

To add a new standard note type:

1. Create a new note in this folder, for instance `teaching`. Make the note look like you want, add the right properties, etc.
2. Create a folder where notes of that category should go, for instance `teaching`.
3. Then go to the Templater plugin screen and press `Add New Folder Template`, and add your note template and and folder where the notes should end up.
4. Done! All new files created in this folder will now automatically use your new template!

### Bases

Making notes is very nice and all, but it is not very useful if you cannot find your notes later. So, to solve this problem, we use **Bases**. [Obsidian Bases](https://help.obsidian.md/bases) are files that display your notes in a table, where you can filter for note properties. You can also display the table inside another note. Let's take experiments as an example:  

![[Experiments.base]]  

Here you see all experiments currently in our vault that are _not_ marked as completed. If you make a new experiment, it will be added to the table. In the top left, you can select a different _view_. This means a different filter is applied to your notes. The `All experiments` view will show all experiments, including their name and status. The `Useful experiments` view will only display experiments marked as useful. The `Stale experiments` view will display experiments that are not yet completed but have been created over a month ago.  
You can also make your own view. You can filter on all properties you gave the experiment: tags, date created, the presence of certain words - whatever you want.

In this example vault, I have created four default bases:

1. [[Experiments.base]]
2. [[Stocks & Samples.base]]
3. [[Spreadsheets.base]]
4. [[Meetings & Talks.base]]  

Just look at them if you need to find something specific. You can of course also create your own views inside an existing base, or create your own bases!

## Final comments

If you like using this template, have comments or suggestions, or anything else really, please leave a comment [here](https://swnkls.nl/en/posts/obsidian_as_an_eln) or send me a personal message [here](https://swnkls.nl/en/contact) - I would love to hear your feedback, and whether people find this useful! You can also open discussion or issues in GitHub if you know how to do that.