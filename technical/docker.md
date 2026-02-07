Noah — 01:00
hmmm, here's a q - might post to the p5js chats, just check if ya got an idea
say you have a docker container with two p5js sketches in it
you want a simple no brainer 'webserver' in there to make both sketches appear at two urls
Eric — 01:02
sorry didn't see the soudn question, i have a toy implementation and i have a student doing one for the show
Noah — 01:02
is there a popular way to do that?
Eric — 01:02
right now these are node servers
say more, what are you trying to do with it
Noah — 01:03
not much more yet - just realized this is objective 👍
seeing a microservices type deal with three containers for old school
Eric — 01:04
you just bring up two node servers and run them on different virtural or real unix servers
Noah — 01:04
ahha yeah node sounds right - have never messed with
Eric — 01:04
it's not really a micro erver, just a general node server
a microserver would mean like different servers handle different parts of the game
that's probably not a great idea
Noah — 01:05
ok - i'll probly learn a bit about node - know zero about the js world
well - got dec10 running in a container today on macbook today, kinda micsrv1 - then ten robots running on macbook, kinda micsrv2 - then galaxy on macbook, kinda micsrv3?🤔
then watched a complete game happen all on my macbook 😄
Eric — 01:08
wow, that's cool
yea i mean node is pretty much javascript with some libs for http, etc
Noah — 01:08
one cool thing will be packaging up so people can run 'push button' anywhere
Eric — 01:08
well i guess more generally it is a javascript virtual machine running out of the browser
Noah — 01:08
k - thinking micserv3 will be pure js - so yeah node in there
https://github.com/decwarorg/utexas - pure stone age
https://github.com/decwarorg/merely-players - pure python robots, rest api 'cic'
https://github.com/decwarorg/galaxy - pure p5js
will start learnn a bit more about 'servn' with node for galaxy - thanks! 👍
ahha - here was first big step today - stone age in docker 😄 
https://github.com/decwarorg/utexas/-/blob/main/utexas.dockerfile?ref_type=heads
bit of manual stuff on top of this, but should be able to fully automate eventually
