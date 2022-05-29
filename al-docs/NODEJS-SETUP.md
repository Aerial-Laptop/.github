# NodeJS Setup
The following is general documentation for how to download, configure and run a **NodeJS** project from **Aerial Laptop**.

---
Clone Codebase
---
`git clone <repository>` [^1] the repository to your machine.

`npm i` in the working directory to install dependencies.

Configure
---
Depending on the project, it may have a configuration JSON file or dotenv.[^2]

**If `config.json` or `config/` directory:**

*Open the configuration file or directory and set all described parameters inside the JSON file(s).*

**If `.env.example`:**

*Run the command `mv .env.example .env` to use the example configuration. Then open .env and set your parameters (ex. `nano .env`).*

Run
---
The entry point for Aerial Laptop codebases is `main.js`

`node main.js`

It is highly recommended that you install [PM2 by Keymetrics](https://pm2.keymetrics.io), a node process manager.

`pm2 start main.js` [^3]

[^1]: The repository placeholder indicates the repository you want to clone. For example, a full command for cloning **Filing Saucer** would be `git clone https://github.com/Aerial-Laptop/Filing-Saucer.git`.
[^2]: Additional configuration may be required for your use case including items such as changing a splash screen or adding a content copyright notice.
[^3]: It is recommended to use the argument *name* when starting a process with PM2. This is done by appending it to the command to create `pm2 start main.js --name <codebase/instance name>`.
