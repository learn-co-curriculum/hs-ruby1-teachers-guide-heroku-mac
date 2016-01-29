##Let's deploy!! 
[Heroku](https://www.heroku.com/) is a platform that allows for easy Command Line deployment of Ruby applications through integration with Github (as well as Node.js, Python, and Java and other languages).

Students are going to deply their applications using their own Heroku accounts.

###Setup
**1.** Students create their own [Heroku](https://www.heroku.com/) accounts

**2.** Students must download [Heroku Toolbelt](https://toolbelt.heroku.com/), which will allow you to deploy our applications through terminal.


**3.** Student's code must be up to date on Github. Heroku uses Github to deploy.

**4.** Students must create SSH keys and upload them to both Heroku and Github. You can read about creating SSH Keys [here](https://help.github.com/articles/generating-ssh-keys/).

###Deployment
+ In terminal, in the directory of your final project first enter: `heroku create`. 

+ This should prompt you to enter an email address. You'll enter your email address associated with your Heroku account and your Heroku password.
  * You should get a return that ends with `Git remote heroku added`.

+ At this point, Heroku will have generated a really weird name for your app, something similar to `thawing-ravine-1908`. 
 
+Then enter in terminal: `git remote -v` which should return the remote configuration of the heroku repository. You should see:

<img src="https://s3.amazonaws.com/after-school-assets/heroku-remote.png">

  * This creates an empty Heroku repository. 

+ To deploy, in temrinal enter `git push heroku master`. This takes your code from Github and pushes it to Heroku. You should see a successfull deploy. You can enter `heroku open` which should open your app in the browser.

+ If your app doesn't load in browser, enter in terminal `heroku logs`. You should start to see similar error messages to when you had problems with Shotgun. You can start to debug.


###To Deploy Changes
Once you deploy your project and make some changes, and then want to deploy those changes, your workflow in terminal will be:

```bash
git add file_name
git commit -m "commit message"
git push
git push heroku master
```

###Hints:
+ Deploy students apps one at a time. 
+ If a student opens their deployed app in the browser and sees an error instead of their page, enter `heroku logs` in terminal.
  * Scroll through the logs to find an error. Students will need to correct the error in their code and redeploy.

+ Students can run into errors in creating their SSH Key:
  * When they get prompted for where to save the SSH Key, the answer is literally provided for them in parentheses
  * The `pb copy...` actually copies their SSH Key for them, they just need to paste it into Heroku and Github.


<p data-visibility='hidden'>View <a href='https://learn.co/lessons/hs-ruby1-teachers-guide-heroku-mac' title='Let's deploy!!'>Let's deploy!!</a> on Learn.co and start learning to code for free.</p>
