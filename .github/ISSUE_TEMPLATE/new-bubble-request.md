---
name: 🫧 New Bubble Request
about: Use this template to request a new bubble
title: "🫧 [BUBBLE REQ] New Bubble Request <....>"
labels: bubble request
assignees: ''

---

# Setup Requirements for New Bubble

## General Context

Please write at least two sentences explaining the general context for this request, including why it is needed, who will use it, its business purpose, and other relevant general information that might inform its design and deployment.

## Bizdev Contact Person

Please specify who in Bizdev is making the request (and mention if you are making the request on behalf of some other contact or external client or potential client).

## Deadline / Importance

Please specify any deadline or timeline when this setup must be available by. Note: This deadline is not committed to until the ticket has been reviewed and moved to committed status by dev.

## Bubbles Required

Please detail the bubbles required as A,B,C etc.  For each bubble specify whether it 

- is a participant bubble (used for reviewing own data and selecting what will be uploaded) or a destination bubble (used for viewing multiple individuals' data together)
- (for a participant bubble) which destination bubble it uploads to

For example:

### Bubble A

-  Participant or Destination: Participant
-  Uploads to Destination Bubble: B

### Bubble B

-  Participant or Destination: Destination
-  Uploads to Destination Bubble: N/A

## Bubble Appearances

For each bubble please provide the following information:

1. Display name of the bubble (mixed case, spaces and punctuation allowed)
2. Shortname of the bubble (for use in URL, no spaces, no punctuation except dash, lowercase only)
3. Image or Image URL for the bubble (in bubble sidebar menu and top of experiences list within bubble). If you don't have one you can say 'default Hestia logo'
4. Text to display in this bubble's outgoing consent/upload form, including any options or choices that need to be included
5. Small description the bubble (appears underneath its title)
6. Text content for bubble homepage (can be a long paragraph or two, appears above the list of experiences within the bubble)
7. State whether bubble should be listed publicly (e.g. on digipower.academy) or hidden

## Bubble Security: Passwords

For each bubble, please specify a username/password combination (or state happy with random username/password assignments). By default, each bubble will have a different username and password and all bubbles will have a username and password. Please state if any of the bubbles should be unsecured.

## Bubble Security: Encryption

For each Destination bubble, if data stored in that bubble is to be encrypted, please provide a public key to be used for encryption. You can generate a key at https://digipower.academy/import/

## Experiences to be included

Please specify which experiences should be included in the bubble set. Or you can say 'the default set' which is: Facebook, Twitter, TrackerControl, Apple AppActivity, Instagram, Uber (rider), Tiktok, LinkedIn, Netflix, Strava, Fitbit, Google Takeout, Generic

----

# Development requirements for new Bubble

The above requirements can be satisfied with minimal code - mainly just config. However we recognise that requirements can be more complex. Please provide details of application/functionality-specific requirements using the sections below. All custom requirements will take additional development time.

## Custom Data Sources

For knowing the data source of a bubble, we assume that:

- All Participant Bubbles allow viewing of local files in browser only and do not access data stored remotely anywhere.
- All Destination Bubbles load data from a bubble, which will include data from multiple users.

If a particular bubble uses a different source than this assumption, (e.g. a participant/destination bubble hybrid, or something that uses some other source such as an external storage API) please specify it here. Similarly if a new type of file is to be supported, detail that here, and provide a sample if possible.

## Custom Set of Views

For deciding what views will be available within the experiences within each bubble, we assume that:

- The experiences within all Participant Bubbles will not include any aggregate views, only individual tabs for different types of data
- The experiences within all Destination Bubbles will include both individual details tabs (e.g. tables/maps) as well as aggregate views

We further assume that all provided tabs will be the same ones we already have for those companies on existing experiences.

If you require any new views or different sets of tabs than the standard set, for any of the experiences you listed, for any of the bubbles, please specify the requirements about which tabs/views you want in each bubble, in as much detail as possible, here.

## Custom Aggregations

Currently we offer Aggregate statistics for Twitter, Google, TrackerControl, Apple AppActivity - in Destination Bubbles only.

If you require any aggregations in Participant Bubbles, or any new aggregations that do not already exist, please specify in as much detail as possible, what aggregate statistics or views/tabs are needed, in which bubbles, for which companies/data sources, and specify how to calculate them if it is not obvious.

## Other customisations

If there are other special requirements, such as teacher features, analytics, unusual flows, different import requirements or storage requirements, please provide as much detail as possible here. Please note that anything more complex than the standard version as described above will take longer.
