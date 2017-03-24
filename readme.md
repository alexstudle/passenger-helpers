# Phusion Passenger: helpers

[Phusion Passenger™](https://www.phusionpassenger.com/) is a web server and application server, designed to be fast, robust and lightweight. 

Phusion Passenger supports Ruby, Python, Node.js and Meteor, and is being used by high-profile companies such as **Apple, Pixar, New York Times, AirBnB, Juniper** etc as well as [over 350.000 websites](http://trends.builtwith.com/Web-Server/Phusion-Passenger).

**Learn more:** [Website](https://www.phusionpassenger.com/) | [Documentation & Support](https://www.phusionpassenger.com/support) | [Github](https://github.com/phusion/passenger) | [Twitter](https://twitter.com/phusion_nl) | [Blog](http://blog.phusion.nl/)

<a href="https://www.phusionpassenger.com"><center><img src="http://blog.phusion.nl/wp-content/uploads/2012/07/Passenger_chair_256x256.jpg" width="160" height="160" alt="Phusion Passenger"></center></a>

# Install Passenger

It can be used as Standalone solution, with Apache or Nginx. 
>More infos [here](https://www.phusionpassenger.com/library/walkthroughs/deploy/)

I choosed to use it as Standalone... :

```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 561F9B9CAC40B2F7`
sudo apt-get install -y apt-transport-https ca-certificates
```

```
sudo sh -c 'echo deb https://oss-binaries.phusionpassenger.com/apt/passenger xenial main > /etc/apt/sources.list.d/passenger.list'
sudo apt-get update
```

```
sudo apt-get install -y passenger
```

# Use and configure

The best way to use it as Standalone solution, is to create a `Passengerfile.json` at Project root !

Please refer to the Folders named by the language you wich to use to get a working config file...

# Run

As soon as Passengerfile.json is created and Passenger is installed, simply go to your application folder:

```
cd /var/www/html/Lab_
```
and run: 

### For NodeJS / Python / MeteorJS:

```
sudo passenger start
```
### For Ruby:

```
sudo bundle exec passenger start
```