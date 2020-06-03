# Software engineering lessons:

## Tasks needed to perform when working in a new project(the order is important):
1. Read the existing code and docs
2. Make sure I understand how the system works, draw a diagram ow r¡write w my words how I understand it works
3. Draw or write down my suggested design/solution
4. If I'm not 100% confidence my solution is the best possible discuss w a co worker
5. Once the right design/solution was found: put headphones on and code.

## Constantly ask for feedback and set goals:
Don't wait for your managers to give it, some nay forget it and over time not receiving feedback reduces the motivation to keeping improving so ask for feedback at least once a month and make sure you and your manager have clear goals for you in the Company. In the second startup I worked for this only aspect is what killed my motivation and ended up quitting with a very degraded performance and confidence about my work after 2 years of not asking for feedback. 


## Pieces of advice  gave me in my second startup:

- Communicate when I check out 
- Call him or any coworker when they don't reply and if they're blocking me
- Prioritize only 1 task at a time, make sure the task I'm working on right know is the most important


## how to solve a problem by my boss(teach leader) in one of my startups:

### This was extracted from an Slack conversation we had where he descibed the process he used to solve a technical problem:

the key is all about not jumping to conclusions or jumping to coding solutions, but trying to make sure to understand the real problem & trying to see the interesting properties of a problem.

This problem had a couple different issues - but you struggled with one, which is that the gmail api force you to fetch the full previous draft before appending anything.
So with files, this becomes a huge issue...
first thing i did was think about a solution to this, so decided to store in s3 to allow client to upload in parallel, and append at once when client would be ready to send the final outbound.
Second, files are big, and you don't want that in memory - so I just googled to see if we could uplaod in chunks (to be fair i remembered that we could) so will do that.
Then last friday i spent 3h reading thoruhg the crappy google doc to have a good sense of how gmail drafts & attachments works.
So i know i'll use nodemailer, & the resumable upload in google api.
Last concern is about cleaning the files in s3, but there is a built in s3 life cycle (i would have found that in google before implementing anything) but naive solution was to clean manually or cron job.
So bottom line, it's all about taking the time to understand the core of any problem, & trying to think about how to solve those.
If a solution isn't jumping to mind & you don't have time, try to do the naive solution, then iterate over that
That strategy always worked for me in problem solving
I personally wouldn't try to describe the problem with many detail, as that would be confusing, but instead try to describe the problem from another angle.
The first step to a problem solving, is simplifying the problem: isolate the parts that compose the problem, try to understand the problem from another perspective




