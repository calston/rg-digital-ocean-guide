Rails on DigitalOcean guide
============================

## Create an account

Head to [https://www.digitalocean.com/go/app-platform](https://www.digitalocean.com/go/app-platform) and sign up for the 60 day free trial.

![Trial page](images/1.png)

Sign up using Github to link your account

![Github Authorization](images/githuboauth.png)

You will need a credit card but will receive $200 to start with if this is your first time using DigitalOcean.

![Complete signup](images/2.png)

## Create an application

Click on `Deploy a web application` to get started. 

![Deploy a web application](images/create-app-1.png)

Chose "Deploy your source code" to add an existing GitHub repository

![Deply source](images/create-app-2.png)

Authorize DigitalOcean to read your repositories

![Authorize DigitalOcean](images/create-app-3.png)

Select the repository for your application

![Choose repo](images/create-app-4.png)
![Choose branch](images/create-app-5.png)

Click `Next` to continue then `Edit Plan` to ensure we use the appropriate resources. We will start with a Basic plan and the smallest container size which should be sufficient.

![Container size](images/create-app-7.png)

Continue through the next steps until the end. We should not need to change anything else. 

![Environment](images/create-app-8.png)
![Region](images/create-app-9.png)

## Deploying our Rails application

Wait for the application to build, you can view realtime logs of the process while it happens. 

![Build](images/building.png)

If all went well you should see your application is available, however it still needs to be initialized and have a database added.

![Deployment](images/deploy.png)

Click on `Create` and `Create/Attach Database` to connect a Postgresql database.

![Database](images/database.png)

The application will automatically be configured with the database credentials

## Configuration
You can now head to the `Console` to access your application container and setup the database.

Type `rails db:migrate` into the terminal and press Enter. You should see the database being setup with the Rails schema.

![Migrate](images/migrate.png)

If all went well you should now be able to click on the `Live App` button which links to the live server.

![Tada](images/fin.png)
