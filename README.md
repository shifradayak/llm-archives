# llm-archives

### Instructions

Click the "Use this template" button for this repository and choose "Create a new repository". You can give it the same name (llm-archives).

Once it's ready, go to [Groq](https://console.groq.com/keys) and follow the directions to get an API key. You'll need to login (or create an account if you don't have one).

Copy the API key value and then click on the Settings of your GitHub repository and click on "Secrets and variables" on the left side, then choose "Codespaces"

Click the green "New Repository Secret" button and paste your API Key into the "Secret" box, then put GROQ_API_KEY in the Name box above it. Click "Add Secret" and click on the name of the repository to return to the main page.

From there, click the green "Code" button and create a new Codespace in the Codespaces tab.

In the Terminal type the following: pip install requests groq and hit enter.

Then type: python get_stories.py

You should see a file called cns_maryland_posts.json appear. Let's look at it. It contains some details of the past 10 CNS stories.

Back in the Terminal, type: python entity_extraction.py and watch the output.

### Evaluation for JOUR389W

PUT YOUR EVALUATION HERE
I chose this Grist story on a challenge by Republican attorneys general to the EPA's use of the Civil Rights Act in regulating pollution: https://grist.org/regulation/republican-attorneys-general-epa-civil-rights-law/. I thought this worked pretty well — the lists that Groq generated were entirely accurate based on skimming the story and manually pulling out the people, places and entities mentioned. The one area where things were a little off-base was with specificity. In the places category, for example, the Grist story mentions the "Deep South" as a concept/category of places, but Groq just listed it as a place of the same nature as Flint or Louisiana, which isn't entirely accurate. It's used more in a metaphorical sense as a writing tool in the story, so it would be good to distinguish things like that (e.g. regions vs. actual census-designated places) given that they may have different contexts and roles in different pieces of reporting. Also, under the people section, some of the people listed are sources that Grist reporters interviewed, while others are simply mentioned by name as part of historical context. There also isn't a distinction here, which might be helpful to have if a newsroom is trying to keep a specific archive of people it's talked to, rather than just any people mentioned in its stories. Despite these small things, I think this could be really important for a newsroom like Grist to keep documentation of its reporting and build an archive of sources and stories. Building up a source database is important to ensure that Grist is talking to a diverse base of sources and doesn't use the same people too many times, and also to store information about people for easy access and source-building (which are two sides of the same coin, almost). From a place perspective, Grist could also use a tool like this to keep track of the different cities and regions it's reported on. As a publication focused on environmental solutions and justice, it's important for Grist to be intentional in what and who it's covering, so having a record of all the places mentioned in its stories could help reporters determine if there are any environmentally-significant places that aren't getting the deserved coverage, which is one important step in remedying reporting gaps.
