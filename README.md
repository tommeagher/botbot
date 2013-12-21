

# botbot
## Thunderdome's helper in our IM channels
This is a version of GitHub's Campfire bot, [hubot](https://github.com/github/hubot). He's pretty cool.

This version is designed to be deployed on [Heroku](http://www.heroku.com). This README was generated for you by hubot to help get you started. Definitely update and improve to talk about your own instance, how to use and deploy, what functionality he has, etc!

## Commands for botbot
For users, here's a recent list of the commands that you can give to botbot. Note that right now, commands for botbot only work in public channels and not in private messages or discussions. 

    applause|applaud|bravo|slow clap - Get applause
    beer me - Grab me a beer
    bees - Oprah at her finest, or a good way to turn the fans on coworkers machines
    dance - Display a dancing Carlton
    debug - {user: <user object to send message to>}
    gob it - Display a GOB
    botbot 9gag me - Returns a random meme image
    botbot <user> doesn't have <role> role - Removes a role from a user
    botbot <user> has <role> role - Assigns a role to a user
    botbot <user> is a badass guitarist - assign a role to a user
    botbot <user> is not a badass guitarist - remove a role from a user
    botbot I need some advice
    botbot abstract <topic> - Prints a nice abstract of the given topic
    botbot animate me <query> - The same thing as `image me`, except adds a few parameters to try to return an animated GIF instead.
    botbot ascii me <text> - Show text in ascii art
    botbot catfact - Reply back with random cat fact.
    botbot convert me <expression> to <units> - Convert expression to given units.
    botbot die - End botbot process
    botbot echo <text> - Reply back with <text>
    botbot fake event <event> - Triggers the <event> event for debugging reasons
    botbot forget <key> - Removes key from botbots brain.
    botbot github search [repo] <query> - Search for <query> in [repo] or anywhere
    botbot help - Displays all of the help commands that botbot knows about.
    botbot help <query> - Displays all help commands that match <query>.
    botbot how do you handle (.*)
    botbot image me <query> - The Original. Queries Google Images for <query> and returns a random top result.
    botbot kitten bomb me <number> - Many many kittens!
    botbot kitten me - A randomly selected kitten
    botbot kitten me <w>x<h> - A kitten of the given size
    botbot map me <query> - Returns a map view of the area returned by `query`.
    botbot math me <expression> - Calculate the given expression.
    botbot mustache me <query> - Searches Google Images for the specified query and mustaches it.
    botbot mustache me <url> - Adds a mustache to the specified URL.
    botbot ping - Reply with pong
    botbot pug bomb N - get N pugs
    botbot pug me - Receive a pug
    botbot random memory - Returns a random string
    botbot remember <key> - Returns a string
    botbot remember <key> is <value>. - Returns nothing. Remembers the text for next time!
    botbot repo commiters <repo> - shows commiters of repository
    botbot repo show <repo> - shows activity of repository
    botbot repo top-commiters <repo> - shows top commiters of repository
    botbot show <chat user's> issues -- Lists all issues for chat user IFF botbot_GITHUB_USER_(.*) configured
    botbot show [me] [<limit> [of]] [<assignee>'s|my] [<label>] issues [for <user/repo>] [about <query>] -- Shows open GitHub issues for repo.
    botbot show [me] issues -- Lists all issues IFF botbot_GITHUB_REPO configured
    botbot show [me] issues for <repo> -- List all issues for given repo IFF botbot_GITHUB_USER configured
    botbot show [me] issues for <user/repo> -- List all issues for given repo
    botbot show storage - Display the contents that are persisted in the brain
    botbot show users - Display all users that botbot knows about
    botbot the rules - Make sure botbot still knows the rules.
    botbot time - Reply with current time
    botbot translate me <phrase> - Searches for a translation for the <phrase> and then prints that bad boy out.
    botbot translate me from <source> into <target> <phrase> - Translates <phrase> from <source> into <target>. Both <source> and <target> are optional
    botbot what are your favorite memories? - Returns a list of the most remembered memories.
    botbot what do you remember - Returns everything botbot remembers.
    botbot what do you think about (.*)
    botbot what role does <user> have - Find out what roles are assigned to a specific user
    botbot what should I do about (.*)
    botbot who has admin role - Find out who's an admin and can assign roles
    botbot who is <user> - see what roles a user has
    botbot youtube me <query> - Searches YouTube for the query and returns the video embed link.
    it's a trap - Display an Admiral Ackbar piece of wonder
    repo#nnn - link to GitHub issue nnn for repo project
    sarcastic applause|clap - Get sarcastic applause
    ship it - Display a motivation squirrel
    user/repo#nnn - link to GitHub issue nnn for user/repo project


## To set up your own hubot
If you'd like to run a hubot, there is a lot more documentation below. For a high-level overview: 

* you'll need to have Node and NPM installed locally. Here's [a great tutorial on setting that up](http://www.joyent.com/blog/installing-node-and-npm). 
* Start with the instructions here at the [Hubot repo](https://github.com/github/hubot/blob/master/docs/README.md). 
* Our botbot is running on Heroku, which is fairly easy to launch and maintain. There is great documentation on [how to create your Heroku Hubot app](https://github.com/github/hubot/blob/master/docs/deploying/heroku.md).
* Connect the bot on heroku to your messaging service. We're currently using a Hubot's adapter [to connect us to Slack](https://github.com/tinyspeck/hubot-slack), but there are [loads of adapters for other popular chat services](https://github.com/github/hubot/blob/master/docs/adapters.md).


## Environment Variables
For the [hubot scripts](http://hubot-script-catalog.herokuapp.com/) that we're currently running, you will need to configure several environment variables within Heroku. Right now, those include: 

    HEROKU_URL
    HUBOT_GITHUB_REPO
    HUBOT_GITHUB_TOKEN
    HUBOT_GITHUB_USER
    HUBOT_SLACK_BOTNAME: botbot
    HUBOT_SLACK_TEAM
    HUBOT_SLACK_TOKEN
    

## The standard documentation that came with botbot...
### Testing Hubot Locally
Once you're set up and installed, you can test your hubot by running the following.

    % bin/hubot

You'll see some start up output about where your scripts come from and a
prompt.

    [Sun, 04 Dec 2011 18:41:11 GMT] INFO Loading adapter shell
    [Sun, 04 Dec 2011 18:41:11 GMT] INFO Loading scripts from /home/tomb/Development/hubot/scripts
    [Sun, 04 Dec 2011 18:41:11 GMT] INFO Loading scripts from /home/tomb/Development/hubot/src/scripts
    Hubot>

Then you can interact with hubot by typing `hubot help`.

    Hubot> hubot help

    Hubot> animate me <query> - The same thing as `image me`, except adds a few
    convert me <expression> to <units> - Convert expression to given units.
    help - Displays all of the help commands that Hubot knows about.
    ...


### Scripting

Take a look at the scripts in the `./scripts` folder for examples.
Delete any scripts you think are useless or boring.  Add whatever functionality you
want hubot to have. Read up on what you can do with hubot in the [Scripting Guide](https://github.com/github/hubot/blob/master/docs/scripting.md).

### Redis Persistence

If you are going to use the `redis-brain.coffee` script from `hubot-scripts`
(strongly suggested), you will need to add the Redis to Go addon on Heroku which requires a verified
account or you can create an account at [Redis to Go][redistogo] and manually
set the `REDISTOGO_URL` variable.

    % heroku config:add REDISTOGO_URL="..."

If you don't require any persistence feel free to remove the
`redis-brain.coffee` from `hubot-scripts.json` and you don't need to worry
about redis at all.

[redistogo]: https://redistogo.com/

## Adapters

Adapters are the interface to the service you want your hubot to run on. This
can be something like Campfire or IRC. There are a number of third party
adapters that the community have contributed. Check
[Hubot Adapters][hubot-adapters] for the available ones.

If you would like to run a non-Campfire or shell adapter you will need to add
the adapter package as a dependency to the `package.json` file in the
`dependencies` section.

Once you've added the dependency and run `npm install` to install it you can
then run hubot with the adapter.

    % bin/hubot -a <adapter>

Where `<adapter>` is the name of your adapter without the `hubot-` prefix.

[hubot-adapters]: https://github.com/github/hubot/blob/master/docs/adapters.md

## hubot-scripts

There will inevitably be functionality that everyone will want. Instead
of adding it to hubot itself, you can submit pull requests to
[hubot-scripts][hubot-scripts].

To enable scripts from the hubot-scripts package, add the script name with
extension as a double quoted string to the `hubot-scripts.json` file in this
repo.

[hubot-scripts]: https://github.com/github/hubot-scripts

## external-scripts

Tired of waiting for your script to be merged into `hubot-scripts`? Want to
maintain the repository and package yourself? Then this added functionality
maybe for you!

Hubot is now able to load scripts from third-party `npm` packages! To enable
this functionality you can follow the following steps.

1. Add the packages as dependencies into your `package.json`
2. `npm install` to make sure those packages are installed

To enable third-party scripts that you've added you will need to add the package
name as a double quoted string to the `external-scripts.json` file in this repo.

## Deployment

    % heroku create --stack cedar
    % git push heroku master
    % heroku ps:scale app=1

If your Heroku account has been verified you can run the following to enable
and add the Redis to Go addon to your app.

    % heroku addons:add redistogo:nano

If you run into any problems, checkout Heroku's [docs][heroku-node-docs].

You'll need to edit the `Procfile` to set the name of your hubot.

More detailed documentation can be found on the
[deploying hubot onto Heroku][deploy-heroku] wiki page.


### Deploying to UNIX or Windows

If you would like to deploy to either a UNIX operating system or Windows.
Please check out the [deploying hubot onto UNIX][deploy-unix] and
[deploying hubot onto Windows][deploy-windows] wiki pages.

[heroku-node-docs]: http://devcenter.heroku.com/articles/node-js
[deploy-heroku]: https://github.com/github/hubot/blob/master/docs/deploying/heroku.md
[deploy-unix]: https://github.com/github/hubot/blob/master/docs/deploying/unix.md
[deploy-windows]: https://github.com/github/hubot/blob/master/docs/deploying/unix.md

## Campfire Variables

If you are using the Campfire adapter you will need to set some environment
variables. Refer to the documentation for other adapters and the configuraiton
of those, links to the adapters can be found on [Hubot Adapters][hubot-adapters].

Create a separate Campfire user for your bot and get their token from the web
UI.

    % heroku config:add HUBOT_CAMPFIRE_TOKEN="..."

Get the numeric IDs of the rooms you want the bot to join, comma delimited. If
you want the bot to connect to `https://mysubdomain.campfirenow.com/room/42` 
and `https://mysubdomain.campfirenow.com/room/1024` then you'd add it like this:

    % heroku config:add HUBOT_CAMPFIRE_ROOMS="42,1024"

Add the subdomain hubot should connect to. If you web URL looks like
`http://mysubdomain.campfirenow.com` then you'd add it like this:

    % heroku config:add HUBOT_CAMPFIRE_ACCOUNT="mysubdomain"

[hubot-adapters]: https://github.com/github/hubot/blob/master/docs/adapters.md

## Restart the bot

You may want to get comfortable with `heroku logs` and `heroku restart`
if you're having issues.