# Lesson 3: AI Botnets, Incentivized by Cryptocurrency
In this lesson, we demonstrate how Koii nodes can be used as a hosting infrastructure for generative AI deployments.

Because some devices may be smaller, or have limited resources available, we will take advantage of open source tools from Gemini AI to write comments and process bulk information.

Our bots will use BlueSky, the open Twitter universe, to post content and learn from one another. 

Once you've deployed this project, you'll have your own army of Koii nodes, each with their own BlueSky Accounts, powered by intelligence from Google Gemini. 

**Note:** Because both Gemini and the BlueSky API are open endpoints with free tier access, Koii nodes can join for free and earn a reward when they run your task. 


## Project Structure
The Koii Task will run periodically, every 10 minutes, and will index the latest tweets on BlueSky matching a keyword. As the nodes index content, they will build up a 'context', which they will feed to Gemini to generate insightful tweets.

Our army of bots will help to spread uplifting and positive messages of your choosing.


### BlueSky Integration
You'll need to start by generating a Blue Sky API Key. An API Key is a token (a string of letters and numbers) that gives you special access to an online service. Think of it like a password.

[Generate you key by clicking here and signing up for an account](https://blueskyproject.io/tiled/how-to/api-keys.html) 

### Gemini Integration
The Gemini module is managed in `src/gemini/` and features a basic implementation. 

You can test the Gemini integration by adding your Gemini API Key to the `.env` where it says `GEMINI_API_KEY`.

Then, run the following command to test the key works:
```sh
node tests/testGenerateComment.js
```

If you don't have a Gemini API Key, you can get one for free [here](https://aistudio.google.com/app/apikey).


## Mechanism Design and Task Deployment
Now that you have the basic functionality of your Koii Task in place, we'll begin testing the payments, verification of work, and then get your task deployed onto Koii Nodes.


#### Testing and Deploying Your Task
Now that you've configured your rewards and have your task ready to go, you can follow the end-to-end deploy guide to get your task up and running on your Koii Node. 

[< Click Here to Get Started > ](./TaskDeployment.md)


## Going one step further...
If you got through everything and you're bored, this is where it gets creative.

There are a few ways to make your bots *shine*.


### Extend the Context Window to Include More Information
Implement improvements to the Gemini module by implementing a wider context window (more information) for your AI to act on.

Gemini supports long-context file storage via the API, which is described [here](https://ai.google.dev/gemini-api/docs/long-context).

*Context Caching* provides API management and usage of the key components, and supports garbage collection to reduce costs.

Some examples of large context data you can use:
* A PDF Like the [Koii Whitepaper](https://koii.network/whitepaper.pdf)
* A download of a website or blog like [Econ3.org](https://econ3.org/archive.html)
* A video or other larger file from Youtube or elsewhere (you'll need a crawler for these, unless you want to download it manually and package it with the task) 


### Incorporate Non-BlueSky Data into Your Task Flow
Just reading and regurgitating existing Tweets from BlueSky can get a bit boring, so you might want to try adding an external service or web crawler to give even more information to your context window. 

One option is to include a Puppeteer window and crawl the web for more information. [Check out the Koii EZSandbox for some example code.](https://github.com/koii-network/ezsandbox/tree/main/Lesson%203)

You can also implement the [Google Custom Search JSON API](https://developers.google.com/custom-search/v1/overview) which provides 100 search queries per day for free.

Another way to do this is to include another Generative API like ChatGPT or Claude, which offer basic packages and API keys for free. 

In any of the above, it is suggested to incorporate additional JSON data into your existing Gemini generation flow, which can help produce more interesting comments and allow the other bots a chance to grow and learn from outside sources of information.


### Update your BlueSky module to Post Tweets instead of just replying
The BlueSky API has lots of available options, check them out [here](https://docs.bsky.app/) and look for interesting ways to improve your bots' performance.


### Experiment with the Rewards Mechanism
So far, we've left the distribution file alone, but you can make updates at `src/4-distribution.js` to improve functionality and give your nodes a reason to work harder. Just be sure to map your rewards to the value being created, so that your token supply is not needlessly inflated.

What's the best way to reward nodes for their work?

Here are some ideas:
- Rewards based on [Tweet Views](https://docs.bsky.app/docs/api/app-bsky-feed-get-actor-likes)
- Rewards based on the [amount each node is staking](https://www.koii.network/docs/develop/write-a-koii-task/namespace-wrapper/task-state#gettaskstate)
- Rewards based on how creative the node is and how unusual it's content becomes [(hint: you'll want to check for new keywords that other nodes aren't using)](https://www.npmjs.com/package/node-nlp)
