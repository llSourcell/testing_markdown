#FlexPort Interview

Siraj:
>Hi, everyone. Welcome to the StackShare Tech Stack Podcast. I'm your host Siraj and I have with the me the StackShare CEO, Yonas. In this episode, we sat down with Desmond Brand an engineering manager, Amos Elliston the CTO, and Evie Gilly another engineering manager at FlexPort; the worlds largest freight forwarding logistics software provider. We talked about how FlexPort first started, and what the MVP looked like. We also talked about all of the issues they faced when it comes to logistics and dealing with multiple very large clients.


>We dove into how their Tech Stack filters out the unnecessary data and helps the team provide the most sufficient transit data when they need it. Desmond is an expert in React, so we talked about that for a bit. Then we talked about how engineering ideas are surfaced and later implemented on the team.

Amos :
>Hi I'm Amos Elliston. I am the CTO of FlexPort.

Evie:
>I'm Evie Gilly. I was engineer number three.

Desmond:
>I'm Desmond Brand. I don't know what number engineer I am, but I've been here for about a year.

Siraj:
>Awesome. Thanks guys. I just wanted to start off with, what is FlexPort in your own words? When I saw it, I thought that freight shipments that's not that sexy, but it must be.

Amos :
>Yeah. I guess we are known as boring un-sexy startup, which I take offense to, but I can see from the outside why it is that. I think it's really sexy.

Evie:
>I don't think they're talking about us Paige.

Amos :
>Yeah exactly. I think it's only about shipping but, attractiveness we're really good. FlexPort is an international freight forwarder and customs brokerage. That means we move goods usually over 150 kilograms in weight from one country to another. 150 kilograms is interesting because it's the size of freight that's too big to fill into a UPS or FedEx network, so you need someone like us to make sure it from a factory in China to the US. We are like travel agents for freight which is a little sexier because travel agents...

Evie:
>Yeah.

Amos :
>Used to be sexy.

Yonas:
>Logistics is sexy in general.

Amos :
>Isn't logistics sexy?

Siraj:
>It is.

Evie:
>I think so.

Amos :
>I think so.

Yonas:
>It's deep tech. We're going to get into it, but it is super sexy.

Desmond:
>The thing I think about that's cool is the way we look at the product. Freight forwarding is an information problem. We get information in about what needs to move. We give information out about what trucker to pick up something where and drop it off at this port, etc. Everyone just throws bodies at the problem, but we use information technology to solve an information problem. I don't know if that's actually supposed to be novel but it feels like it is in this industry.

Amos :
>Yeah. You're moving tons with software. That's pretty cool.

Evie:
>My dad tried to ship a container full of equipment a couple of years ago, and it was like he could track his Domino's pizza way better than he could track his multi-thousand dollar business shipment.

Amos :
>Domino's is pretty important though.

Evie:
>Yeah.

Amos :
>If we get to the level of Domino's, we have made it.

Siraj:
>Okay so Domino's is the next step. Okay. That's V2.0. Cool. We are really interested in your engineering culture and the kind of team that you guys want to build here. Just right off the bat, how would you describe the engineering culture here at FlexPort?

Yonas:
>Maybe also your roles, your respective roles.

Amos :
>I think have already said it, We're attractive and hilarious. Beyond that.

Evie:
>You can't see it in the interview.

Siraj:
>And humble.

Amos :
>And humble. Clearly some of us are humble. Technically we have a pretty high bar. I think everyone says that. We believe it, and we're all really committed to working together to try to build this thing in a very collaborative environment.

Evie:
>We are fortunate to have the people who are the real power users of our product; the people running the shipments sitting 20 feet away from us.

Yonas:
>>Really. Wow.

Evie:
>If you think of the travel agent of the shipment, the person handling all the handouts and making sure everything's going okay, those are the operations people who sit on the same floor. If an engineer is building product and they don't know what it should look like or what they're even doing because a lot of the engineers are new to the freight space in general. They'll go and be like, "Phoebe what is this supposed to do?"

Siraj:
>That must be nice, that instant feedback.

Evie:
>The iteration loop is super tight.

Siraj:
>Super tight? Okay. Cool.

Yonas:
>Just as far as roles, you're just overseeing everything tech-related.

Amos :
>Yeah. I am the CTO, oversee tech and product as well. I make sure we get everything out the door on time, quickly, and well. Quality, very important.

Desmond:
>I'm and engineering manager, and I guess I am focused a little bit on the front end kind of stuff, and the bugs process as well.

Evie:
>Also, engineering manger more toward the backend.

Siraj:
>Back end? Okay.

Yonas:
>You guys collaborate quite often?

Amos :
>Yep.

Evie:
>In theory, yeah.

Amos :
>Sometimes the backend talks to the front end.

Siraj:
>Okay cool. If I heard correctly, you are a React expert. Is that a valid moniker?

Desmond:
>I guess one person did say that, but that's just one person. Our front-end stackers React, it's been like that since before I joined which is pretty cool. I think historically the app was a Rails app, and it migrated to a completely powered by React application. We use all of the Javascript Fatigue stuff like Webpack, ES6. We use f.lux, it's a little bit of a custom f.lux thing. Apple app is a React. There's actually a few different apps. That one that we talked about before, where the operations people in this building use it. There's also another app which is the one that the clients log into. They're independent applications on the front-end. They share some components and stuff.

Yonas:
>We'll circle back to the stack in details.

Desmond:
>Sure.

Siraj:
>I think that's pretty cool that your guys have migrated from Rails to something completely different. When you come in to work what is that bigger vision that you have? What is that goal?

Desmond:
>Yeah, good question. We set goals on a quarterly bases. We have some big pieces of product that we're trying to build in the next 90 days. Some of those right now that happening, we need to get bookings which is this thing that will generate a bunch of shipments happening. As we grow we also need to lock down some of our sites. We're doing this permissions project.


>On the technical side, we have some things going on in the front-end, that I think will make it more difficult to collaborate when we have more engineers. I'm trying to get ahead of that and set some better practices. One thing I'm experimenting with now is replacing some our f.lux stores with GraphQL and Relay in the hope that we're going to have a little bit more of a scalable system if that turns out to work. There's a lot of different things that are on my mind for the long term. That's some of them.

Evie:
>Super excited about GraphQL and Relay.

Desmond:
>Yeah.

Yonas:
>Okay, we're going to have to get into that.

Siraj:
>I'm just waiting to dive in. Maybe we could just talk about how FlexPort started? What was the motivation? Where did the idea come from?

Amos :
>Sure. It started with our founder Ryan. He had been doing import export for 15 years. He used to import ATBs and walk in bathtubs which are these bathtubs for old people so they have doors on them. You get in, close it, fill up the tub. They're pretty sweet. I kind of want one for my house.

Siraj:
>What am I doing stepping over stuff?

Amos :
>That's like a totally unnecessary step. There's a little door.

Siraj:
>Like an automated voice, "Please step in. Wash yourself immediately."

Amos :
>Yes. I don't know if they're automated. Also I think they sold in room saunas. Ones that you could be for $5,000 and get installed in your house. Some random stuff. He used freight forwarders and customs brokers that were terrible. They didn't even have a website. He showed us some of these things. It's literally like they just discovered the blink tag situation. He was like, "God. There's got to be something better. I bet I can build it." He started a customs brokers. Did YC Batch 2014 Winter or something like that. His original app was done by some people in the Philippines so that was Rails.

Siraj:
>That was Rails then?

Amos :
>Yeah. That was the reason we picked Rails because that existed when I came to the come which was right after YC. Don't worry we rewrote the whole thing. There's no consultant code in there. Git-blame is gone. It's all well thought out code now.

Siraj:
>Right. Were you in Rails before? Had you dealt with Rails prior to coming to FlexPort?

Amos :
>Yeah so 2006 I helped start a company Genie. We were a genealogy. It's like do your social family tree.

Siraj:
>Ancestry?

Amos :
>Yes. We were trying to be Facebook for families. We also spun out Yammer which was Rails stack way back in the day. Yammer started 2007 on Rails.

Siraj:
>Yammer spun out of that company?

Amos :
>Yeah. Yammer started with Rails 2.1. We actually started basically right when git had launched so we used git which was pretty advanced at the time. Git was like the Flow of it's day.

Siraj:
>There was no distinction between git and [crosstalk 00:09:54].

Amos :
>I don't know what it would be like the Flow or the GraphQL of it's day. We used that. We used Rails 2.2, 2.3 maybe, which was very cutting edge. I have lots of, lots of experience with it. Now some of my experience is very dated. I think they've moved on.

Evie:
>We smile and nod.

Amos :
>I'm a little old school. If I was going to start another company it was just there. I don't know if I would've picked it to be honest.

Siraj:
>Really?

Amos :
>Yeah.

Siraj:
>Why?

Amos :
>I don't know. It's an interesting choice. It's showing it's age a little bit and there's some other interesting frameworks out there. I don't even know what I would be chosen. We talk about this all time. Would we have done Node? Would we have done Java? Would we have done Scala? It's a discussion we have a lot.

Siraj:
>You'd just have to go to StackShare and see what [crosstalk 00:10:47].

Amos :
>I'm always curious about what are all the kids doing nowadays. What's the hotness?

Siraj:
>The hot company's Node.

Amos :
>Is it Node?

Evie:
>There's Python-

Siraj:
>Node is pretty popular these days.

Amos :
>Yeah?

Siraj:
>Yeah. Node, React. Javascript is-

Yonas:
>GO.

Evie:
>Go is big.

Amos :
>Yeah, we talked about that. I still really do like Rails.

Siraj:
>Okay so you're still a Rails fan. Do you have other Rails fans in here? No?

Evie:
>I came in a skeptic but I'm kind of a fan now. There's just been so many moments when I need to do something and there's already 5 gems.

Siraj:
>That's one of the biggest advantages is everything has been done for you.

Amos :
>Yeah. She misses all the typing in Java. Her hands feel really-

Evie:
>That's all it took to make a HashMap? That doesn't feel right.

Amos :
>At least 15 lines to open a file.

Siraj:
>Was it just basic functionality like you could get freight container from A to B and that was it?

Amos :
>It was pretty much just a database of this is what's happening right now. The basic functionality was almost database admin interface. It'd be like hey here are all our shipments which is represented like 4 or 5 tables in our database so it was very bare bones.

Evie:
>Quoting was in Excel.

Amos :
>Quoting was in Excel. That was probably our first real big feature. We took an Excel spreadsheet that was mind-blowingly complicated, like Excel on steroids and then made it an app which increased the ability for us to quote. We went from 5 hours down to 2 minutes so it was a really big win.

Desmond:
>Didn't people also used to track shipments in Trello instead of the app?

Amos :
>They used to track shipments in Trello so our app we built a Trello killer which was great.

Yonas:
>Wait. Oh, you mean internally?

Amos :
>Internally right. It was for our workflow.

Siraj:
>I was like wait they know about Trello?

Amos :
>I'm not saying it's a Trello killer.

Siraj:
>Okay.

Amos :
>It was a Trello killer for our workflow and we killed it successfully. They were much happier than the were when they were using Trello.

Siraj:
>Got you. Maybe you could just walk us through the entire experience. You're dealing with all these folks that want to be able to move containers across the country. Right?

Amos :
>Yes.

Siraj:
>They're looking for companies that do that.

Amos :
>Usually it's people moving stuff from China so across the world so from China to the US. What happens is a factory in China will be like we have all this stuff ready for you to come ship. Come pick it up at our factory. We don't do that. These people have to go online figure out how do I get stuff from China to the US. It can't fit in a little box. It's like pallets of stuff. They'll find someone like us to help do it.

Siraj:
>Then you're probably doing a bunch of webscraping and consuming some APIs because you needed the data source right?

Amos :
>Yes to get that data. To figure out at any given time where is the freight we have to do some scraping. We're trying to get more and more to APIs successfully I would say.

Siraj:
>You're probably building what amounts to an API just scraping right?

Evie:
>Yeah.

Siraj:
>You're structuring the data and then you have to feed it to-

Desmond:
>I call scraping a hostile API integration.

Siraj:
>That's a good way to put it.

Desmond:
>We definitely have some of them.

Amos :
>A one way API integration. We're the only [crosstalk 00:13:58].

Siraj:
>That's funny. Hostile. Okay so that doesn't sound too bad. Rails sounds like the perfect fit. You're doing a little scraping.

Amos :
>It does. The great thing is we monetize such a high percentage of our traffic we don't have crazy amounts of scale so it's not like you need these high concurrency website going on. We can do a lot of it off probably a single or two servers. That's one of the big complaints like Rails comes slow. It's not an issue for us.

Siraj:
>Got you. That V1 you were hosted on what? Heroku? Where?

Amos :
>AWS I think always.

Siraj:
>Interesting. Okay.

Amos :
>I don't think they ever had Heroku.

Siraj:
>Was that a big decision? Do you remember?

Amos :
>No.

Evie:
>We had so many credits.

Amos :
>Yeah, we were YC. Oh, I shouldn't say this.

Siraj:
>Okay, awesome. AWS, Rails all sounds very simple. At that point you were just trying to go after the folks that were looking to ship stuff from China and they needed a better solution. How did you get to them? SEO?

Amos :
>Yeah, SEO is a big way. Freight forwarders, they don't buy keywords. Again, I shouldn't say this, but we got a lot of traffic from that. Those were our first few clients. We pretty quickly hired a head of sales and he started going after smaller shippers. It was very, very successful right away because there was huge market need.

Siraj:
>You guys, maybe still are, the biggest software solution, first software movers in the space. Right.

Amos :
>The big guys do have software. It's just not web software. They have mainframe and stuff. It's all AS/400's. Our biggest competitor all AS/400 mainframes, AS/400 simulator, this mainframe probably Cobol. That's the internal system so their web presence is very minimal.

Siraj:
>Got you. Okay. That sounds cool. You guys moved away from Rails? Can you talk about the evolution? What were the challenges you faced? How did you end up with your current?

Desmond:
>The front end, the rendering has moved away from Rails. All the backend is still Rails.

Siraj:
>Oh, okay.

Desmond:
>There's no plans to change that or anything. It's just that Rails was rendering like HTML and now it's just a static HTML page where React does all the rendering. I guess technically Rails is still rendering because we have server side rendering set up. The thing we moved away from was just rendering views with Rails and Rails partials and stuff like that. All that stuff got moved to the client side, but controllers, active record, routing, all that stuff is still Rails and will be for a long time.

Siraj:
>Postgres?

Amos :
>Postgres. We started with MySQL I switched to postgres because-

Evie:
>Transactional migrations.

Amos :
>Transactional migrations are huge for development. It's a very nice win on that. I also am better at admining postgres databases when they're on fire than MySQL so I was just like I know how to scale this better.

Siraj:
>Why is that?

Amos :
>Just with the experience of both Genie and Yammer were always on postgres so I had a lot of experience dealing with 3 am fires on Saturday night and I'm like I don't know if I'm as comfortable with MySQL.

Siraj:
>Wait. Yeah go ahead.

Evie:
>Then we had postGIS too. I love postGIS.

Siraj:
>I love postGIS. I guess now Uber's moving away. I can't believe it. It makes me cry.

Evie:
>I know. Apparently with their use case it makes sense but oh my god. PostGIS, we do the kayak style radius search reports so if you want to go from Milan to New York or Shenzhen to LA it will search all the nearby airports and seaports. It's just super fast and postGIS.

Siraj:
>Nice. Okay. You mentioned the admin side of it. Were you guys on RDS?

Amos :
>Yeah we're on RDS.

Siraj:
>Were you originally as well?

Amos :
>We were originally on RDS MySQL. I think it was probably the biggest push for me was the transactional migrations. I was getting very frustrated not being able to roll them back or not having them automatically rollback when you're doing Rails migrations. It was a huge pain point wasn't it?

Evie:
>Yeah.

Amos :
>Yeah. I like that part a lot. Again, because scale is not the biggest issue for us you could kind of pick either one. What's faster to develop on?

Siraj:
>Got you. Okay. That was probably the biggest piece of the stack that you guys changed.

Amos :
>Yeah, well the front end stuff. I think our templates were Haml right? What were they? Haml and what was the other one?

Desmond:
>Slim.

Evie:
>Slim.

Amos :
>Slim which was an even weirder version.

Desmond:
>There's still about ten or eleven Slim files that just render everything.

Amos :
>Slim was odd. I inherited that too. I don't think I would choose that.

Evie:
>It got to the point where no one wanted to touch any of the pages that weren't React?

Siraj:
>What was the main reason why Slim was so odd?

Amos :
>Why was it odd?

Amos :
>There were certain things you actually couldn't do with it. I can't remember the exact scenario. There's a way of embedding tags that you couldn't do with it and you'd have to-

Amos :
>There's a couple things you cannot do with it and you're just like this is crazy. It prevents me writing HTML so you have to then have a string of HTML inside of it. It's a deficiency.

Siraj:
>Yeah. We're using Haml for our site and there are some limitations. The benefit though is it's super clean. It's very clean, structured. You know exactly what's going on, but yeah it can get confusing.

Amos :
>The choice of React was very interesting. This was 2014. What was React like 0.9? Was it even 1.0? That was interesting because that was one of our lead front end guys I said, "You got to choose between Angular and React. I wasn't as involved in the front end world and he's like, "React. No problem."

Siraj:
>No research just boom.

Amos :
>Well he knew it. He had been using Backbone. He was at Trulia before so he know Backbone really well. I think he knew were the evolution of stuff was going. He really didn't like Angular. We had two other companies in the office at time and I asked both of them. I'm like, "Our lead front end guy, he'd only been there three weeks and I don't know if I trust this guy, he's going to choose React over Angular." They both use Angular and they were like, "Yeah. I don't know about that."

Siraj:
>That guy's dumb.

Amos :
>To Natesh, Natesh runs this company called Padlet, I was like, "Isn't Angular like everyone's using it. Why do you use the dominate platform? You're going to get left behind. There's no support of it. He's like, "Look, just because it's the dominate platform doesn't mean it's right. I can definitely see why React is going to beat Angular one of these days." He was using the prototype jQuery analysis. He's like, "A one time prototype" just crushed everyone and then jQuery came along and all of a sudden it was the dominate platform. That was a good argument. It was a good choice I think.

Siraj:
>That was the right bet.

Amos :
>It was a really good bet.

Siraj:
>This was pre-Angular 2?

Amos :
>Yeah.

Desmond:
>Oh definitely.

Siraj:
>That's interesting. You definitely made the right call. What are some of the challenges that you guys have run into as you've started to scale? As you've started to build out even the team? Maybe we can just get into some of the engineering challenges that you've faced. Was it on the data side? What was the hardest part about what you guys built?

Evie:
>I'd say the most complex was all the coding stuff that Brian and folks are working on now and we did originally with RTQ. Just getting our structure of like if you want to go between these two ports what are all the different charges? Do you charge by weight? Different partners have for the first hundred kilograms they charge this much and you get these really complex rate types.

Siraj:
>Where are you getting all this?

Evie:
>Partners actually send them to us directly.

Siraj:
>In nice format like API? Of course not.

Amos :
>No, sketchy, weird spreadsheets. Not even CSVs they're like these complicated Excel spreadsheets.

Evie:
>Thank god for data entry.

Amos :
>That's really hard. Other people's sophistication is probably one of our biggest challenges because we get data sources in such funny ways so we have to basically all this massaging code to deal with it.

Siraj:
>Okay so you have a bunch of Ruby scripts that are just parsing CSVs and-

Evie:
>Just a translation layer between god knows what business logic and who knows what format and our internal format.

Yonas:
>Is there any sort of standard between these companies when they send you these CSVs or you just run the script for any company?

Evie:
>That would be nice.

Amos :
>No, some of these are like, I wouldn't say mom and pop, they're actually pretty big companies, but they're in China and I don't know what they're internal systems are, seems like Access databases. They spit out these crazy complicated Excel spreadsheets.

Evie:
>They themselves have sketchy fees like handling fee. What does that really mean?

Amos :
>Yes. Yeah, they put in these really weird fees that we have to be like is this a real thing or this-

Evie:
>A kickback or a-

Amos :
>Yeah.

Siraj:
>Yeah. No, it's interesting. This sounds like a lot of Zenefits has to deal with. I was just doing Zenefits the other day and it's like all these outdated, complex systems that you just have to put a really nice UI on, but in the background there's a lot of stuff happening. Can you talk about how you're processing that stuff? Is it background jobs running every so often or rate tests?

Evie:
>Since we're processing it into our standard we have a team of data entry folks who know what we expect. They transform it. We've outsourced some that of that to Catapult I guess. Then when we get a new rate sheet, which is like every week, we have someone upload it and usually there's conflicts because spelling errors and stuff like that happens and they have to go into this edit view that gets all the conflicts between what we expected and what we got. Then it's just a dump in the database.

Yonas:
>It sounds like this could be a use case for predictive analytics? You have all these inputs and you have an output.

Evie:
>The historical data gets fun. I think in the future a big part of what we're going to do is like market predictions like should we buy now, should we wait for spot pricing, stuff like that.

Amos :
>Search pricing.

Evie:
>Yeah, man. I see us having finance guys.

Siraj:
>Yeah. It's holiday season so you're going to have to pay more.

Amos :
>Predicting prices is a huge challenge in our industry because it's this funny kind of not really open market. All the shipping lines, there's like I don't know 17 of them in the world or something. It's a bit of a cartel. Hope none of them are listening. The way pricing moves it's sometimes just all over the place because it will be like some guy on some desk at Mersk being like, "I think this client should get these prices." There's no real marketplace for it at all.

Siraj:
>There's no transparency.

Amos :
>No transparency whatsoever so we hope to build up a data set enough that we're really good at it and if we can we'll probably be one of the best at it in the world, but right now we're like wow.

Desmond:
>One thing that was interesting to me, when I joined I remember seeing this article that some people were colluding or there was a cartel or something, but then a few months after that the prices just dropped like crazy because everyone massively overcapacity planned and they all created this humongous ships which lowers their individual price but then every company did that which meant a massive overcapacity. I don't know how competent that-

Evie:
>We're not saying it's a competent cartel.

Amos :
>Yeah, exactly. It makes you think it's not a cartel because it's a historic lows and they're doing all this stuff to try to get the prices back up. They're parking ships in Singapore to try to reduce supply. It's kind of working actually, but it's just some crazy stuff. They definitely oversupplied.

Yonas:
>Have you guys noticed any kind of illegal behavior?

Amos :
>If we did we would report it. By law we should have to so yeah [crosstalk 00:25:58].

Evie:
>There have been some cases where clients ask us things and I've seen ops respond be like, "As a licensed so and so I'm not allowed to advise you on that."

Siraj:
>Canned response.

Amos :
>Yeah, no illegal behavior.

Siraj:
>I was actually going to ask, have you guys gotten any push back? People saying we don't these prices to be public?

Amos :
>Oh, from the carriers? Yeah, it's a big deal. There's this company called Xenta and they're whole business model is trying to predict prices so what you do is you upload all of your freight prices for the past however long and in return they give you a dashboard that shows, it's a data sharing platform, they show you every other one's aggregated prices. We hope this doesn't happen, but we think they might get murdered by the shipping lines or something because they do not want an open marketplace at all.

Siraj:
>Wow. Okay. Death threats are coming.

Amos :
>For them I hope that isn't the case. They're awesome. It's a great company.

Evie:
>That's a good sound bite.

Amos :
>Yeah, I'm sorry.

Siraj:
>Cool. All right so I guess you're saying one of the biggest challenges is the data side of it?

Evie:
>Just integrations with everybody else in the industry. There's a reason that this opportunity was still left available.

Amos :
>If it wasn't our problem then there wouldn't be a lot of value there.

Desmond:
>One way I look at the hard challenge is the business logic and domain rules are really complicated and not very intuitive. No engineer has really done anything with freight forwarding. It's hard to use intuition about what should be happening without spending a lot of time learning about it first. Just like modeling the supply chain in an accurate without our code turning into spaghetti is a pretty big challenge I would say.

Yonas:
>Speaking about that modeling the supply chain programmatically, was there ever an engineering disaster like red alert, like oh my god? Is there something like that you can talk about where you felt really worried? Like there was some suppliers who were pounding and the code was just breaking, you had to stay up late.

Desmond:
>What's a disaster that's happened?

Yonas:
>Maybe a near-disaster.

Desmond:
>I don't think there's been anything related to the modeling that's been disastrous.

Amos :
>Usually disasters are emails not going out. That's as close as we get.

Desmond:
>What was the one around the weekend the other day? That was some zombie process or whatever.

Evie:
>The delayed job?

Desmond:
>That was nothing [crosstalk 00:28:34] delayed job.

Yonas:
>Okay.

Desmond:
>It was running an old version of our code somehow which then meant that it was writing incompatible stuff and things we're blowing up. That was nothing to do with the modeling? I don't thing there's anything there. Probably like permissions is the only thing.

Evie:
>HackerOne's found some stuff that if it had been public it would have been bad.

Desmond:
>We have penetration testing through HackerOne. There's been some stuff they've found. That's a really good service actually because we give bug bounties when people find stuff and I'm really glad that it's them finding it and not three years from when we're-

Amos :
>Not the cartel.

Desmond:
>Right. Well not these people that apparently are murders or whatever.

Amos :
>It's a cartel. It comes with the territory.

Evie:
>Should we use fake names here?

Amos :
>Some hit squads.

Desmond:
>HackerOne's pretty cool. Sometimes the communication there's a little bit difficult, but it's been worth it. Although it has forced us to add in denial of service protection and some stuff we wouldn't have prioritized otherwise but it kind of comes with the territory with HackerOne.

Evie:
>Yeah, I think some of them are scarier.

Amos :
>Once you know about it then you have to move on it type of thing.

Evie:
>I think our scarier engineering moments have been HackerOne caused.

Desmond:
>It's mainly HackerOne participates running scripts that is nothing like normal user behavior. In theory someone could do that to us, but I don't know if anyone every would because that's malicious. To get value out of their service we had to make those things not affect production.

Siraj:
>Right.

Amos :
>Which is good. That's kind of the point is your service a denial of service proof.

Desmond:
>They're kind of like human fossers to some degree, but there's also some more intelligent attacks which is awesome.

Evie:
>Although it takes down the site and ops is like, "Wait, you mean this is on purpose? Why are we doing this?"

Amos :
>Yes.

Yonas:
>It seems like you guys have things on lock more or less but speaking about your development methodology? What is the methodology you guys use here? [crosstalk 00:30:40] Waterfall?

Siraj:
>What does sprints look like?

Desmond:
>Yeah we don't do sprints. We don't do waterfall. We're actually kind of working on that at the moment. I think what we've done so far is just take some practices from what we've seen elsewhere and thought about if they make sense for us and applied the parts of Agile or whatever part of Waterfall make sense. Whatever different methodologies there are take the parts of them that work and then or the parts that we think work for us and we've used them. I don't know if there's a name for what we do.

Siraj:
>It's almost de facto Agile because engineers have to have so much back and forth to figure out what ...

Desmond:
>Yeah.

Siraj:
>Okay.

Amos :
>We were a small team for a while so we were kind of like whatever gets stuff out the door. Now that we're a lot bigger we're buying some stuff from Yammer this thing called a Big Board. We're about to release this tomorrow so I'm announcing it here first before the rest team.

Siraj:
>This will go on much after.

Evie:
>You heard it here first folks.

Siraj:
>Stupid.

Amos :
>I think originated with the Yammer VP there, but it's basically trying to time box development from one to four weeks and getting feedback from the engineer or group of engineers that are working on it, how long it's going to take, and making sure each project has a DRI to borrow from Apple, directly responsible individual to help with the time boxing.

Desmond:
>It's all about fixed time but variable scope so we can try to know what we're doing and when it's going to happen and if things are delayed we try to cut scope to fit it in. That's all happening literally tomorrow.

Siraj:
>Okay. When you say Big Board do you mean literally there's a big board?

Desmond:
>It's going to be this.

Amos :
>It's going to start with this white board that we have in front of this and it's going to expand. We bought a bigger one. It hasn't arrived yet. It's just literally going to have every single project we're doing and who's working on it and then the dates for when they're going to be done. We're going to do some feedback loops like say is it on time. What is it green, amber, red?

Desmond:
>Yeah, green, amber, red. Yammer does this and I previously was at Kahn Academy which was inspired by Yammer to do the same thing so it's not really that big of a thing but we just have a large proportion of descendants from the company here.

Siraj:
>The whole purpose there is to get a better idea of what the road map looks like time wise?

Desmond:
>A big purpose is to provide space for engineers to work on projects and be accountable to getting it done on time without having to deal with a lot of interrupts. We have a support team that handles any kind of interrupt. They're like an interrupt handler so any bugs go to them, any pm that has a demo and we forgot this one little feature that has to happen tomorrow. That will go to the support team. The support team handles all the unpredictable stuff. That means developers can be heads down on a project and operate on maker time.

Siraj:
>You have engineers on support?

Desmond:
>Yeah.

Siraj:
>Got you. Then does this also have to do with prioritization? I think Pandora does it. It sounds similar where they have a big board and they've got sticky notes and you put everything next to each other than you realize that my feature's not important.

Amos :
>>That's like when they do they're 90 day road map planning. They have voting. It's usually for the executives to go in like, "Hey. I want this feature. I want this feature." Then the head of prod will go back and be like, "Okay. This one wins. This is what we're going to work on. That's a separate process for us. We do that a little bit. A long with what everything Desmond said, one of the problems we had with things just taking to long so we really want to force that scoping step. A PM will work with an engineer. The engineer will be like, "You know this is going to take me two months." What can we take out so it will only take me four weeks? Really just having that process nailed down.

Siraj:
>Got you. That's awesome. Do we want to dive into the tech and talk about what are the moving pieces? Where are these apps? How many apps do we have going? Just like run through the stack? Maybe briefly. You probably have a good idea of everything going on.

Amos :
>Yeah. You guys can start. We only have two apps, oh three. Three apps. These are single page apps and the isomorphic Javascript sense, right?

Desmond:
>Yeah I think that's the terminology.

Evie:
>Isomorphic asterisk.

Desmond:
>I think the word is universal now. People reacted against isomorphic.

Amos :
>That never made sense so [inaudible 00:35:31].

Siraj:
>okay.

Desmond:
>There's three front end apps. One for internal usage, one for clients, and then another one for partners which is a lot smaller. Mainly I think trucking companies are using that right now. There's different requirements for browsers on that app because trucking companies in China are probably on IE6. Whereas for Core which is the internal app we just require that everyone uses Chrome and we can use FlexBox or anything else that we want to make development easier on that.

Siraj:
>Is it three Ruby apps?

Desmond:
>No these are three React apps.

Amos :
>No these are front page apps. Only one back end Ruby.

Desmond:
>They all took the same monolithic Rails backing.

Siraj:
>Okay so one big Rails app serving up the API for the most part.

Amos :
>Yes and one database as well. One schema.

Yonas:
>Any plans for iOS or Android?

Amos :
>Yes, we have plans. Can't tell you exactly.

Desmond:
>To be announced.

Amos :
>Most likely we'll probably do React Native.

Desmond:
>Yeah, I'm definitely going to push for that.

Amos :
>We have several React experts on staff that were push for it. I think it makes logical sense.

Siraj:
>>Yeah. Most of them are in the room.

Desmond:
>No, there's others.

Yonas:
>Which of the three apps takes the most engineering effort would you say?

Evie:
>Core.

Amos :
>Core.

Yonas:
>Core?

Amos :
>Easy.

Desmond:
>Yeah, which is the internal one.

Siraj:
>Wait, so when you say internal you're talking about internal to Flexport?

Desmond:
>All of the people in this rest of this floor are the ones spending most of their day in it. That's the app where we have the really fast feedback cycle because we can launch stuff and literally walk over to see it over someone's shoulder in production. That's the most complex one.

Siraj:
>Most of the changes you're making all the deploys they're mostly to the Rails app right?

Evie:
>Both.

Amos :
>We consider the front end different so it's probably more to the front end. Right?

Desmond:
>Yeah, I don't know. I haven't thought about it actually.

Amos :
>60/40?

Desmond:
>I don't know what the breakdown is on lines of code between Javascript and Ruby?

Evie:
>It's so verbose in Javascript I think.

Desmond:
>Yeah.

Amos :
>Functionality.

Desmond:
>F.lux kind of skews it a bit.

Amos :
>I would say we have more Javascript if I had to throw it out there.

Evie:
>Yeah definitely.

Siraj:
>Then there's the 4 apps, 3 front end one back end.

Desmond:
>Yeah, if you want to call the back end separate. That's not really an app. Right? Users still use it. It's part of the other app.

Evie:
>It's the back end to the other end.

Yonas:
>The helper app.

Amos :
>Yeah. We don't have separate logical website that goes to a totally different database and servers like that. We pretty much just have one.

Yonas:
>Changes propagate to all three sometimes if you want to.

Amos :
>Yeah. We're probably using apps in the wrong way a little bit.

Desmond:
>Yeah maybe. The terminology's weird here.

Amos :
>The front end is like three different views on the same Rails app.

Siraj:
>Oh, okay.

Yonas:
>Got you.

Siraj:
>Let's say you have a new version of the app. You're just pushing that to the Rails app?

Desmond:
>Our deploy process everything goes out at once so there is not services or anything like that. If you want to get some code out you have to deploy everything so that's Rails and Javascript at the same time. If that makes it one app then it's one app.

Amos :
>We have one app. We have one repository of code.

Desmond:
>Except the CSS.

Yonas:
>Do you guys use continuous integration?

Evie:
>Travis?

Desmond:
>Travis? Oh, yeah.

Siraj:
>What does your whole deploy process look like? Everyone's using Docker hopefully I assume?

Desmond:
>No ours is nowhere near as fancy as that. Actually ours has inspired a lot, well at least in my opinion, is inspired by Zack Holman's deploying software blog post which is really good.

Siraj:
>I remember that.

Desmond:
>When someone has a poor request it gets approved and then as soon as it's merged to master it's immediately deployed. It's a manual step to deploy it. It's a bunch of Capistrano scripts.

Siraj:
>Plenty of TEC too.

Desmond:
>Yeah, exactly.

Siraj:
>While the tests are running on Travis you said?

Desmond:
>No, well we wait till the tests pass before it would be approved. Usually it gets code reviewed by someone and then once the tests are green the author merges it and immediately deploys to production. Our tests I think we have 5. We're paying Travis the maximum we can which means we can test two things concurrently because we used 5 instances to run tests when we open a poor request.

Siraj:
>How long do your tests take to run?

Desmond:
>I think the slowest one's about 11 minutes. 11 minutes after a poor request is open you know if it's passing or not.

Siraj:
>Okay. Then are you pushing it out to staging?

Desmond:
>Sometimes.

Siraj:
>Do you guys have a staging ...

Desmond:
>Yeah, we have a few different staging environments. We've got just one that is identical to production and then there's a new thing that just got created recently. We're having some contention there where there's a single staging environment and multiple developers want to test their stuff.

Siraj:
>Yeah, you might have to have different staging zones for different branches.

Desmond:
>An engineer just set up a containerized staging thing where we a have a machine that will just deploy it to a container and then I think we can have ten or something there.

Siraj:
>That's all Docker right?

Desmond:
>Yeah, that's all on Docker.

Amos :
>Feature branches are on different servers.

Desmond:
>Yeah. I think long term probably our normal environment will move towards that, but that's brand new as of two weeks ago or something.

Amos :
>Yeah, we have plans. Production right now is not containerized but we have plans to get it there based on this test with staging.

Siraj:
>Interesting. Okay.

Amos :
>I guess our dev would then naturally fall out of that as well.

Desmond:
>Yeah, maybe.

Amos :
>Yeah.

Yonas:
>What's the current successful build rate?

Desmond:
>I have no idea.

Yonas:
>Oh, okay.

Amos :
>Out of every single build to master, how many break?

Yonas:
>Yeah.

Amos :
>It's probably like way over 90. We should look at that.

Desmond:
>Yeah, I don't know what it is but-

Evie:
>We go days sometimes. Sometimes we have multiple failures in a day.

Desmond:
>Yeah. It's definitely [inaudible 00:41:31] part of break master. I think the most frequent way it breaks is Travis had some network error. We have tests that we hit and endpoint and service side rendering is a little bit flaky sometimes in a test environment for some reason so sometimes those will fail. Just the other day we ran into an issue where all of our pre-rendering tests were in a single instance and I guess we just got enough of them that I think maybe it doesn't clean up memory after running them or something and it was getting out of memory on Travis so we just split it into two instances and we'll deal with that in the future.

Amos :
>For some perspective it breaks way less often than other companies I've been at.

Siraj:
>Oh really?

Amos :
>Oh yeah.

Siraj:
>Nice.

Amos :
>Like 90% less.

Desmond:
>It's definitely above 90 yeah.

Siraj:
>Wow. Do you punish whoever broke the build?

Amos :
>Yes.

Evie:
>There's a cone of shame.

Amos :
>A cone of shame and our ...

Siraj:
>Send out an emoji.

Yonas:
>Do f.lux on the roof or something.

Siraj:
>Are you guys using Slack or what are you guys using?

Evie:
>Oh yeah.

Siraj:
>We're just assuming stuff now.

Yonas:
>You guys have coding standards? I mean of course you do, but what are ...

Desmond:
>Yeah, we use Rubocop and ESLint to lint everything.

Yonas:
>Codeclimate? How does that run?

Desmond:
>We don't use codeclimate. We just have some manual linting setup in a configured file with a bunch of rules.

Amos :
>We used codeclimate before and we did not like it.

Siraj:
>Really?

Amos :
>Oh yeah.

Siraj:
>[crosstalk 00:43:04] for an old GPA thing?

Amos :
>Yeah, I mean-

Desmond:
>When was that?

Amos :
>Before you were here. Consensus was like turn it off because it wasn't helping us at all. Maybe it's changed. That was a year and half ago.

Siraj:
>We're using codeclimate. It's interesting because it really enforces a lot of the best practices for Ruby but some of the stuff we just don't really care.

Desmond:
>Don't you get from Rubocop?

Siraj:
>You do. They run it over there and then they give you the score and you can see how it changes over time.

Desmond:
>We just have it set up as a pre-commit hawk so if you do anything wrong you just can't open a poor request.

Siraj:
>Oh really?

Desmond:
>Yeah.

Siraj:
>That's crazy.

Desmond:
>You fix your stuff before you show it to anyone else so you don't [inaudible 00:43:46] discussions in poor requests. Then so poor request can focus on design or architecture or something as opposed to it's a multi-line block so you should use do end versus braces or whatever.

Siraj:
>Yeah, it's kind of the same idea behind CI right? It's running somewhere else and then it passes or fails.

Desmond:
>Yeah.

Siraj:
>What you're saying makes sense. You want to solve that sort of thing before it gets there. Do you want to cover monitoring? What do you guys use to take a look at production and make sure that everything is running smoothly?

Amos :
>We use New Relic. We also have-

Desmond:
>Sentry.

Amos :
>Sentry which is for exceptions, but then Pingdom. You guys probably don't even know that. It rarely breaks. I'm probably the only that gets those and I haven't gotten one in like a month or two.

Siraj:
>That's really good. That's awesome. 100% up time for the past couple months.

Amos :
>Some things break. Pingdom doesn't get everything.

Yonas:
>How do you split up PagerDuty?

Amos :
>Again, we don't have a need for it so we don't use it.

Yonas:
>You're just using pure Pingdom?

Amos :
>Yeah. That's it. We don't use PagerDuty.

Yonas:
>That's pretty cool.

Siraj:
>Everyone gets 8 hours.

Amos :
>I have spent a lot of time at 2am on Saturdays fixing code and this is it's great.

Evie:
>This is so nice.

Amos :
>It's great.

Siraj:
>Nice. Are you guys using anything else aside from New Relic like Librato?

Evie:
>Occasionally Bullet we use for digging into N+1 queries.

Siraj:
>Oh, Bullet, yeah for actually queries in code.

Amos :
>Monitoring no I don't think so.

Siraj:
>New Relic is really all you need to see what's ...

Amos :
>It's pretty good. I haven't checked out Librato.

Siraj:
>Okay. Cool. Analytics? What do you guys use to look at front end or user flows and all that stuff?

Desmond:
>We use a couple of things. The black magic one that I hadn't seen before I joined this company is FullStory because we have fewer users that have larger transactions. You get a lot of value out of watching sessions.

Siraj:
>They record the whole session.

Desmond:
>Yeah. That's been really valuable for that and also for figuring out if a bug was user-impacting or if some part of the UI is confusing or anything like that so FullStory is definitely a good tool that we get a lot of use out of.

Evie:
>If I could invest in FullStory I would.

Siraj:
>Nice.

Amos :
>It's a good tool. We also use Periscope Data for all our analytics. A lot of people probably know what this is, it basically looks at your slate database and allows you to build graphs out that. We'll push stuff to it event logs as well to figure out what's happening in user flow and just basically runs sql queries that are graphed over time.

Siraj:
>Oh, okay so it's like UI over your data.

Amos :
>Yes.

Siraj:
>An easy way to slice and dice.

Amos :
>Yes, sql [inaudible 00:46:50] tool probably.

Siraj:
>Very cool. I guess Google Analytics somewhat as well.

Amos :
>Some people use it. We don't use it as much.

Desmond:
>I use it to see how many people are using bad browsers and stuff like that.

Siraj:
>Nice, browser breakdown. For FullStory, are you just recording every session all the time? How does that work? Is a percentage of traffic?

Desmond:
>I think right now we're recording everything.

Siraj:
>How do you know what to look at? You can see which ones have exceptions?

Desmond:
>Well, they're exception stuff isn't that great actually. We use Sentry to figure out when exceptions happen and often there's you open Sentry and then you figure out who it was then you go find them on FullStory. I would really love if those two things would merge actually.

Yonas:
>Yeah, integration.

Siraj:
>Yeah, that doesn't seem too bad though. Right? Other companies like us we just have to manually figure it out. FullStory sounds cool. Analytics then payments.

Evie:
>Stripe.

Siraj:
>Stripe?

Evie:
>Yeah. There was some talk of Adyen for SEPA but we haven't gotten to that point yet. Although I think Stripe has a beta SEPA payment now.

Siraj:
>I have no idea what that is.

Amos :
>It's for European payments.

Siraj:
>Okay, good to know.

Evie:
>Single Euro pay zone or something.

Siraj:
>Oh, okay.

Yonas:
>Throw Bitcoin in there as well maybe.

Siraj:
>We've talked about Bitcoin.

Amos :
>We're a little worried that Bitcoin makes us look like we're money launderers or drug dealers which is really bad when you're licensed by the custom board. It was a pretty good argument our CEO made.

Evie:
>Like, "Oh, they paid for this container from Columbia with Bitcoin."

Amos :
>Exactly so we've stayed away probably wisely.

Siraj:
>Got you. I'm just running through looking at this stack here. Emails? You said there were some issues from time to time. What are you guys using?

Evie:
>SendGrid.

Siraj:
>SendGrid. Okay. Those are all transactional. You guys send out newsletters? Flexpoint Daily?

Evie:
>We do some digests.

Amos :
>Do we use MailChimp?

Evie:
>Oh, we might. I've seen records.

Desmond:
>I think sales uses something for like newsletter kind of stuff.

Amos :
>I think we do MailChimp for newsletters. I could be wrong.

Siraj:
>One thing you mentioned that I wrote down here, for pre-render have you experienced any issues using pre-render through React for SEO purposes? Has that impacted SEO at all? I know that's a big part of your strategy right?

Evie:
>I think we first started doing it to help with SEO.

Siraj:
>Right.

Evie:
>Oh I'm sorry. Was that what you were ...

Siraj:
>Well yeah. I've heard stories people saying there have been issues where sometimes crawlers won't get stuff. Have you guys run into any issues or has that been working fine for you?

Desmond:
>I think we've been server-side rendering stuff from the start so I guess we wouldn't really detect if there are any issues. Most of our app is behind log-ins so it's not SEO-related. I think the public facing stuff's always been server-side rendered.

Evie:
>There was a while where I think Toine had to turn it on for. I remember him mentioning SEO.

Desmond:
>I actually did a lot of AB testing for this at Kahn Academy because SEO is really important there. Our app was very client rendered. We put a big emphasis on making sure that our code was server side renderable for that purpose. I think Pinterest has a really good blog post about this called Demystifying SEO where they outline an AB test they did. It's kind of old now. It might not be relevant anymore because I know that Google has actually stated that you can client render things and it will work, but they measured some stuff that was to the contrary. It might be a year and a half ago now.

Siraj:
>Okay, interesting. Everything is pre-rendered for you guys.

Desmond:
>Yeah.

Siraj:
>Okay.

Yonas:
>You guys were talking as well about moving from f.lux stores to GraphQL and Relay. Could you explain a bit why you guys chose to transition?

Desmond:
>I don't think the choice has been made quite just yet, but we're definitely seeing some pain with Flux. State management in React is a thing where there's a bunch of different opinions about how to do it and our app is pretty big so there's a bunch of different ways that it gets done. Most of the time we use Flux. There is a lot of use of local component state as well, but some of the problems that we have are, for example, we have this shipment details page in Core which originally it started as an admin view of the shipment entity but now it's grown so many different things it needs to display and it makes a lot of calls to the back end. Those back end endpoints have that rest problem where they might get used on multiple views so they accumulate more and more properties on h-model that may not necessarily be used on the calling view so you end up having to load a bunch of data that you don't need to render the page. GraphQL solves that problem really well. We're experimenting with that and what we're going to do is-

Yonas:
>Sorry. GraphQL solves that problem really well because?

Desmond:
>Sorry. It solves that problem really well because it co-locates the jSON template. It's basically jSON without values so each React component describes exactly what it intends to display and then relays a sibling to GraphQL when using it with React. Relay assembles all of those components into one big query that says here is precisely the data I need to display this particular page declarative and the you'd get just that data. We've run into problems where we're trying to display a shipment but we might have an invoice and a due date but that invoice is, when we load it from the database, joining on a bunch of unrelated stuff that the shipment page doesn't need but because it happened to be in the API we're spending the time to generate it.

Siraj:
>You can specify that through Relay you're saying?

Desmond:
>Yeah. I don't know if you guys have used prop types. It's basically like saying exactly the things that end up in the view are the only things that will come back from the API. Everything else will be ignored.

Siraj:
>What do you need GraphQL for?

Desmond:
>GraphQl is kind of like a server-side component of that and Relay is the thing that takes a bunch of GraphQL fragments and assembles them together and says, "Hey GraphQL, get me this stuff".

Siraj:
>Then GraphQL is on top of postgres?

Desmond:
>Yeah. It's actually on top of Rail so it still will load active record models and stuff to get the information. The other reason is sometimes you have miniature models. If you have a list view you might just want to get a lightweight shipment model for example, but when you go into the details page you want a heavyweight one. That means you have a different type of object but both of our languages are weakly typed so we do have a lot of errors where if you access this page in this particular way a bunch of the attributes will be null so you'll get a run-time error. GRaphQL introduces some types to our API which will make it obvious when that kind of thing is going to happen. If we do that and then also start using Flow on the front end I feel like we can catch a lot of those errors that we run into at compile time. That would be awesome.

Siraj:
>What is Flow? I've never heard of Flow.

Desmond:
>It's kind of like typed script but better.

Siraj:
>For the real time tracking piece, can you talk about how that works? Is that web sockets? What are you guys using? How'd you build that?

Evie:
>For real time shipping tracking? User tracking?

Siraj:
>Real time shipment tracking.

Evie:
>Sorry what?

Siraj:
>Postgis. I guess is for communication aspect.

Evie:
>We just have a lot of integrations in the scrapers with FlightStats is a really useful thing we use for tracking flights because a lot of our cargo just goes on flights sometimes on passenger flights in the belly of the plane. We use the same services that power AmericanAirlines.com flight status. That gives us really good data. With ships it's a little bit sketchier especially depending on the country and everything. We have a few different sources that we try and combine and it's just whoever reports that the ship has arrived first wins.

Siraj:
>Got you. Okay.

Desmond:
>For updating on the client side we use Firebase. We ping browsers with Firebase to make them request data from the API. We don't actually send information over Firebase except the fact that this model that you're looking at might be stale and needs to be updated. There's some software for that I guess.

Siraj:
>Okay so you're requesting it from the API. That makes sense.

Desmond:
>In Rails I think we have when a model gets written to there's a callback that says notify all browsers that have this model on the screen open so Firebase is the thing that does that. When a browser session's open it has a subscription to Firebase. Firebase is the thing that pings all the browsers to tell them my dot is out of date. I need to request an update.

Amos :
>It's mainly also for presence to figure out if there's multiple people looking at a particular shipment at once will pop up their profile and be like this person's looking and this person's looking.

Siraj:
>Oh nice.

Amos :
>Yeah. That's all done through Firebase.

Siraj:
>Have you guys run into any challenges with that? Is that pretty simple to set up?

Amos :
>It was pretty simple to set up. The engineer who did it is not here but he did it in a weekend basically. It hasn't gone down. It went down once I think in a year. It's been good.

Siraj:
>I'm just curious future decisions in general, how does that play out in the engineering team?

Amos :
>Again, we're changing this process. A part of our big board is engineers can write project proposals to be approved by some other group of individuals. Again, they should be from one to four weeks. Previously it was pretty much the PM's would come up with a lot of the stuff. We originally had engineers come up with features but because what we do is so complex and there are so many business rules like for each feature we did in the early days there was 50 new fields you would have to add to the database. At a certain point we kept adding fields we'd be like, "Oh, this is done. We have every single field of freight forwarding mapped out and then another project would come through and it'd be like a hundred more fields. It got to the point where you really need product managers to digest all this information and figure out what we need to build next. A lot of the stuff comes down from them, but the thing like the presence and the Firebase stuff that was just organic. That was an engineer who's like, "I think we need this." He did it over a week.

Desmond:
>I think a lot of the tech tools are just an engineer is passionate about it and can convinces the rest of the team that it's something we want to do.

Siraj:
>That's awesome. Cool. Okay. That's good to hear. Maybe we should, we're coming up on time, but we never really covered team structure and team size. How big is the engineering team?

Amos :
>The engineering team total is about twenty right now. Then we have four PM's, four designers. We really want to keep it at a one to one PM to designer ratio and then about one to four engineer to PM ration. Again, because it's so complex. We need a lot of PM's to build what we need to build.

Siraj:
>Got you. Then at least two engineering managers.

Amos :
>We have three now.

Siraj:
>Three? Okay. All right, cool. Then there's sales and support.

Amos :
>Yeah. In the entire company?

Siraj:
>Yeah.

Amos :
>Yeah, so we have sales, operations, and they make up a big part of it. Again because it's a very human powered thing right now. HR, recruiting, finance.

Siraj:
>Then are you counting the support engineers as part of engineering?

Amos :
>The support engineers they are engineers. The way we do support is a rotation. We do a week long rotation of one engineer will be on support for a week, then a different one, then a different one to go through everyone.

Siraj:
>You don't have support engineers?

Amos :
>No.

Siraj:
>You just have engineers who do support.

Amos :
>We have a QA person but just one.

Desmond:
>She's a recent convert from ops so she's got a lot of product knowledge and a lot of knowledge about how to work around bugs and stuff like that. She's developing knowledge on the technical side. That's actually made our bugs process go a lot more smoothly.

Amos :
>Yeah, it's been great because the business rules are so complex that she already knows all that stuff.

Evie:
>She teaches the support engineers what is going on.

Amos :
>She teaches like, "This is what we need to do to move the shipment here."

Desmond:
>She's able to prioritize bugs way better than we can. Before we had her and you were on support duty you would get a bug and you wouldn't know is that actually a bug? Where do I go in the appropriately to even get here? It was a lot harder to diagnose what's going on.

Evie:
>People would just send you a screenshot and you'd be like I don't know what's wrong with that.

Desmond:
>Yeah.

Siraj:
>Nice. That's good that you guys have figured it out.

Yonas:
>She seems pretty high quality. It seems like you guys have high quality engineers here in general. What is the interview process like?

Siraj:
>Are you looking for engineers?

Amos :
>Yes, we are looking for engineers. Always.

Siraj:
>Has anyone ever answered no to that?

Amos :
>We changed it recently. You guys recently redid it a little bit.

Evie:
>I guess. It starts with a phone screen unless people go through TripleByte which a lot of our candidates come through.

Yonas:
>Okay. TripleByte?

Siraj:
>TripleByte is a YC company. They're recruiting very, very awesome. Plug for TripleByte.

Evie:
>Thank you TripleByte.

Siraj:
>Okay so the first step is go through TripleByte.

Desmond:
>Well sometimes.

Siraj:
>Sometimes.

Evie:
>Maybe ideally a phone screen just for our sake. If they pass the phone screen we bring them on site. Three engineering interview. We usually like to have them get coffee with someone on operations so they can ask about the business and stuff. We tend to attract entrepreneurial engineers who see the business opportunity and that's what caught their eye about us.

Siraj:
>Okay.

Evie:
>Standard issue interviews. We give a demo. We try and dig into someone's past projects and try and get them to tell us in depth about something they really worked on or enjoyed working on. Try to get a sense for what make them happy day to day and how they fit in the team.

Siraj:
>Cool. All righty.

Yonas:
>All right.

Siraj:
>Anything else before we wrap up here?

Yonas:
>What's next for Flexport?

Siraj:
>Oh yeah we didn't even talk about that. What's next on the tech side, business side? Anything big in the pipeline?

Amos :
>Yeah. The next ten years we're hoping to build the platform for global trade. We think we have a unique opportunity in this space because a lot of the bigger players stopped innovating a long time ago in terms of technology. Maybe this is a little too far out, but we really are trying to build out end to end how you move freight so building up this platform that anyone can use and trying to open it up to other providers, other freight forwarders so broad based, that's definitely what's next for us technically.

Siraj:
>Taking over the world?

Evie:
>Yeah.

Amos :
>Yeah. I don't want to say world domination. I think I just said that.

Evie:
>It's such a fragmented space because the top ten forwarders have 9% market share.

Amos :
>Yes, and it's a $1.2 trillion space so it's just massive. There's a lot of opportunity there.

Siraj:
>Definitely. Super exciting. On the tech side anything new in the pipeline? Any major changes?

Desmond:
>Yeah, I talked a little bit about Relay and GraphQL we're experimenting with. Flow is another thing we're going to start using if I have anything to do with it. I don't know.

Siraj:
>Containerizing stuff.

Amos :
>Yeah that's true. Containerizing is going to happen soon.

Siraj:
>Move to ECSL. Start using ECS. Okay. Cool.

Evie:
>I'm excited about advance coding and all of the routing optimization problems we're going to run into.

Siraj:
>Oh right, okay. Awesome.

Evie:
>The graph theory nerd in me has been waiting for that since day one.

Siraj:
>Upgrading to Rails 5 probably?

Desmond:
>I mean maybe.

Amos :
>We should do that.

Desmond:
>We'll probably get around to it.

Siraj:
>Cool. Cool. Awesome. Well thanks so much guys.

Yonas:
>Thank you.

Amos :
>Thank you.

Siraj:
>Thank you.


