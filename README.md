### Brief

This will allow you to deploy an unlimited number of ipython notebook docker instances to a dokko-configured server. In other words.

1. Clone this repository
2. Add a dokku remote endpoint
3. Push 

That's it. You'll have an ipython notebook (with no bells or whistles) running at the subdomain you've defined at your dokku remote. 



### Details

1. Get an instance & domain setup. If you're new to digital ocean, sign up using my referral: [https://www.digitalocean.com/?refcode=67d148a44422](https://www.digitalocean.com/?refcode=67d148a44422). It's cheaper than EC2 in my experience. Use your own DNS though as theirs takes a long time to propagate. 

2. Follow this tutorial to setup dokku on DigitalOcean: [https://medium.com/code-adventures/438bce155dcb](https://medium.com/code-adventures/438bce155dcb)

3. Clone this repository

	git clone https://github.com/richstoner/ipython-dokku.git
	
4. Add a dokku remote endpoint

	git remote add dokku git@YOURDOMAINHERE:ipython
	
5. Push to the new endpoint

	git push dokku master
	
6. Wait a few moments (~80 seconds), then visit your new ipython notebook running in docker, via dokku, on digital ocean. 

	http://ipython.YOURDOMAINHERE
	

Remember - this is a barebones install of ipython notebook, but once it's running, you can easily install additional python dependencies via pip within the notebook itself.




### Next steps

1. Package a few more modules so it doesn't require extra installs within the notebook
2. Add a password configuration script
3. Write a frontend that does steps 2-5 for you.