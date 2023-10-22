
# Cloudflare LLaMa Worker AI Chatbot

This project is a POC and a pretty basic (but will be updated!) way of creating your own chatbot using cloudflares new and 100% free (No KYC or credit card!) way to create an AI chatbot with a simple UI.



## Steps

First create a cloudflare account.
https://cloudflare.com/ this is 100% free and does not require any KYC. Max 100k requests per day. (on free plan)

```
  1) Create cloudflare account
  2) Go to https://dash.cloudflare.com/
  3) Click workers & pages
  4) Click overview
  5) Click create worker
  6) Name it whatever you want
  7) Click deploy
  8) Click edit code
  9) In this repo there is the CF folder and HTML folder, in the CF folder copy all the code inside the worker.js file.
  10) paste the code in & click save and deploy
  11) Copy the URL and save it since it will be needed.
  12) Next eather use cloudflare pages (recommened) or any other hosting site of your choice for static hosting such as netlify or github pages
  13) Upload ALL the files from the html folder and edit the script.js
  14) modify the API Url to the URL you got from your worker
  15) Profit!!
```
    
## Basic API Explenation

The API is pretty simple, there are 3 main parts:

1) the root page ==> "/"
2) the API page "/:API"
3) the query "/:API?q=%query"

The root page simply just redirects you to the API page with a randomly generated API key
the API page shows the message history for that API key
the query page is how the user sends messages and returns a responce.

### Future updates:

```
1) Rate limiting your API [PARTIALLY DONE ☄️]
2) Password locking your API [NO SUPPORT YET🌑]
3) Much better Frontend UI [WIP]
4) Ability to keep UUID/apikey and go back to previous conversations (frontend) [NO SUPPORT YET🌑]
5) Add markdown support on frontend [DONE! ⭐]
6) Ability to change models quickly and easily [PARTIALLY DONE ☄️]
7) Voice & audio to text via wisper (not any time soon) [NO SUPPORT YET🌑]
```

### Why this over the offical cloudflare API?

1) custom domain.
2) much more customization.
3) ability to easily share your api without giving out any api keys.
4) chat history (limited but better than none) and ID system.
5) pre-made frontend

#### known issues:
--> Sometimes the bot will respond with nothing, this is becasue the amount of text in history execed cloudflares max which is pretty low, solution is to lower max history or set it to none if needed.

#### Wanna host *without* cloudflare workers?
Use miniflare! allows you to host cloudflare workers off your local machine and if you wanna go all out use cloudflared tunnel to create a tunnel to the public with your custom domain!
https://github.com/cloudflare/miniflare

### If you are using this project PLEASE provide credit it is greatly appricated :)
![Logo](https://github.com/localuser-isback/Cloudflare-AI/blob/main/logo.png?raw=true)
