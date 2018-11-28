# Linux Server Configuration

This is the first attempt at a remote deployment of the Wolfgang Bike Exchange; created in fulfillment of Udacity's Fullstack Nanodegree's final project.

## Specifications
- Server IP Address: `18.195.60.22`
- SSH Port: `2200`
- URL: `http://18.195.60.22.xip.io/`

## Summary & Steps
### Server Prep
- Created instance of Ubuntu on Lightsail
- Updated all installed packages
- Modified Lightsail Firewall to include non-standard SSH port
- Configured UFW to only allow specific ports
- Created `Grader` user
- Configured grader user's permissions to allow sudo
- Generated unique SSH Key-pair for grader

### Deployment
- Installed Apache to process the HTTP requests
- Created WSGI app container
- Installed PostgreSQL
- Installed Git
- Cloned bike-classifieds repo to `/var/www/`
- Installed all dependencies from the bike-classifieds projects listed fully in the `requirements.txt` file
- Created database file by running `database_setup.py`
- Moved database into sub-directory and modified permissions
- Disabled default .conf file
- Created `wolfgang.conf` to display my project

## References
- [Deploying python Flask web app on Amazon Lightsail](https://hk.saowen.com/a/0a0048ca7141440d0553425e8df46b16cdf4c13f50df4c5888256393d34bb1b9)
