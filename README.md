# profile

BUILDING APP

Index.html

Here i use FONTAWESOME'S cdn to use icons for my social media button links.

use cloudinary (https://cloudinary.com/) to store Profile pic. and put it into an open source Tool images.weserv. 
Know More to use it better way(https://images.weserv.nl/docs/)


CSS

import font family

use @media query to make it responsive according to display size

max-width : 500px (It means all these css Properties will apply till the width of display is under 500px  )

min-width : 50px (It means all these css Properties will apply till the width of display is more then 501px  )




DEPLOYING THE APP

We will deploy it on heroku 

first install docker on your machine  (https://docs.docker.com/engine/install/)

Create account on Heroku (https://signup.heroku.com/)
Install Heroku Cli for your OS ( https://devcenter.heroku.com/articles/heroku-cli ) 


Dockerfile 

Write Dockerfile in the root directory 

it will use nginx image 
Default working dir of nginix is /usr/share/nginx/html

Copy all the content which you want to render to working dir of Nginx

Now build your image using this Dockerfile, by { docker build . } 
Then run your newaly created image { docker run -p 80:80 imageID} -p flag is use for to map port
now do loacalhost in your browser 

  nginx.conf 
   
   This is the customized nginix configuration file which will replace content of the defalult configuration of nginix
 
   In nginx.conf we set PORT a variable Because Heroku give it's random port to the app, So we can not hardcode the port
   By default Nginix listion on the PORT 80,
    
   so usning sed -i command we have to set port in nginix default conf file { Read more about sed command https://linuxapt.com/blog/590-how-to-use-sed-command-to-delete-a-single-line-and-multiple-lines-in-linux-mint-20 }
   
We can deploy docker on heroku using two diffrent method
 1. Container Registry & Runtime (Docker Deploys) (https://devcenter.heroku.com/articles/container-registry-and-runtime)
 2. Building Docker Images with heroku.yml ( https://devcenter.heroku.com/articles/build-docker-images-heroku-yml )
   
   will follow 2nd method
   
  Now make heroku.yml in the root directory. IN heroku.yml file we can define our app.
 
  
   




