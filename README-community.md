# The Great List of Stremio Addons

To see the great list of Stremio Addons go to [the website](https://stremio-addons.netlify.app/).

To submit a new addon to the list, use [this link](https://github.com/danamag/stremio-addons-list/issues/new?assignees=&labels=misc&template=submit-addon.yaml&title=Addon+Name).

To upvote / downvote an addon, find it in [the issues](https://github.com/danamag/stremio-addons-list/issues) and react with a thumbs up / down to the issue comment.

To comment on an addon, find it in [the issues](https://github.com/danamag/stremio-addons-list/issues) and comment on the issue, this will update the comments on the site too.


## Project Features

- anyone can publish an addon
- all addons are ordered by community votes, everyone can vote on addons
- addon labels
- filter by addon labels
- comments for addons ordered by newest
- emoji reactions to comments
- "is it online?" real-time check for addons (on the addon page)


## How it works

When submitting an addon to the list, a github issue is created to represent this submission. If the original poster closes his/her issue, or someone with access to the project closes the issue, the addon will be removed from the list.

All addons in the list are ordered by the thumbs up / down votes of the github issues, if an addon has less than -10 votes it is removed from the list.

Labels for addons are a 1:1 copy of github labels used for issues, the colors chosen for these labels on github will also be used on the site.

Commenting on an issue will also add the comments to the dedicated addon page on the website.

The site is currently refreshed based on the following triggers:
- a new issue is created (a new addon was submitted)
- a new release was created
- a new commit was made
- a label was created, edited or removed


## Fork me

This project is available under the MIT license, and uses exclusively free resources. (GitHub WebHooks and Netlify)

To create your own Stremio Addons list:
- fork this project
- enable issues for your fork: Settings -> Features -> Issues
- edit `/config.json` with your repo information
- connect Netlify to your GitHub fork (on `main` branch)
- in Netlify: Sites -> (choose site) -> Site Settings -> Build & deploy -> Build settings: Base directory = "Not set" ; Build command = "npm run build" ; Publish directory = "out/"
- create a Netlify Hook: Sites -> (choose site) -> Site Settings -> Build hooks -> Add build hook (and copy the URL from the hook)
- create a GitHub WebHook: Settings -> WebHooks (left side menu) -> Add WebHook (top right button): Payload URL = URL copied from Netlify ; choose "Let me select individual events" ; ensure "Active" is enabled
- choose events that will trigger the website builds: Issues; Labels; Releases; (other events that could be used: Pushes; Issue comments)

You're done!