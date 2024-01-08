# my-sentry-docker
How to deploy sentry on your local system

# Stable Requirements
- v24.0.0+ Docker version 
- v2.21.0+ Docker Compose
- 4 CPU Cores
- 16 GB RAM
- 20 GB Free Disk Space

###### Note: The minimum requirements are lower. These requirements have been chosen to avoid build-in incompatibilities.


## Step 1 - Get Latest sentry repo
```
$ git clone https://github.com/getsentry/self-hosted.git
```

## Step 2 - change directory and permissions
```
$ cd self-hosted
$ sudo chmod -R 777
```
## Step 3 - Env vairables (Optional)
- You can create your custom env variables. It can be used to connect to external Redis, Kafka, etc.
- Environment specific configurations can be done in the ```.env.custom``` file. It will be located in the root directory of the Sentry installation, and if it exists then ```.env``` will be ignored entirely
- By default, there exists no ```.env.custom``` file. In this case, you can manually add this file by copying the ```.env``` file to a new ```.env.custom``` file and adjust your settings in the .env.custom file.

## Step 4- Install
```
$ ./install.sh
```
###### Note: You should create a user while installing

## Step 5 - Create User
- You will be prompted to create a user
- Type user ID - email
- Type password

###### Note - you will use this user and pass to log in after sentry is up and running.

## Step 6 - Run
```
docker compose up -d
```

## Step 7 - Launch
```
http://127.0.0.1:9000
```


###### Reference - https://develop.sentry.dev/self-hosted/


