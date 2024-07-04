<div align="center">
  <a href="https://koyeb.com">
    <img src="https://www.koyeb.com/static/images/icons/koyeb.svg" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">Koyeb Serverless Platform</h3>
  <p align="center">
    Deploy a Ghost blog on Koyeb
    <br />
    <a href="https://koyeb.com">Learn more about Koyeb</a>
    ·
    <a href="https://koyeb.com/docs">Explore the documentation</a>
    ·
    <a href="https://koyeb.com/tutorials">Discover our tutorials</a>
  </p>
</div>


## About Koyeb and the Ghost example application

Koyeb is a developer-friendly serverless platform to deploy apps globally. No-ops, servers, or infrastructure management.  This repository contains a Dockerfile that allows you to deploy a Ghost blog on the Koyeb serverless platform.

This example launches a Ghost blog with [Cloudinary](https://cloudinary.com/), a digital asset management platform, to store uploads, a Mailgun account to send transactional and bulk emails, and a MySQL database to store user and application data.  You can follow the associated [tutorial](https://www.koyeb.com/tutorials/deploy-a-ghost-blog-in-production-to-koyeb) to learn more about the application and how to extend it.

## Getting Started

Follow the steps below to deploy and run Ghost on your Koyeb account.

### Requirements

You need a Koyeb account to successfully deploy and run this application. If you don't already have an account, you can sign-up for free [here](https://app.koyeb.com/auth/signup).

Additionally, you will need:

- A [Cloudinary](https://cloudinary.com/) account to store uploads and media.
- A [Mailgun](https://www.mailgun.com/) account to send transactional and bulk emails.
- A MySQL database for user and application data.

### Deploy using the Koyeb button

The fastest way to deploy the Ghost application is to click the **Deploy to Koyeb** button below.

[![Deploy to Koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?name=example-ghost&type=git&repository=koyeb%2Fghost&branch=main&builder=dockerfile&env%5Burl%5D=REPLACE_ME&env%5Bdatabase__connection__host%5D=REPLACE_ME&env%5Bdatabase__connection__port%5D=REPLACE_ME&env%5Bdatabase__connection__user%5D=REPLACE_ME&env%5Bdatabase__connection__password%5D=REPLACE_ME&env%5Bmail__options__auth__user%5D=REPLACE_ME&env%5Bmail__options__auth__pass%5D=REPLACE_ME&env%5BCLOUDINARY_URL%5D=REPLACE_ME&ports=2368%3Bhttp%3B%2F)

Clicking on this button brings you to the Koyeb App creation page with everything pre-set to launch this application.  Replace the values of the environment variables with your own information and deploy right away.

_To modify this application example, you will need to fork this repository. Checkout the [fork and deploy](#fork-and-deploy-to-koyeb) instructions._

## Configuration

When deploying Metabase on Koyeb, the following environment variables will be provided. Take care to set the required variables with the appropriate values if not set.

**Note:** All of the following environment variables are required.

- `url`: The URL where ghost will be accessible.Must have the format: `https://<YOUR_APP_NAME>-<KOYEB_ORG_NAME>.koyeb.app`.
- `database__connection__host`: The hostname where MySQL database is running.
- `database__connection__port`: The MySQL database port.
- `database__connection__user`: The MySQL database user.
- `database__connection__password`: The MySQL database password.
- `mail__options__auth__user`: Your Mailgun SMTP login.
- `mail__options__auth__pass`: Your Mailgun SMTP password.
- `CLOUDINARY_URL`: The Cloudinary connection URL.

## Fork and deploy to Koyeb

If you want to customize and enhance this application, you need to fork this repository.

If you used the **Deploy to Koyeb** button, you can simply link your service to your forked repository to be able to push changes.  Alternatively, you can manually create the application as described below.

On the [Koyeb Control Panel](https://app.koyeb.com/), on the **Overview** tab, click the **Create Web Service** button to begin.

1. Select **GitHub** as the deployment method.
2. In the repositories list, select the repository you just forked.
3. In the **Builder** section, select **Dockerfile**.
4. In the **Exposed ports** section, change the port value to **2368**.
7. In the **Environment variables** section, set the following environment variables:
    - `url`: The URL where ghost will be accessible.Must have the format: `https://<YOUR_APP_NAME>-<KOYEB_ORG_NAME>.koyeb.app`.
    - `database__connection__host`: The hostname where MySQL database is running.
    - `database__connection__port`: The MySQL database port.
    - `database__connection__user`: The MySQL database user.
    - `database__connection__password`: The MySQL database password.
    - `mail__options__auth__user`: Your Mailgun SMTP login.
    - `mail__options__auth__pass`: Your Mailgun SMTP password.
    - `CLOUDINARY_URL`: The Cloudinary connection URL.
8. Choose a name for your App and Service, i.e `example-ghost`, and click **Deploy**.

You will be taken to the deployment page where you can follow the build of your Ghost blog. Once the build is completed, your application will be deployed and you will be able to access it via `<YOUR_APP_NAME>-<YOUR_ORG_NAME>.koyeb.app`.

## Contributing

If you have any questions, ideas or suggestions regarding this application sample, feel free to open an [issue](https://github.com/koyeb/example-ghost/issues) or fork this repository and open a [pull request](https://github.com/koyeb/example-ghost/pulls).

## Contact

[Koyeb](https://www.koyeb.com) - [@gokoyeb](https://twitter.com/gokoyeb) - [Slack](http://slack.koyeb.com/)
