# Contributing Guide

We welcome input from users on expanding this wiki. Sometimes it takes a village to share the wealth of knowledge out there.

This guide will provide methods to make submissions to the wiki as well as the process to expect when a submission is made.

## Goals

Remember, there are some things that you need to keep in mind when submitting new things or changes to the wiki:

* The directions must be clear and concise.
* It must be able to be replicated by someone else. Someone should be able to take your document and starting at the top, they should be able to move step by step through it and at the end have the same thing setup as you have.
* Don't be discouraged if your changes or new item is rejected. It just didn't fit what we needed at the time. If it was rejected, you will be told why and what needs to be done to fix it for it to be included.

## Methods to Contribute

### GitHub Pull Request

If you are familiar with how Git and Github works, or you have used Github before, you can fork and clone the wiki repo [github.com/hamsoverip/wiki](https://github.com/hamsoverip/wiki), make a change and do a pull request to submit it back. Once the PR has been reviewed and merged, the change will be deployed to the wiki site automatically. That is all you need to do if you are submitting that way.

This is good for both new items and change requests.

If you have forked and cloned a previous version of the repo, ***PLEASE*** make sure that you merge any outstanding commits from the main repo to your fork and then do a `git pull` prior to doing any local editing. This wiki is always in flux and if you do not merge those commits and then do a pull prior to starting editing, you will either miss updates or overwrite things on the repo. It is always good practice to do a merge and a pull prior to starting work on a forked repo anyway. This makes sure you are on the most current `main` branch edits.

### Non-Github related way

If you are not familiar with Github, or do not have an account, that is ok. You can still contribute.

If this is just a change request (in other words something needs to be changed or updated on the wiki), please submit it in the [:fontawesome-brands-discord: #wiki-chat](https://discord.com/channels/966060559961296956/975534734157443112) channel on Discord. No need to format it or anything. This would be things like "This word is mis-spelled" or "can you add this?" if it is longer, like a rework of an existing document, then please put it into a Markdown Document to make updating easier.

If this is a whole new item, it is asked that you make the submission using a Markdown Document.

??? tip "Not familiar with Markdown?"
    If you are not familiar with Markdown, it is a very simple way to format text files. In fact, this wiki is actually done in Markdown.

    Markdown makes documentation much easier as it is easier to format commands and such in a way that is familiar.

    A Markdown Primer can be found [here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

#### Submission

If you are not using Github to do a pull request, to submit the file, please upload the file to the [:fontawesome-brands-discord: #wiki-chat](https://discord.com/channels/966060559961296956/975534734157443112) channel on Discord. The Wiki Maintenance team will take it and review it.

## Approval Process

Once the change has been submitted, the document will be reviewed. If more clarification is needed, changes will be asked for and the updated file resubmitted. Once everything is in order, the change will be approved and the submission included in the wiki.

This process is in place to make sure we have very good and complete documentation on things. It does no good to have a wiki and have things that do not work. But at the same time, if you want to make a submission, be thorough. Go through the process of creating the documentation.

## Tips for Submission

* Look though the Markdown Primer linked above.
* Look at the Github repo (it's a public repo) for the HOIP Wiki to use documents as examples of how to proceed and how to structure your document [github.com/hamsoverip/wiki](https://github.com/hamsoverip/wiki).
* If you have questions, ask. That is what the [:fontawesome-brands-discord: #wiki-chat](https://discord.com/channels/966060559961296956/975534734157443112) is for in Discord.
* Please do not submit anything other then a Markdown Document. This will get your submission rejected right off the bat till it is in the correct format.

## Tips and Tricks Learned about MKDocs

* Typically in Markdown, you only need to indent 2 spaces for nested lists. Apparently in MKDocs, you need to indent 4 Spaces. The upstream provider for the Markdown Plugin for MKDocs has decided to die on a hill and say this is not a bug, which sadly it is. So when doing nested lists (sub points in a list) make sure to indent them 4 spaces.

----

!!! info "Last Updated 2024-07-09"
