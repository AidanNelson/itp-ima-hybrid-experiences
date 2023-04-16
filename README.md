# Hybrid Learning and Social Experiences for ITP and IMA Community

This repository is an open source project intended for internal use within New York University's Interactive Telecommunications Program (ITP) and Interactive Media Arts (IMA) programs. Its purpose is to enable hybrid learning and social experiences for students and community members and to provide a test-bed for ongoing experiments with hybrid experience design and implementation.

Want to learn more? Visit [Hybrid at ITP/IMA](https://hybrid.itp.io).

## Contributing to the Codebase

This guide assumes some familiarity with your the command line (a text-based interface for your computer) and with web-development technologies. So when you see blocks of code below, these should be entered into your MacOS Terminal 💻 or Windows/Linux equivalents.

```sh
# download this repository and change directory (cd) into the root folder
git clone https://github.com/AidanNelson/itp-ima-hybrid-experiences.git
cd itp-ima-hybrid-experiences

# install all dependencies on the front end
npm install

# start the front-end development server
npm run watch

# You should now be able to access the venue from your web-browser at http://localhost:1234/
```

In order to actually use this application, however, you will need to start the back-end server in a separate terminal

```sh
# enter into the /server folder and install all dependencies
# note that this may take several minutes as it will compile the Mediasoup package
cd server
npm install

# once everything has been installed, start the server from the root of the repository
cd ..
npm run start-server
```

The code is organized into a few different sections:

## Server

The backend Node.js server code is contained within the `/server` folder. The server manages all real-time communications between community members connected to the server. It uses the [Mediasoup Selective Forwarding Unit](https://mediasoup.org/) through the [Simple Mediasoup Peer Wrapper Library](https://github.com/AidanNelson/SimpleMediasoupPeer).

## Front End

There are several web pages available in the front-end. These are available at the following paths.

[App](./src/electron-app/) - This is the root folder for the Electron app, meant to be run on dedicated screens at ITP

[Web](./src/) - This is the root folder for the web app, meant to be accessed by remote community members.
