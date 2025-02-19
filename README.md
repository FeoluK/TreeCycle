# TreeCycle

## Brief Overview
TreeCycle uses VR to show kids how everyday recycling choices shape our planet. Through immersive visualization and interactive gameplay, we're making environmental education engaging and impactful.

## Inspiration
After awkwardly staring between the trash can and recycling bin trying to figure out where our empty Roost & Roast takeout containers should go, we realized that none of us really knew the answer. Despite seeming like such a simple and straightforward binary problem, there is so much ambiguity and misinformation regarding recycling. We wanted to tackle this issue from the bottom up by building something for environmental education.

After some initial research, we found two main causes of unsustainable habits. The first is a lack of environmental curricula, specifically for students in grades K-6. The second was the "one person can't make a difference" mindset—a sort of diffusion of responsibility that many use to justify making unsustainable decisions. Brainstorming ways to tackle these issues, TreeCycle was born.

We decided that we could gamify this process of learning to discard waste and turn it into a VR application that would be a fun and engaging method to teach kids how to get rid of their waste. In addition, being able to control the environment of the virtual world allowed us to change the scenery depending on whether or not the user chose the right bin, helping teach kids that their choices do directly impact our Earth.

## What it does
Our product sets up an environment for people to explore how to discard their waste through two methods: "practice" and "clean mess". For the practice method, we created a welcoming environment that allows users to interact with the world around them and practice discarding the various articles of waste scattered across the ground, updating the dynamic world around them to reflect the effects that their choices would have on the environment. An additional feature that is extremely useful is the clean mess method that is built from a mobile application where you are able to take a picture of articles of waste that you want to clean up, and a model that we've trained identifies what waste they are, and populates the VR game with those exact waste articles so you can practice cleaning up your mess in a fun environment, while simultaneously learning how to actually clean up your mess.

## How we built it
Our product consists of three parts, the iOS application, the ML model, and the VR Application. Our ML model was trained using NVIDIA's Brev.dev platform where we rigorously trained data using a finetuned YOLO model to identify pieces of trash from a picture containing multiple articles of trash. The model identifies what trash it is and creates a JSON file with the objects it found. In order to get an image of the trash, the iOS application has been built to have the capability to take a picture and then send it to an API that handles the image and returns data containing what objects it found. Then, the VR application is able to access that same data and create a game to work with sorting the pieces of trash that you have taken a picture of. Additionally, the VR Application has access to common trash items and can create a randomly generated game that helps people learn to sort their trash even when they don't have a mess.

## Challenges we ran into
One of the main issues we ran into was that we worked using Apple's Vision Pro, and due to the fact that it was recently released, there isn't a great deal of documentation for the device, and we often had to do rigorous research to get even basic features implemented due to how complex the Vision Pro is. 

Another issue was being able to integrate all of the moving parts of this product since there were so many different factors that came into play, whether it was the iOS Application, the classification model, or the VR app, being able to get everything to work between each other was difficult and challenging to integrate.

## What we learned
Aside from tackling the technical challenges of integrating VR, iOS, and computer vision, this project that designing meaningful educational experiences requires extensive consideration for the intended audience. Through researching current discussions on environmental education, we learned that creating learning experiences for young students is far more than telling someone "recycling is important." Showing them the direct impact of their choices through immersive visualization can fundamentally change behavior. The immediate visual feedback in our VR environment—seeing the trees around you grow when you make the correct decision—helps break down the common "one person can't make a difference" mindset. Our most important takeaway is that **developing human-centered technologies requires consideration for human psychology and cognition.**

## What's next for TreeCycle
We intend to reach out to elementary school teachers for feedback on our product. We are working toward conducting testing sessions with students and gathering direct feedback on the game's engagement. We also recognize the price of VR headsets raises concerns regarding our product's accessibility in underresourced communities and intend to start conversations with educational nonprofits to ensure our product isn't furthering socioeconomic gaps.
