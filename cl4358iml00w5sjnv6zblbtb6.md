## Introducing ReactPlay - Learn, Create, Share ReactJS projects

> NOTE: ReactPlay made by @[Tapas Adhikary](@atapas)

If I tell you React(aka ReactJS) is one of the leading user interface technology(ok, library) in web development, would you believe it? Most of you will. For the rest of you, let me put forward some stats.

As per the Stack Overflow Trends, ```React``` is the most emerging JavaScript-based user interface technology since 2014. This trend is entirely based on usage.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654542735731/hA7aYfLWG.png align="left")

Source: [Stack Overflow Trends](https://insights.stackoverflow.com/trends?tags=jquery%2Cangularjs%2Cangular%2Creactjs%2Cvue.js%2Csvelte)

React was among the most used web frameworks used in 2021 and continues.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654542788333/vhD9jdk4v.png align="left")

Source: [https://insights.stackoverflow.com/survey/2021#section-most-popular-technologies-web-frameworks](Stack overflow survey 2021)

In the last few years, we have seen popular web frameworks like ```Gatsby```, and ```Next.js``` choose ReactJS as the base technology to build upon. With the Web3 boom as well, React is the front runner. While there are other remarkable frameworks and libraries around, the demand for React is evergreen, and it has been proven so far.

The React Developer Communities are very active in learning and sharing on various social media platforms like Twitter, LinkedIn, Showwcase, etc. There are many tutorials, YouTube videos, and courses to help many beginners get started with ReactJS. However, we seem to miss something.

# The Need

In early 2022, I published a revised, [full-fledge roadmap to learn ReactJS on freeCodeCamp](https://www.freecodecamp.org/news/react-fundamentals-for-beginners/). To my surprise, I have received some great questions on Twitter DMs. Here are a few,

- The roadmap is great, but what to build as a beginner?

- How do we know we are doing the right coding with React?

- Can I look into a project and build something inspired by it?

- Can someone look into my code and give me feedback?

None of these was an extra ask. If you are learning something, you need to practice. To practice, you need to build projects. To build projects, you need to know what to build and how. Once you figure it out, the next thing is to learn and excel from the feedback and reviews. Finally, you need to tell the world that you have learned it hard and earned it passionately. So you need to socialize on what you have accomplished.

As these thoughts were taking multidirectional swings inside my tiny brain, I thought, why not build a platform for community-driven learning of ReactJS? At that moment, the idea of ```ReactPlay``` started seeding in my mind.

# What is ReactPlay?

```ReactPlay``` is an Opensource platform to learn, create and share ReactJS projects with the developer community. You can start by browsing through many ReactJS based projects like beginners, intermediate, and advanced. It allows you to learn from the code, explanation, articles, and videos related to a project and inspire you to create one.

We call each project a ```play``` in ReactPlay. When you create a play with a few simple guided steps, it goes through some serious code reviews by experienced ReactJS developers. In the code review process, you learn several aspects of doing it right with React, "Thinking in React". After a successful code review, your play gets accepted and be part of ReactPlay to inspire many others in the community. So it is a chain to learn, create, and share all about React.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654543177778/3XIURQwOz.png align="left")

Here are some important links for you to look into,

<ul>
<li>✅ <a target="_blank" href="https://www.reactplay.io/">Check out the ReactPlay Platform</a></li>
<li>✅ <a target="_blank" href="https://github.com/reactplay/react-play">The Open Source Code on GitHub</a>. Please give the project a ⭐ to show your support.</li>
<li>✅ <a target="_blank" href="https://twitter.com/reactplayio">Join us on Twitter</a></li>
</ul>

# How ReactPlay Can Help React Developers to Grow?

The motto of the ReactPlay platform is to help developers to ```Learn```, ```Create```, and ```Socialize```. Let's understand how!

## 👩‍🎓 Learn from Existing Plays

The ```ReactPlay``` web application lists the React projects of different experience levels. You can find them on the [playlist page](https://www.reactplay.io/plays). The interactive search and filter feature allows you to find the plays of your interest and get into the details.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654543384865/DHlm1H7De.png align="left")

Each project is detailed with a title, description, who created it, and a playground to interact with it. The interactive nature helps you understand the purpose of the project, and at any point in time, you can dive into the source code to learn from it.

If a play creator links the project with a blog article or YouTube video, it helps you further read and learn about it. Got a doubt or feedback? You can instantly start a conversation with the play creator using the ```Comments``` feature.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654543444686/mvhNPbteR.png align="left")

GitHub's Discussions feature powers the comments feature. Please read more about this implementation from here: [Comment system using React and GitHub Discussions](https://blog.greenroots.info/comment-system-using-react-and-github-discussions).

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654543490183/y2EsgAjr5.png align="left")

Overall, the opportunity to learn from others will only accelerate your learning and inspire you to do more. But, hang on, who approved these projects? How to create one?

# 🏆 Create a Play

ReactPlay encourages you to create plays(aka projects) using a few simple steps. You can create plays with any ideas of your choice. If you run out of an idea, please take a look at the [ideas](https://www.reactplay.io/ideas) page to pick one and create. If you are unsure or have any doubts, start a discussion, and we will make sure you get started.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654543553285/fFT6qGPb-.png align="left")

Once you have settled on the play idea, please follow these steps to get started.

- First, you need to fork the [react-play](https://github.com/reactplay/react-play) repo. You can do this by clicking the ```Fork``` button on the top right corner of the repo. If you are new to forking, please watch this [YouTube Guide](https://www.youtube.com/watch?v=h8suY-Osn8Q).

- Once forked, you can clone the repo by clicking the ```Clone or Download``` button on the top right corner of the forked repo.

- Next, install the dependencies by running the following command in the ```react-play``` repo:
```bash
 npm install
 # Or
 yarm install
```

- Use the following command to start the app in the development mode:

```bash
  npm start
  # Or
  yarn start
```

- It runs the app in the development mode. Open http://localhost:3000 to view it in your browser.

- Open another command prompt in your project folder and run the following command

```bash
  yarn create-play
  # or
  npm run create-play
```

It will ask a few questions about your ```Play``` and then perform the required steps to create the play. The screenshot below shows the output of the command. ```ReactPlay``` is equipped with both ```JavaScript``` and ```TypeScript```. So you can use either of them as the base language for your play.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654543975063/BxrYRa9Qx.png align="left")

ReactPlay uses [PlopJS](https://plopjs.com/) to automate the play creation. It automatically helps create the scaffolding, setting imports, and initial code structure for the creators. The creator can import the project into their favourite code editor like VS Code and start implementing the play logic. It's simple. Give it a try.

After you are done with coding for your Play, you can submit it for review. Submitting a Play for review is a two-step process.

- Create a Pull Request on the ```react-play``` repository with your changes.

- Dedicate some time in a week to take care of the review comments.

Once the Pull Request is approved and merged, we will notify you and add you as a contributor to the ```react-play``` project. Your play will be available on the playlist page for others to take a look and learn from it.

# 🚀 Socialize Your Play

```ReactPlay``` supports deep linking. It means you can access a play directly with a unique URL. You can share the same URL on social media platforms for others to access it. The play appears with its cover image, title, and meta description. Here is an example,

> New Play alert 📢
It’s called Keeper.

> 🖌️ Created by @Shivamkatare_27

> Want to take note and keep it somewhere 📝

> Have a look 😃 https://t.co/4uflHajqYV


> &mdash; ReactPlay.IO (@ReactPlayIO) May 5, 2022

Additionally, you can share the play on Facebook, Twitter, LinkedIn, and Reddit with a single click from the Share modal.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654544228664/7P2GspcgN.png align="left")

So, let the whole world know about your work and achievements.

# How Can You Contribute?
Want to contribute to ReactPlay? It is easy. Just get started by creating a play. It will help you to practice everything that you learn about ReactJS. At the same time, you will also contribute to an Opensource project. It's a Win-Win.

But what if you are not a React developer and still want to contribute to the project? No problem, you can. Here is how,

> 🤯: I don't know React. Can I contribute to ReactPlay?

> 🤩: Absolutely. Opensource is NOT only about the code. You can,
> - Improve the doc
> - Suggest Ideas
> - Test the app
> - Improve UX
> - Take part in discussions.

> Head over to our GitHub repo. The 🔗 is in comment below









> &mdash; ReactPlay.IO (@ReactPlayIO) April 23, 2022


A community grows with learning, sharing, and contributions. ReactPlay project team is proud to have 15+ contributors since we started a month back in April 2022. You folks are rockstars 🌟 🌟🌟.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654544432781/5E_UJsGQq.png align="left")

I wish to change the above image every week as we get more contributors. Last updated: 21st May 2022 🤩

# The Future of ReactPlay

The ```ReactPlay``` project is still at its early stage and running several proofs-of-concept. We are damn serious about growing it further with ideas, features, and engagements. We are working on these top-5 priority features currently,

- Integrating an Authentication System.

- Persisting the Play data in a Data Store.

- Ability to Like Plays.

- Show Trending Plays with an Automated Algorithm.

- Create a Leader Board to Encourage Play Creators.

We will also make changes in the way plays are architected at the code level. Lots of exciting pieces to come, and you can play a significant role in them.

- Join us in ideating on our Discussion Board.

- Feel free to create an issue for a bug or feature request.

- Helps us build our top-5 features.

- Create plays, and write about them.

- Join the Code Review board.

That's all for now. I'm proudly submitting this article as part of the "The Epic Hashnode Writeathon!" under the THW Web Apps category. Let's learn, share, and build the ReactPlay community together for the ReactJS Developers.

<hr />

I share my knowledge on,

- 🌐 Web Development(JavaScript, ReactJS, Next.js, Node.js, so on...)

- 🌱 Opensource

- ✍️ Content Creation

Let's connect,

[Give a Follow on Twitter](https://twitter.com/Programing_Pro)
[Subscribe to my YouTube Channel](https://www.youtube.com/channel/UC1YTVmV31RZV2oie1kKpJkw)
[Side projects on GitHub](https://github.com/Programming-School-Pro-Coding)
[Showwcase React Community](https://www.showwcase.com/community/react.js)
