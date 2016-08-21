# testing


###Siraj:
>Hi everyone, welcome to the Stack Share Tech Stack Podcast. I’m your host Siraj and I have with me the Stack Share CEO Yonas. In this episode we sat down with Jatinder Singh directory of engineering at HotelTonight. One of the world’s largest hotel apps with over fourteen million downloads. We talked about how engineers contribute new ideas, their iOS and Android teams, the first version of HotelTonight hint, it wasn’t native.




How they introduced global caching via Fastly and reduced the number of servers by 4x, how they run tests in containers, building a schemaless append only store on top of MySQL based on FriendFeed and Uber’s implementation plus much more. How are you doing today how’s life?


Jatinder:
Doing great, couldn’t be better just as the quarter is beginning a lot of things at HotelTonight that we are looking to get into, it couldn’t be better.


Siraj:
Awesome, do you have a routine you do every day in terms of waking up and just getting in the mood?


Jatinder:
Absolutely, I live in South Bay that’s roughly about an hour and fifteen minutes’ commute every day.


Siraj:
Is it car, is it train?


Jatinder:
I took the car train for roughly about a year and then I gave up.


Siraj:
You got to give up on that one.


Jatinder:
It is so unpredictable and it is so, like I had to go from my home to the car train station and then from car train station to San Francisco, San Francisco to the office. I was like, “No, this is not my cup of tea.”


Siraj:
I tried it for a week I was like, “No, I can’t do this.”


Jatinder:
Now with commuting what I typically do is I wake up super early and go to the gym in the city. HotelTonight provides a subsidized gym membership at Equinox which is right across.


Siraj:
Are you serious, Equinox?


Jatinder:
Yeah.


Siraj:
Nice, okay. I got to tell some of my engineering friends about this place. Equinox okay.


Jatinder:
That’s how I start my day and usually early and so the energy levels are up. The first thing that I typically do is look at the performance in New Relic. How was the day yesterday, what’s the response time, of our average response time, ninety-five percent response time of our key APIs. Also in the company there’s a single email that goes out to everyone in the company that’s like, “Hey, how did the company do, how did we do as a business?” Looking at that every day is reminder that we’re on a mission here.


Siraj:
Who sends that email?


Jatinder:
It’s an automated email, we use a tool called Looker. Looker is an analytical tool that you can use on top of databases like Redshift and you can send scheduled reports. One of that is scheduled every day.


Siraj:
From what I know about you and what you’ve said so far, it seems like you have a pretty good gig here. You got the equinox, you got the HotelTonight in San Francisco, short commute, all good things. What got you into computer science in general, what made you decide you wanted to be in programming?


Jatinder:
The programming world definitely excited me back in the day in the nineties, hooking into dial-up to connect internet and waiting for twenty minutes to hear a song or even more than that. Those are interesting times. It really fascinated me right from the beginning and pretty much after that on the side I started looking at actually, like C and Unix were the introduction to me.


Siraj:
C and Unix?


Jatinder:
I started playing around with C. Before C of course the whole about just seeing the transformation from DOS to different windows systems. It was fascinating back in the day. Now when I look I’m like, “What, what world did we live in?” Those were fascinating and then that took me on and just ever since I just took one step to another.


Siraj:
It’s always interesting to hear programmers talk about one of the first thing they worked on and usually there’s some amount of reference or like yeah and it’s still the best. I feel like you must feel differently now, you don’t feel as though C is the go to language these days.


Jatinder:
Absolutely I’m open to, I think there’s no one size fits all especially depending on the situation of the company, where they are. If they are just getting started C probably is not the right tool, not the right technology even at HotelTonight and some of the startups that I’ve worked for before.




Ruby on rails for example is a perfect fit for even when you’re getting started, but eventually you may run into very specific challenges. That’s where something like C could be really powerful or in these days it could be GO which could be really powerful. Depending on the job at hand pick the technology.


Siraj:
That makes sense depending on the job the different stack and speaking of job HotelTonight. Why HotelTonight because it seems like you have a lot of experience you could pretty much pick where you want to be and you chose this place?


Jatinder:
One of the things that I really like about HotelTonight is the open environment, it’s the influence and impact that engineers can make at HotelTonight to the entire business. Looking at that email like I said every day and then doing something about it and not just seeing that. That is something that I saw right from the get go. I’ve been in the consumer space for about ten years now. I’ve worked for a couple of startups before.


Siraj:
As a programmer?


Jatinder:
Before HotelTonight I was one of the founding engineers at a company called MUBI, I was one of the first engineers there. I realize that I worked there for about eight years. I realized …


Siraj:
That’s forever.


Jatinder:
Yeah exactly.


Siraj:
In programmer terms.


Jatinder:
I realized that there’s so much more to engineering than just writing code. I saw that when I looked at HotelTonight back then I saw this as another startup really. Which was not a startup in the sense of the numbers and the scale that this was running at, but in terms of how it was running inside, it was still pretty much a startup. People were really open, everyone had an opportunity to make an impact. That’s really why back then, this is about three years ago, I joined HotelTonight.


Siraj:
The openness is a major thing for you and interesting when it comes to engineering culture specifically, let’s say an engineer on your team has an idea for a feature. What does that process look like if he wants to implement it?


Jatinder:
Let’s say I have an idea, I had a number of ideas in the past year. The number one thing is how quickly can you demonstrate that idea has legs. There are two types of innovation. There’s the tech innovation that you can get into, where you’re improving the tools and technologies.




The other types of innovation is something that we need to also figure out how to make money out of them. Whether that’s a feature and how that feature fits in, you don’t want to end up with a patchwork where you have a thousand different ideas from different brains.




Coming back to the idea, proving out really quickly how that is actually going to help our customers. Customers on the mobile app side would be people who want to book rooms, hotel rooms on the supply side it’s the hotels. How can that idea, how does that work within the existing framework that we have? Which is we’re a mobile app, mobile only. We’re on iOS and Android and mobile web. If you look at our products very, very simple.




How do we keep that simplicity is one of the things that when you have an idea you have to figure that out? Spend some time quickly rapidly prototyping it and then get the stakeholders in, this is the product team and the other groups in the company. Then they could then formalize it if it’s actually something that we all believe that this is something we should get behind.




Then there are a number of ideas that we’re working on now which we’re … there’s one idea actually, if you have booked a hotel room using HotelTonight, the process is pretty simple. You look at a list of hotels, you tap into one of the hotels, you enter your payment information and then you book. This used to be the flow the first three months and then one of the engineers on the team was like, “There’s no wow, there’s no HT specific and this is a pretty regular flow that you would find on any other side or any other app.”




Now if you think about it, it will be counter intuitive to add another step to the flow of booking process, but what that engineer proposed was adding a H bed that you have to trace instead of pressing submit. You have to trace and H bed to confirm the booking. That’s an extra step.


Siraj:
You have to trace an H bed what did you say?


Jatinder:
There’s an H bed, our logo is H.


Siraj:
Okay got you.


Jatinder:
In the booking the final …


Siraj:
It’s something I don’t know about.


Jatinder:
The final screen, the final step now is to actually trace that bed, trace that H bed.


Yonas:
That’s live now?


Jatinder:
That’s live, that’s been live forever, this was really early days. Some of those ideas are engineering driven that we always look and encourage our teams to figure out how they can contribute.


Siraj:
Awesome, it seems like there this DIY culture where it’s like if you have an idea you just make it and if it works out, if it’s profitable it can happen?


Jatinder:
Yeah.


Siraj:
In terms of teams like engineering teams what is the structure here, do you guys have small teams, big teams? What does that engineering structure look like?


Jatinder:
We typically, we are strong believers in actually small teams. Whenever you’re working in a project we strongly believe that there should not be more than let’s say like six people, five or six people on that project. Those are feature teams that we form whenever we embark on a project. In terms of structure we have the team that I lead at HotelTonight it’s platform team.




Platform is the back-end infrastructure, APIs, any web-based products that we have this is the team that handles that. There’s a mobile team which includes iOS and Android and then there’s QA and the product team. This is within engineering and of course outside engineering you have supply, marketing, financing and so on.


Yonas:
How many engineers is it?


Jatinder:
We have roughly about forty engineers including mobile, QA platform.


Yonas:
What’s the biggest team out of that?


Jatinder:
Platform is one of the biggest teams. platform has roughly about fifteen folks now.


Yonas:
It’s nice even split between Android and iOS?


Jatinder:
Even split between Android and iOS.


Siraj:
What platform would you say gets the most attention dedicated to it these days iOS, Android, web out of those three?


Jatinder:
For us definitely iOS. That’s the platform that we actually started HotelTonight on back in end of 2010. We’re looking now, we’re always for opportunities or partnerships on Android as well as on mobile web. Mobile web just to give you a little bit of background, until last September or last August we launched a mobile web product to book hotels. Back then you could have only booked hotel rooms on iOS or Android App but after that you can now book on any mobile device but it’s still mobile only.


Siraj:
You were here for the launch of iOS initially or was that.


Jatinder:
That dates before me but I can give you a little bit of background there from the stories that I’ve had.


Siraj:
What was the MVP?


Jatinder:
It worked, it was the best decision back then. Within two months the team back then launched an app. One of the Appcelerators, Titanium is what they used and a lot of CoffeeScript to write it but within two months. The Rails back-end to like a hotel interface for hotels to manage the inventory and also for internal staff. Within two months they were able to launch it and go to market was really fast.




That was back then, that was the iOS app and Android they used back then they used HTML5 and jQuery straight up. Eventually over the next few years what we’ve done is we formed iOS and an Android team, really good experts and have converted those apps to native.


Siraj:
Awesome, that seems the way to go these days. Something that really interests me is like data storage and I know it can be different amongst your platforms, but how do you guys store your data?


Jatinder:
It has evolved over the years, back when we started it was a single MySQL database sitting on some EC2 instance but over the years it has evolved into. We still use MySQL that’s one of our go to storage platforms, but definitely have evolved into more partitioned and more [shattered 00:16:19] approach. Then other things that we use for storage are Elasticsearch, Veris, Memcached different types of storage. Some of them are persistent storage some of them are caches.




We use a lot of queuing systems so [INMQ 00:16:45] is one of our go-to tools for inter-service communication. For ETL we use for data warehousing and stuff we use Redshift and there are other databases that we use to pull scripts in some form for some of the geo-support that [inaudible 00:17:14] supports.


Siraj:
Got you, so you have multiple types?


Jatinder:
Multiple types year.


Yonas:
But primarily MySQL?


Jatinder:
MySQL is where most of the stuff started and like I said one of the things that we’ve been trying to, storage is one thing. Storing state is one thing that is challenging when you’re scaling. You can horizontally scale your app servers or web servers but storage is what ultimately gets you. That’s where we’ve been evolving our single database into removing single point of failures from our stack and one of them has been MySQL.


Siraj:
Now you guys just have multiple points of failure that was good. That’s awesome though that you guys have specialized data storage for different things. Usually it’s like one or the other. What back-end languages do you use to deal with the storage and retrieval?


Jatinder:
Ruby on rails is one of the platforms that we are heavily invested in. That’s how we wrote our first app back in 2010.


Yonas:
The first app for the Appcelerator?


Jatinder:
The back-end for the APIs and the hotel interface that we built. Overtime we have evolved that into more Rails apps and also recently we’ve also looking at GO and tiny services to glue. You have to get information from one place to another, instead of putting that code in the monolith that we have been trying to break apart. Why don’t we try something like GO? Node.js is another platform for mobile web that I mentioned about it. Node.js is another platform that we started investing in.


Yonas:
What percentage of the code base would you say is Ruby?


Jatinder:
I would say it’s at least 80%.


Yonas:
All the API is all Ruby?


Jatinder:
Yeah.


Yonas:
Objective C and Java?


Jatinder:
Objective C, React, the mobile web app again and also the interface that we have for hotels. That app uses React.


Yonas:
You have a different app for the hotels?


Jatinder:
Yeah we don’t have …


Yonas:
Hotel management?


Jatinder:
When I say app it’s really a desktop and mobile web app not a native app, but that and the mobile web app for the consumers that uses React and a combination of Node and Rails.


Siraj:
What do you think of GO. I really like Go, are you a fan?


Jatinder:
Again going back to the point about right tool for the right job. It could excel in a lot of things but if you’re trying to write a [crowd 00:20:25] app that’s not where I would go.


Siraj:
You simply stick to JavaScript.


Jatinder:
Stick to something like Rails for a simple app and Go would be good for just you have a very specific need or you’re having a very specific. You want to get data from one place to another and you want something really fast. You don’t want things like garbage collection to come in the way or multiple layers of framework to get in the way. That’s where you want to get down to something like GO.


Siraj:
I like how detailed you are when you think about partitioning different problems and using technologies for that specific problem. Is there like a really hard engineering problem that you solved recently or that really just people were up late doing?


Jatinder:
There are a couple engineering problems that I can talk about. Let me set the context for the first one first. Back in 2014 we used to be a same day booking service for booking hotels. As a customer you could only book hotels the same day, you could not book in advance. What HotelTonight would do is we would send a push notification at 9:00 am to all our customers.




It’s a self-inflicted DDOS. Now suddenly at 9:00 am you see such a spike of traffic, customers trying to come to the app and trying to see what’s available. That was really interesting because that actually put a lot of pressure on the database and there was very limited caching that we did back then.


Yonas:
Because of the actual push notification or because they were actually starting to use the app?


Jatinder:
All of them were trying to come to the app at the same time because of that push notification. We don’t have one specific algorithms for all the customers. We have various number of factors, different number of factors and the algorithm to choose, to figure out what hotels do we show to a user. We don’t show hundreds of choices to the customer, we show them only 15 hotels.




Location is one of the very important aspects of the context for the customer. If a user is opening the app from LA versus San Francisco they’re going to see different results. What that means is the API powering that has limited cache ability. That was an interesting challenge. There were these big days like July 4th, Memorial weekend where people would be opening the app, way more people would be opening the app at the same time right.




That was an interesting challenge, what we did back then was we introduced a service called Fastly, we started using them. There are some APIs that cannot be cached for Rail on time but we did was we started caching for example one of these APIs that powers the hotel list for a very limited time. Also the caching was based on where the user was.


Yonas:
You could do geo-location?


Jatinder:
Yes.


Yonas:
Geo-based caching with Fastly?


Jatinder:
Yes, we’re huge fans of Fastly. I’ve used one straight up in the past. The amount of hash power it gives you, its edge caching is just like that’s where you should stop. If you can solve a problem by introducing something like Vanish you should absolutely use it. Re-counting our experiences from back in that time there were other APIs which could be cached way more aggressively. I remember when we introduced Fastly we cut down our servers by like 3x or 4x just by introducing Fastly.


Yonas:
Response time?


Jatinder:
No, the number of app servers. The response time it went, Fastly responds within depending on the payload size of course. I’ve seen responses in forty milliseconds, thirty milliseconds or fifty depending on where the user is too. They have an edge, the network of nodes which pretty much coincides with where our customers are. On the other hand, like APIs that a request has to go through entire stack. It has to go through all the load balances, rails, all the databases. It cuts all that.


Yonas:
Where is the core app posted, AWS?


Jatinder:
We recently moved to AWS straight up. We used to use a service called, a platform there’s a service called Engine Yard.


Yonas:
Engine Yard?


Jatinder:
Roughly about I think this year, earlier this year we started. We have been using AWS for a long time but for the web containers and for the background containers we moved to AWS. Started using ECS Elastic Container Service.


Siraj:
Elastic Beanstalk right?


Jatinder:
Not Beanstalk ECS is more you can Dockerize.


Yonas:
Container management.


Jatinder:
Container management like you can Dockerize, we’ve Dockerize our app.


Siraj:
You guys use Docker?


Jatinder:
Yeah, we’ve Dockerized our app and use ECS such as like a scheduling service for containers. That transition has been pretty good too.


Yonas:
We’ll have to circle back to that, that sounds interesting. Coming back to Fastly right you were reducing the number of service on Engine Yard. When you introduce it?


Jatinder:
Yes.


Yonas:
How did you find out about Fastly and how did that decision come about, what was that process like?


Jatinder:
It was not a hard process, like we had been a huge number of fans in the engineering team of Vanish. We had seen the power of Vanish. On the other hand, we had been trying to get away from self-hosting tools for example MySQL, we used to host it on EC2 instance. We moved away from that and started using RDS, similarly we were looking for a service for Vanish. Is there anything out there which provides Vanish as a service? Fastly was the name, we started looking around.


Yonas:
Started googling, started stack share and then?


Jatinder:
For sure.


Yonas:
Were there already folks internally that had already heard of Fastly and were saying, “We should go Fastly,” or did consider other options?


Jatinder:
We stopped and Fastly, there was some discussion on CloudFlare. There were some common friends too at Fastly and then what typically when we’re evaluating tools it just goes back to the question about, if you have an idea how do you go about it? Just let’s prove it out like sign a free trial and see what works. With Fastly it was so simple, all we had to do was change out route 53 DNS to point to Fastly and change how would TTL, specify TTL or cache header on our responses. That’s it and it was like up and running within a few days.


Yonas:
You started routing some of the requests, you didn’t do automatic or like overnight?


Jatinder:
That’s right, we started rolling out some of the less critical traffic first to make sure that everything was working fine. Then overtime it has become one of our go-to tools.


Yonas:
You mentioned a couple of challenges …


Jatinder:
There’s only so much you can cache. We solved the 9:00 am problem by making sure we’re caching aggressively during that 9:00 am but you cannot cache for a long time. Especially the hotel list, something like hotel list because prices. The business that we’re in people come to us to look for hotels at the last minute. The last minute hotels are changing their price and allotment all the time, it’s changing every minute.




That means that we can only cache so much. Then we started looking at what was the bottleneck in the stack that was the reason for not being able to scale. One of the bottlenecks was MySQL. When a customer would come in, we would basically let’s say the [movement 00:30:43] of inventory that occurs in our database will run a geo-query on top of that and try to pick the fifteen best hotels out of that, millions of records.


Siraj:
Why the fifteen?


Jatinder:
Why the fifteen? We believe that choice should be limited for the customer. Just by showing them the best 15 hotels make it easy for them.


Siraj:
I like it.


Jatinder:
We basically also make sure that there are different variety of hotels, different neighborhoods and a lot that goes into algo right. That we used to do some of that in MySQL and a lot of that in Ruby and it would take, like that was a bottleneck. The MySQL was becoming a bottleneck.




We started looking around at different technologies, Elasticsearch came to our attention. A lot of people had been fan of other technologies like Solar and so on but just you’ve seen for ranking hotels seemed like interesting idea. We explored that and then now we have that into our stack, now we have Elasticsearch into our stack.


Yonas:
You’re hosting it yourself?


Jatinder:
Yeah, we use Found for hosting Elasticsearch. One of the things I want to mention there is the combination of Ruby and MySQL the same like picking up the fifteen best hotels. That used to take depending on where the customer is, deepening on the supply level. It would take anywhere from five hundred milliseconds to one second.


Yonas:
It’s going through active record right?


Jatinder:
It was going through the ORM for sure and then MySQL and then post-processing and a lot of post-processing in Ruby to mix and match the hotels. A lot of that with Elasticsearch, the same thing that we did in Ruby and MySQL now takes fifteen milliseconds with Elasticsearch.


Siraj:
Incredible.


Jatinder:
That was one of the interesting challenges. I can go and on about Elasticsearch because then we discovered another problem with Elasticsearch but like, “Okay so this is great, this is are we done here?”


Yonas:
There was a problem [inaudible 00:33:16].


Jatinder:
The next thing was it turns out this is on the consumer side, a lot of consumers are coming in and trying to see the list of hotels, but now on the hotel side we’ve worked with a lot of hotels that are changing their availability and rates very often. What would happen is now the data has to propagate from MySQL to Elasticsearch.


Yonas:
By the way they’re inputting that data, you’re not scraping or anything?


Jatinder:
No, they’re inputting that data, we also directly connect with them. It’s also like APIs that we work with. That means the data is changing a lot of times and that has to propagate to all the storage systems including Elasticsearch. That’s a really light-heavy load that we have for Elasticsearch.




Something that typical Elasticsearch usage is around logs and analysis. This was unlike that, this was the number of documents may not be that large but the fact that they’re changing all the time introduced a number of things, a number of behaviors that we were not aware off when we started using Elasticsearch.




Elasticsearch would drop some of the rights silently. If you used one of the APIs got bulk update, you can watch for those errors back then we were like, “It’s going to scale, Elasticsearch scales right?” Then we discovered now we make sure that we throttle the rights. We have a queue sitting in between Elasticsearch and our systems.


Yonas:
What’s the queue rabbit or?


Jatinder:
INMQ.


Yonas:
INMQ yeah the hosted service.


Jatinder:
INMQ is what.


Siraj:
It would just know when it needs to be used or is there a human behind it, like an engineer who’s watching and waiting?


Jatinder:
We also have a lot of monitoring built into these queuing systems and pretty much all the systems, we use Datadog for a lot of metrics on all these services. If the number of messages in that queue has gone beyond a certain threshold, then alert the person on call.


Yonas:
Datadog is sort of like your dashboard right?


Jatinder:
More than dashboard, dashboards are fun to look at but a lot of times you don’t get meaningful insights out of them or actionable insights out of that, action is the key. Allotting is where Datadog really excels for us. We’ve set alerts for all our systems like [inaudible 00:36:19] starting from load balances to all the databases, to all the caches. We have checks and balances to make sure that the on call person is alerted. If for example the CPU of the RDS database goes beyond a certain limit.


Yonas:
Got you, awesome. Go ahead.


Siraj:
Cool.


Yonas:
So much more to talk about.


Siraj:
There’s so much more to talk about, there’s so many questions I have for you, but I know your time is limited and we want to wrap this up. From what you’ve said about HotelTonight it seems like a very cool culture and some place that like if I were applying for jobs I would apply.




One thought I had was about the industry in general. There’s a sharing economy in Airbnb and all these sharing services. What do you see is the future of the accommodation industry or like hotels? Do you think people will continue to want hotels or do you think it’s going to move this way or that way, what’s your take on it?


Jatinder:
There are different use cases depending on where the customer is in their lifecycle. If you’re going on a vacation, if you’re with your family and planning your vacation a year in advance then, I think some of the accommodation services like Airbnb excels. A lot of other use cases if you want to be spontaneous, if you’re on the go like me.




I’m travelling a lot of times from South Bay to San Francisco at 6:00 pm I’m like, “Hey should I just called it a night here or should I actually extend my night and book a hotel room here and go back tomorrow?” There’s a lot of those serendipitous experiences that HotelTonight unlocks and that’s a use case as the millennial general with the advent of [inaudible 00:38:09], with the mobile phones. We’re just getting started.




A number of, I don’t have the exact stat, but I think the last minute space for hotel bookings is something that has been growing compared to the week off or compared to the month off or compare to the year in advance.  That’s something that we are excited to see and figure out how can we make it easier for customers and hotels to unlock really new experiences then.


Yonas:
It sounds like a lot of the tooling is enabling you to have the approach right?


Jatinder:
Exactly.


Yonas:
Where you can say we don’t need someone that’s just DevOps and can work with Docker, but a lot of the tooling sounds like it’s helping with that right?


Jatinder:
Absolutely.


Yonas:
Like ECS?


Jatinder:
Absolutely, ECS makes it super simple and we use Terraform on top of [temperetising 00:39:25] our legs, infrastructure as a code really. All of us can read what the infrastructure looks like and that back in the day we were like there were a bunch of systems in place and there was very little documentation about that and now the infrastructure as it goes like the Terraform just look at them. There’s a lot of innovation happening in that space, there are a lot of cool things happening in this space.


Yonas:
You guys use CloudFormation at all?


Jatinder:
We don’t use CloudFormation, terraform is really our leg. It pretty much provisions everything, all the dependencies that we have, all the elastic cache, the dependencies, RDS and so on. It’s great we also have multiple staging environments where it’s pretty much the same recipe that we can just get bend up and down, spin these new environments up and down.


Yonas:
On AWS?


Jatinder:
Yeah.


Yonas:
What is your build, test, deploy flow look like? Is everyone using Docker locally?


Jatinder:
Not at this point, some of them are but that’s one of the things that we’re looking to evaluate next.


Yonas:
Are you using Docker personally?


Jatinder:
Yeah, yeah.


Yonas:
You are?


Jatinder:
Yeah, again there are certain dependencies. What we’re trying to figure out as we are growing the number of services that we have, how do we extract out the interfaces to external services. That’s one of things that we’re looking at. One of the other things that I wanted to talk about, I lost my train of thought there.


Yonas:
Is it related to build, test, deploy.


Jatinder:
Build, test, deploy yes. Our typical workflow is this right. We use Solano, as soon as you check in something, as soon as you create a PR or create a branch really. It goes through Solano and make sure everything is actually cool …


Yonas:
Solano CI.


Jatinder:
Solano CI yes, Circle CI in the same space. All the tests pass and make sure that data within few minutes rather than thirty, forty minutes. That’s where [inaudible 00:41:41] Solano or Solano or something like Solano CI comes.


Yonas:
Get up to Solano and then.


Jatinder:
The build runs in Solano and then depending on the feature or the level of testing that is needed it goes out to the staging there’s auto deploys. You create a PR, tests run on Solano, there are other folks on the team review your PR and then you merge that PR to master it and then Solano or Jenkins in combination with Solano deploy to staging cluster.




That’s when we do depending on the feature, we do some sort of testing, some of sort of manual testing to QA. Then we get it out to production. We deploy multiple times a day. This one we haven’t added the continuous delivery system but that’s intentional. We want to make sure that the quality of, we want to QA allot number of cases to approve some of the changes that we’ve made. Smaller changes usually they just go out multiple times a day.


Yonas:
How does Docker fit into the flow there? I guess once you push it up to get out then it’s going out to, it’s been containerized and then pushed into Solano?


Jatinder:
It’s being containerized and we use Jenkins.


Yonas:
[crosstalk 00:43:16].


Jatinder:
I could be wrong there, AWS one of the services that they provide …


Yonas:
Through ECS maybe.


Jatinder:
… solution through ECS that we started using instead of Docker Hub, but the team was going back and forth there. We use Jenkins and create those Docker bills and create the images that we need with ECS and then ECS, all those tasks definitions that we have defined finally gets out. The deploy time it’s a couple of minutes now to do a deploy for …


Yonas:
The runs you test that quickly?


Jatinder:
No.


Yonas:
You’re talking pre?


Jatinder:
Solano has already run so this is pretty much once the image has been built like getting that out to all the servers. That’s sort of our build …


Siraj:
You build pipeline.


Yonas:
How long do the tests take to run, I’m just curious?


Jatinder:
If you run it locally it’s going to take a while. That was one of the things that we started exploring a couple of years now. Through CI and Solano and last that I ran I remember running test on Solano it takes four and a half minutes.


Yonas:
It’s pretty good.


Jatinder:
We still have a monolith that we’re trying to get away from.


Yonas:
As far as platform is concerned


Jatinder:
As far as platform is concerned and that’s going really well, just looking at a different thing that we can extract out, encapsulate in a different service.


Yonas:
Does mobile have a different sort of process there in terms build and deploy? Knowing the platform like iOS specifically the approval cycle of once you submit an app. We typically every two weeks we try to get something out. A new release and hot fixes of course as soon as we discover something.




That’s typically how we like to have a regular cadence on getting a release out on those platforms, not feature driven releases. It’s more sort of a release stream that we have, we get something out quickly. Sorry there’s some folks waiting out.


Jatinder:
Let me see here. Let me quickly check with these guys.


Siraj:
Okay.


Jatinder:
I think it’s 2:15.


Jatinder:
We’ve recently re-branded some of the conference rooms so people had booked the older version of this and I had booked the newer version of this, the new name of it so that’s why.


Yonas:
You need to update the [crosstalk 00:46:57].


Jatinder:
One of the things that I didn’t touch upon going back to challenges was this. We solved the customer side by introducing caching and moving to Elasticsearch and also rights that were happening to Elasticsearch. Remember when all those hotels are changing their rates and availability, all those were still going to a single database.




There was a hot spot there. That was one of the places where we looked at some of the solutions out there on how different companies are doing it. We built a schemaless, append only store on top of MySQL, pretty much on the lines of what FriendFeed. There’s a pretty good blog post by the FriendFeed guy and this is like 2009.




Then Uber recently also have moved to the same model, schemaless append only store. That allows us to horizontally just have more partitions and [shots 00:48:19] and also just have it schemaless. We don’t have to go and change schemaless and append only is the key. Just storing different version of the same room or same inventory.


Yonas:
You’re not overwriting?


Jatinder:
You’re not overwriting a single row, you’re basically creating different versions of it and then schemaless because there’s stuff changing all the time. You don’t have to go and change, you don’t have to run online schema changes. That we’re a huge fan of like the PT-OSC but not in this context. I don’t know if you’re, Percona online tools. Let’s say like going down, having a downtime is not acceptable or we tried to minimize the downtime especially expected downtime that would be, that’s a no, no, no.




We used to have a lot of changes that we have to go and add a new column to our database or delete a column not delete a column but do something to a column to our database table. There are a number of weird issues that you can run into when you’re doing that. If you’re not suing something like online schema change.




Recently POST ways and MySQL the latest versions of them have tried to solve that so that you’re not going to lock the entire table, you’re not going to lock depending on like … you’re not going to lock rows when you’re doing that. The other solution is using something like PT-OSC and that has helped. That’s our work flow so any migration that we have, any database migration that we have we ran that using the Percona online.


Yonas:
There’s no downtime and no issues?


Jatinder:
That’s right.


Yonas:
Prior to that did you guys have issues like you’d have to plan downtime?


Jatinder:
Yeah, of course. We had not planned, we would think that this alter statement is not going to create any lock and when we ran that just hell broke loose. All those surprises we moved away from by introducing PT-OSC.


Yonas:
It’s awesome.


Siraj:
That’s very cool.


Yonas:
I guess we still have a few minutes. Any other tooling and things that have been helpful? I guess we don’t have touch too much on the mobile side because you’re on platform. Some of the issues, there’s a lot of talk of some issues with Ruby specifically. Are you guys thinking about, I know you mentioned GO but are you think Elixir, are you guys looking at any other new technologies or have you guys had success with Ruby and you’re able to have it perform at a high level?


Jatinder:
Ruby is performing pretty well for us. There’s some use cases that’s where GO is something that people have started looking at. There are lot of Ruby enthusiasts in the house including me who’s been in the Ruby community since 2006. Elixir is one of the things that a lot of Ruby community is going into. There are lot of people on the team who are exploring Elixir.


Yonas:
Are you a fan of it? Have you played around with it?


Jatinder:
I haven’t played around with it.


Yonas:
You’re happy with Ruby?


Jatinder:
I am happy with ruby well at the same time my schedule is not even, I would not even say fifty-fifty between coding and managing. It’s even more on the managing side now. Just making sure the team culture and projects getting done. Infrastructure really excites me, it excites me more. Like I said scaling especially on the storage systems, you can scale Ruby, you can add more web servers but scaling a state is really challenging.


Yonas:
It sounds like a lot of the issues that you have are because of the fact that there’s a lot of rights on the supplier side but I guess on the customer’s side you don’t have those sorts of issues?


Jatinder:
Not a lot of them but we moved away from the call back hell that people would run into in the Rails models.


Yonas:
Going through save.


Jatinder:
After save and there was a long list of those call backs in some the Rails, models that we had. We moved away from that and started backgrounding them as much as we can.


Yonas:
Just a bunch of rate test.


Jatinder:
Not rate test but using something like Sidekiq just add that to the queue somewhere.


Yonas:
Right, queuing it yeah.


Jatinder:
Queuing it offline and the next step there that we’ve started looking into is event streaming. What would happen is let’s say a customer changed one of their attributes and now the rest of the systems need to know about that change. Previously we would have the first night of implementation of that is you have like five or ten different call backs which do the same thing.




The other way to look at that is like producer and consumer. Producer is going to produce that, put it into a cube like Kinesis or Kafka and then all the consumers in the world are going to consume that and take an action on that trigger. That’s the model that we’re moving into. Conceptually it’s just easier to understand what’s going on in the system.


Yonas:
That means you have one central place where you can see everything that’s happening?


Jatinder:
Right.


Yonas:
You’re now introducing Kafka or you’ve had that already?


Jatinder:
We’re actually evaluating Kafka and Kinesis right now. Kinesis is something that the team, again it’s a service by AWS. You don’t have to worry about some of the hosting challenges that you have to take on with Kafka.




At the same time, we’re trying to compare what are the edge cases that we’ll run into both Kinesis and Kafka. Taking that call and then deciding whether should we use Kinesis or should we self-host Kafka and go off with that. Heroku recently launched Kafka as a servicer that’s one of the things that we’re also looking into.


Yonas:
Awesome, cool, I think now we’ve gone through everything right?


Siraj:
Cool.


Yonas:
That’s awesome, Looker is helpful for you all?


Jatinder:
Looker has been very helpful, yeah for sure. How do we democratize like we have so much data? How do we have access to that, how do we have no just me. I can go and run SQL queries. The rest of the team, rest of the company needs easy access and Looker is one of those tools that is designed to do that.


Yonas:
One thing that popped into my mind as you’ve described the notification, the push notifications in 9:00 am. Can you just briefly describe what happens if let’s say a server goes down in the middle of the night. What’s the flow, are you guys using PagerDuty to get like a text message?


Jatinder:
We have the platform team, each member on the platform team goes on call for a week. There’s a primary and there is a secondary. The primary gets paged whatever time it is and then and if they don’t answer then it goes to secondary and then I am at the third level. I’m also on the rotation every fourteenth or fifteenth week, but I’m also as the third level of like if there’s no one on the call answering then I get on.


Yonas:
You get like a text and then a call?


Jatinder:
Depending on the notification settings we definitely want people to get a call rather than a text and depending on the nature of the problem too. If there’s an alert from database, then better look at.


Yonas:
That’s a call?


Jatinder:
Right, that’s a call. We’ve been trying our best to also reduce the noise there through spurious alerts.


Yonas:
Now that’s PagerDuty?


Jatinder:
All the noise, yeah. Just making sure that only high alert, critical calls are getting paged. The next step that we’re looking at is how can we take alerting to the next level, not just alerting but actually figuring out a way to fix that problem right then and there. For example, let’s say a queuing system is backed up can we spin up more workers on the fly to actually help with that like than having the on call person do that.


Yonas:
With no intervention, interesting.


Jatinder:
That one needs to be done carefully because you don’t want to have spin up a bunch of more workers which ends up bringing down your database.


Siraj:
It sounds like this could be a machine learning problem.


Jatinder:
Anomaly detection is one of the things that machine learning, a lot of company are using it. Sumo Logic was one of the company that was showing that they came onsite a few weeks ago and they were like, “These are the …” Some of the tools that seemed really interesting.


Siraj:
Just a parting question. What’s something that excites you or something that you’re looking forward to. It could be technical or it could just be like life in general like, “I have a dog that I’m going to buy or something.” Something in the next day or next week or maybe even next month.


Jatinder:
Personally I like really scaling. I get high when I’m working on a problem which is around scaling. Which it could be a storage system or just scaling to the number of users. Growth and really I’ve asked that question to myself, what excites me. Scaling a company is very actually what really excites me underneath.




Growing the customer base, how to retain users. You could be doing hundred thousand RPMs but if your users are not sticky. Retention is another like key. A combination of both business and as less technical is what excites me.


Siraj:
Awesome, well thanks so much Jatinder it’s been amazing.


Yonas:
Thanks a lot.


Jatinder:
Thank you guys.


Siraj:
All right cool.



