# Run this cli from an EC2 instance running on same VPC as your RDS inatcnes.

This Script is tested with RDS instacne with postgres db v.16 and higher. I used EC2 with ubuntu latest image to test this.

# Use below commands to install dependencies.
sudo apt-get update
sudo apt-get install wget ca-certificates
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

sudo apt-get update
sudo apt-get install postgresql-client-16
pg_dump --version
psql --version

# install pip
apt install python3-pip

# install aws cli
sudo apt  install awscli -y

