# Karla AI Discord Bot

Video Demo: https://youtu.be/cTxS9pnVBwc

## Inspiration
My inspiration for this bot has been all the times that I have gone to the gym and don't know what to do. Getting started at the gym can be intimidating and getting a personal trainer can be expensive. So I tried to figure out a way that I can ask someone a quick question about what exercises they recommend for a leg day or back day. It can even recommend exercises for you if you need to recover from a sprain or injury.

## What it does
Karla gives you a list of 3 or 4 exercises for a routine that helps you workout an body part of your choice. You can talk to it from your own discord server.

## How we built it
The bot was built using the Vertex AI Agent Builder and then I used the Discord integration to try and talk to the agent in my own discord server.

## Challenges we ran into
I ran into many problems trying to figure out how to ground the bot answers. I tried to see if I could get data into a data store but have not been successful at it. I uploaded 800 json documents to a data store to see if I could use that data to help the bot but the import to the data store failed. I then tried changing it to a CSV and it did not work either. Formatting did not work properly.

Originally I wanted the agent to also give people a video that would show them how to do the exercise however that was not working and I learned that it was producing fake YouTube links.

Another problem I ran into was that Karla was not getting its prompt updated after saving a new prompt. I removed the references that tried to give people a video from the prompt but it did not work for some reason. I ended up remaking the agent and rebuilding the discord integration with a new bot.

One more problem was that Karla has some hallucinations or maybe I was not being clear with what i was asking. I asked some clarification questions on some exercises and she doubled down on the wrong way to do the exercise. However, after I asked for a better or different explanation of an exercise she would describe it properly.

Final issue I have had was that the agent takes a long time to respond when you first talk to it on Discord. Also I am not sure how to restart the conversation with the agent once I have started one. The agent also seems to time out and stop responding so you have to redeploy the Cloud Run container.

## Accomplishments that we're proud of
I have gotten more comfortable with using the Google Cloud console because I had to move across different different tools in the Cloud.


## What we learned
Things I have learned:
- Create and use use Google Cloud storage buckets
- Upload a docker image into the Google Cloud Artifacts
- Using Cloud Run to serve the bot to Discord
- Creating service accounts using the IAM API in Google Cloud
- Vertex AI Agent Builder 
- Integrating an agent with Discord
- Learned to make a Discord bot

## What's next for Karla
Now that the Hackathon is done Karla will just be shut down. The infrastructure in Google Cloud has all been shut down and deleted.
