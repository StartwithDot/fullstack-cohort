# Tools Setup — before Day 1

Install each tool and run its command in a new VS Code terminal. A version number confirms it worked.

## Node.js

1. Search for **Node.js download** and use the official Node.js site.
2. Install the current recommended version, then reopen VS Code.
3. Run:

```bash
node -v
npm -v
```

`node` runs JavaScript outside the browser; `npm` downloads project packages.

## MySQL

1. Search for **MySQL Community Server download** and use the official site.
2. Install the server and save the local administrator password securely.
3. Run:

```bash
mysql --version
```

If the command is not found, use [troubleshooting.md](troubleshooting.md).

## Git

1. Search for **Git download** and use the official site.
2. Install with standard options, then run:

```bash
git --version
```

## Visual Studio Code

1. Search for **Visual Studio Code download** and use the official site.
2. Open this repository as a folder, then choose **Terminal → New Terminal**.

Run the commands above again in a new terminal before starting [student-guide.md](student-guide.md).