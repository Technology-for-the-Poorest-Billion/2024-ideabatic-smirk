---
title: SMIRK - Miniaturising A Vaccine Cool Box
---

# Project to miniaturise Smile by Ideabatic

## Introduction to project
The SMile project is a project created by the startup Ideabatic. Their aim was to make a smaller and simplified version of their current well recieved SMILE, which we were tasked to design and prototype. We placed an emphasis on the modularity and repairability of it, focusing on ensuring the pack could be used for a day keeping the vaccines at teh critical temperatures for over 24 hours


Put project core ideas, and show out final outcomes (no reasons jsut the concepts)
Put the core  SDGs it solves (in the ideabatic website)
Image showcase

## Aims of the project
Every day, thousands of vaccines are destroyed and rendered useless due to heat. The SMILE Vaccine carrier aims to solve this by emphasising the ease of use, limited scope for faliure, and comfort in carrying.The smile is used in long journeys which require hours of walking to get to small villages without the easy access to modern medicine. While the current box is fantastic for this use case, having such a large box that can last 5 days is not always suitable, especially not for shorter last mile journeys, where the majority of it will be done in a car. This is why we are aiming to bring all these features to a smaller, cheaper, and simpler version. The current [market options](market_research.md) do not have a big place in markets like this, and so the smaller Smile will help with transporting vaccines at a similar price point to the market iptions, while being specifically designed for this use case, and not a short trek down the road from a GP office.
Talk more about the issues the project addresses and talk about how we accheived it.
Modular straps, easily repairable, useful etc.
etc]
### Market research
Talk about how our solution is better than other options while still beinmg more portable than the original smile. [link to market research page]

## Features Section
Show the features in detail and explain how they help 
Each image has link to its lil prototyping section for each of us

### Ice pack chamber design and prototyping (linked in subpage) with all teh maths and code showcase
The inner carousel was designed to be both modular and easily repairable. The foam allows for the expansion of the bottle once the water has frozen, and continues to hold it securely once the bottle begins to melt. The foam can be easily replaced, and is physically separated from the vaccines, so can be replaces with any scrap foam. (???) unsure about that last sentence. 
[IMAGES]

### Size Reduciton
With this new inner carousel design, we managed to ensure the vaccines be kept at 2-8 degrees throughout the cross section for up to [24 hours](ice_chamber_code_slash_maths.md). The size savings were up to XXX%, reducing the overall weight drastically, making it incredibly portable for the smaller journeys.
(gonna ask for weight stuff once bottle arrives)
### Carousel
The vaccine carrier was designed to be modular while still securely holding the vaccines. The butterfly wing shapes allows different types of vaccines to be fit securely regardless of the dimensions of the bottle, and is made of a durable rubber which can be easily swapped out. The proposed idea is to repurpose the same design, but combine them to make one section which can be attached together to form the carousel in both sections, while keeping the parts the same regardless of the size of the smile. This also allows for a storage compartment to be clipped on, gicing a small box where the clean needles and sanitary wipes can be carried without the original backpack
(withholding review/deail until prints finish)
### Carrying
The backpack added some comfort while carying, and allowed for important information to be written on the top, with added capacity for a biohazard box for the needles and syringes used. It was quite expensive and bulky though, and so we came up with the solution to...
(waitning for wednesday to finish)

### Backback design with how it will strap on and comfort etc.
Talk about how it'll be attached, and how it will remain vaguely comfortable. [Links to prototyping and more detail about attachment mechanisms]

### Vaccine Carousel design 
[Link to how it will hold, different iterations, what worked, what didn't]

Also in each of the sub pagestalk about specifically how it could be implemented (Like kitty would have to find another insulation material, or she would have to injection mould the vaccine rubbber already bent / something similar


## Road to miniaturising
Put links and documentation to initial ideas, and how the market research was further refined
### Redefined aims of project, and expand on what teh orignal breiif was, howe we looked into it, how it changes, and how we settled on a final project




# handout stuff
## Group report 

Web-page highlighting the general context of your work (i.e. the problem your
partner is trying to solve and how your work fits into this) and the technical summary
of what you did and/or achieved. This should be aimed at the general public.
Illustrations and other media supporting ~500 words of text would be appropriate.
Keep it concise and engaging.

• Reflective discussion about the work’s alignment with the Sustainable Development
Goals and where applicable with the UNICEF principles for Digital Development. ~500
words, attached to the web page.

• Statement about project management, explain the team work strategy. Reflect on
what worked and what didn’t work, drawing constructive recommendations where
possible. ~500 words, included in the webapge, git repo or github wiki.

## Individual report – Wiki format. You may use markdown files on the git repository, and the
GitHub wiki feature on your repository.
Each student will take ownership of a part of the technical output, giving credits to others
where appropriate. It would be helpful if the author of each each section is clearly indicated
on the mardown file, although the commit history would also reflect this in principle. There
are 15 marks available for this section (individual). The content should cover:
• The technical presentation of the solution and its effectiveness to address the
problem, presented as handover notes for the partner.
• Description of the data/code/blueprints available in the repository, with links to the
content as required.
In addition to the technical quality of the work, the following criteria will be part of the
assessment:
• Is the document clear and complete enough for someone else to use the work?
• Could somebody else continue the work based on the information available? (code
well documented, building instructions, briefing notes about strength and
weaknesses of the project, material well structured, etc.)


### To configure your website:

- The required files to run a basic website are included in the repository. We use here Jekyll to turn markdown files into html that will be automatically updated on the website. The component responsible for this is a GitHub action, which is specified in the folder .github/workflows. There is no need to change this file. However:

- In the settings of your repository, go the section "Pages", and select GitHub Actions in the drop down menu to indicate that this is the way you'd like the webpage to be generated.

- Each time you update the markdown files in the www folder of the repository, it will regenerate the web content. The address of the website will be:

```
https://technology-for-the-poorest-billion.github.io/[your repo name here]
```

- index.md is the root of your website. To link another page from here, located within the www folder, use the following syntax:

```
This is a [link](linkedpage.md) to interesting content.
```

Which results in:

This is a [link](linkedpage.md) to interesting content.

- Pay attention to the header of the markdown files in this section. It contains a title section that you will need to reproduce for each page to render them properly.


