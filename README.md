# visionBoard

A Pinterest-style content discovery and pinning app built with Node.js, Express, MongoDB, and EJS. Users can register, create boards, save and organize pins, follow other users, like and comment on content, and explore a feed of pins from people they follow. Image uploads go through Cloudinary. Auth is handled by Passport.js with session-based login.

Currently server-side rendered with EJS. A migration to React is planned, along with AI-powered content recommendations.

## Features

**Auth**
Users register with email and password. Passport.js handles login, session management, and route protection. Sessions are stored in MongoDB so they persist across server restarts.

**Boards & Pins**
Users create boards to organize content and save pins to them. Each pin supports an image (uploaded to Cloudinary), a title, description, and link. Pins can be saved, unsaved, liked, and commented on.

**Social**
Users can follow and unfollow each other. Following someone brings their pins into your explore feed. Profile pages show a user's boards, pins, followers, and following count.

**Search**
Search works across both pins (by keyword/tag) and users (by username or name). Results render instantly on the same page without a full reload.

**Profile**
Users can edit their display name, bio, and profile photo. Profile photo uploads also go through Cloudinary.

## Project Structure

visionBoard/
├── bin/              # Server startup script (www)
├── public/           # Static assets — CSS, client-side JS, images
├── routes/           # Express route files — auth, pins, boards, users, search
├── views/            # EJS templates — layouts, partials, and page views
├── app.js            # Express app setup, middleware, session config, route mounting
├── .env              # Environment variables (not committed)
└── package.json


**Why EJS?** This was built as a server-rendered app where each page is rendered on the server and sent as HTML. It works well and keeps the architecture simple — no separate frontend build step, no API layer needed. The tradeoff is that interactivity is limited without adding client-side JS on top.


## Tech Stack

Node.js · Express.js · MongoDB · Mongoose · EJS · TailwindCSS · Passport.js · Cloudinary · Multer · Express-Session


## Getting Started

bash
git clone https://github.com/Samadali123/visionBoard.git
cd visionBoard
npm install


Create a `.env` file in the root:

.env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
SESSION_SECRET=your_session_secret

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret


Start the server:

bash
npm start


App runs at `http://localhost:5000`.


## Apis Overview
Users Apis
Pins Apis
Comments Apis


## Roadmap

**React migration** — replacing EJS templates with a React frontend. The plan is to convert the app into a proper API + SPA architecture: Express serves JSON, React handles rendering. This gives full control over interactivity and state without the limitations of server-rendered templates.

**AI features** — once on React, the plan is to add AI-powered pin recommendations based on what users save and engage with, and smart search that understands intent rather than just matching keywords.


## Topics

nodejs` `expressjs` `mongodb` `ejs` `tailwindcss` `passport` `cloudinary` `pinterest-clone` `session-auth` `fullstack`



## Author

Syed Samad Ali — [LinkedIn](https://www.linkedin.com/in/syedsamad125)
