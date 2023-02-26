demo: https://www.youtube.com/watch?v=gWQ1JKxKllw 

## Inspiration
We are no strangers to the extreme political dichotomy in our society today. From the Capital insurrection, to election deniers, and even controversy about vaccines, we are exposed to countless opinions and articles online. 

Adding fuel to the fire, many social media sites customize your recommended content to fit into a little "bubble" of others who share your opinions, creating an echo chamber where you are exposed to the same ideas, over and over again. But how can we easily tell how factual the articles are? And how do we know if the news is biased towards a political viewpoint?

That's where BiasBubble comes in. By installing the chrome extension in a few clicks, you can instantly see the accuracy and bias rating for every google search result. Take control of the content you consume online!

## What it does
The extension is used in two ways
1. A button under every search result showing accuracy and bias. It can be clicked to define the output, taking you to https://mediabiasfactcheck.com/. 
This is a site we learned about in my AP Econ class. It analyzes + fact checks articles and publishing sources to determine where they lie on the bias and accuracy scale.

2. Click on the extension while reading any article to get a summary and explanation of the accuracy/bias. 

## How we built it
By not sleeping. No but actually, we fetched data from the [newscatcher API](https://newscatcherapi.com/) every few minutes with cron jobs and hosted them on dfinity.  Then, I used basic NLP libraries to detect the source of each individual article and run it through my REST API. Finally, I integrated it into the extension, built with simple html and js.

## Challenges we ran into
A lot of things kept breaking. Dfinity: hosting and integrating it with the extension took a while to figure out, and I had issues with manifest being deprecated on basically every version. 

## Accomplishments that we're proud of
I'm proud that I created such a usable application with technologies I'd just experimented with before! I genuinely see people integrating this into their browsing, and I have found it really interesting to see the types of articles and viewpoints that are recommended to me.

## What's next for Bias Bubble
I would like to add support for different sites, like Facebook, where a lot of misinformation is spread. Also, it would be great to have BiasBubble on WhatsApp, because I personally know many of my relatives use it to spread false or misleading articles almost every day. Another possible feature is recommending aricles with different stances on the same subject, so users can get a more diverse perspective.

## How to use
1. Go to the [github repository](https://github.com/nngngn/bias-bubble/) and download the code. 
2. Unzip it. 
3. Then go to chrome://extensions, click "Load unpacked" and upload the "chrome-extension" folder you unzipped.
4. That's it! Try it out instantly on a google search, or click the extension icon while you're reading a news article. 
