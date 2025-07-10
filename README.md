# Purpose

I have created this guide as a reference for on how to interact with LLM APIs from the IBM i. I have done this as a reference for my team, but also others who might need assistance. The goal is to increase the usage of AI / LLMs on the IBM i, but in a purposeful and impactful way. There are plenty of services that offer an easy shortcut to running AI, but they can cost a lot of money and not provide any actionable benefit. Hopefully you learn from this guide what makes sense for you and your business to make real impact at your company. 

# Synopsis

The [IBM i OS](https://en.wikipedia.org/wiki/IBM_i) on [IBM Power Systems](https://en.wikipedia.org/wiki/IBM_Power_Systems) hardware is often called antiquated because of its support and ability to run programs compiled from 40+ years ago. This is misnomer. Instead the IBM i allows you to not have to continuously solve the same problem over and over, and instead leverage the solutions of the past (RPG programs that work exactly as expected) with technology of today. How IBM i allows you to do this is with modern interfaces bridging the gap to the rock solid database and programs. 

When writing new modern RPG programs the ability to integrate with AI / a LLM can seem daunting. However once you see how to setup local machine learning or an LLM OR setup an account with an AI company and call their APIs you will realize it is just another tool to help you accomplish the job. At this end of this guide you shoudl have enough information to integrate AI. 

# Note On AI Personification

It is easier to personify and describe AI / LLMs as a they/them when talking about it. Note when such language is used it is not because AI / LLMs are alive or anywhere close to it, it is because as humans need a way to think about AI / LLMs and describe their interactions it is much easier language to consume. 

# What is AI / LLM Good At

AI / LLMs are really good at patterns, whether that is pattern recognition OR pattern recreation. Using all their training matierial or prompting matierial they can go through and, based on the guidelines you give it, develop a new pattern. These patterns are developed very fast and are usually very close to the end product you were looking for. Think the 80/20 rule. AI / LLMs are able to reliably produce the first 80% of a challenge you gave it. Sometimes the AI / LLM gets 'lucky' and is able to product 90% or even up to 100% of the solution you were looking for. This isn't enough certainty to blanketly use any result AI / LLMs give you, but it is enough to quickly accomplish a large task that is mostly repeatable off past problems. 

Think of two of the best uses of AI / LLMs right now: Code Completion and Email Composing. 

When you are typing code AI / LLMs can usually figure out with a comment or the start of a pattern a large chunk of what you are trying to accomplish. In general it is spot on and gest you that first 80% (or scaffolding) done. 

When it comes to emails AI / LLMs are very good at at correcting grammar and finding a pattern to present the idea you are trying to convey in a much more clear and consumable way. 

Where AI / LLMs also really shine is in being a Decision Support Engine.  AI / LLMs can get together large amounts of very disparate data from multiple sources and give you an inference that is 'probable'. From there a user can use their expertise to consume that data and then make their decision. 

Note that all these uses still involve a human at the end. This concept is called a "[Human In The Loop](https://en.wikipedia.org/wiki/Human-in-the-loop)". When used in this fashion and recognition the importance of augmenting human decision making AI / LLMs are very very useful!

# What is AI / LLM Not Good At

AI / LLMs are not good at creating discrete answers or solutions of which there is one solution. Because AI / LLMs answers are based off probability themselves their answers will ALWAYS vary and be different. When working in something like Arithmetic you do not want an answer that can possibly change. You want 1 + 1 to always equal 2. This type of discrete data you would create with other methods (machine learning, algorithms, human development), process, and then create data for an AI / LLM to consume. 

AI / LLMs should also not be used to make decisions on their own. When AI / LLMs are set to make their own autonomous decisions they will, by design, make errors. When these errors are made there is no ownership to that error, and there is no way to fix or correct this. There is no way for society to incensitve AI / LLMs from not making illegal decisions. It will make all decisions based off prompts and chance. This concept is called the [AI Accountability](https://aiethics.turing.ac.uk/modules/accountability/?modulepage=part-one-introduction-to-accountability).

**NOTE** I can concede there are some high levels of mathematics where answers do change depending on context and goals. Yes 1 + 1 can equal 3 for very large versions of 1. But that is rarely used in most bussinesses. 

# Decide What Challenge You Are Trying To Solve 

If you keep in mind what AI / LLMs are good at and what they are not good at you can begin integrating them into your business. 

Step 1 is deciding what challenge you are trying to solve. Using AI / LLMs for the sake of saying you have "AI" is going to provide low usability and cost you a lot of money. 

# Running AI / LLM Locally

# Calling AI / LLM APIs

The running of your own AI / LLM takes expertise and commitment to working with a new software stack. For many companies the smarter solution is to be able to offload the AI needs to a company with an available API. What is great is that with the IBM i and its built in functions to the database we are able to generate prompts and calls. 

LLMs are offered by many companies, and there are strengths and weaknesses to each. There is not one set answer to 'this one is better than this one', isntead you might need to test and figure out which one suits your needs best. Know they are constantly changing their models and what is the best today may not be the best tomorrow. Do not get too hung up on always using the latest and greatest model. Find a model that works well, and build your solutions off that. 

The good news is that calling these APIs works 'basically' the same for each LLM. 

For our tutorial we will use OpenAI. Visit the [OpenAI API](https://openai.com/api/) site and sign up for an account. 

Once you have an account you will want to create an [API key](https://platform.openai.com/api-keys). This secret key is what we will use to authenticate our request to our account at OpenAI (and the same concept applies to all LLMs). 


# About K3S (King III Solutions, Inc)

[K3S](https://k3s.com) is a software development company that specializes in inventory management and procurement solutions for the distribution industry. Their applications and solutions are developed to run on the IBM i OS (the best enterprise level OS!) and interface with any ERP application on any platform. 

As well K3S open sources many of its [Guides & Utilities ](https://technical.k3s.com/docs/utilities/) in an effort to improve the IBM i community. 
