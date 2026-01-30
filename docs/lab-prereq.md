# Lab Prerequisites - Detailed Guide

This guide walks you through setting up a local SQL Server environment using VS Code and Docker for the user research session.

**Expected time:** 10–15 minutes

---

## Overview

You will:
1. Install required software (VS Code, Docker Desktop)
2. Install the MSSQL extension for VS Code
3. Create a local SQL Server container
4. Load the AdventureWorks sample database

---

## Part 1: Install Prerequisites

### Visual Studio Code

Download and install from: https://code.visualstudio.com

### Docker Desktop

Download and install from: https://www.docker.com/products/docker-desktop

> Docker is required to run the local SQL Server container.

### MSSQL Extension for VS Code

1. Open VS Code
2. Open the Extensions view:
   - Windows/Linux: `Ctrl+Shift+X`
   - macOS: `Cmd+Shift+X`
3. Search for **"SQL Server (mssql)"**
4. Click **Install**

---

## Part 2: Create a Local SQL Server Container

### Step 1: Start New Deployment

1. In VS Code, locate the **SQL Server** view in the sidebar
2. Expand the **Connections** section
3. Click the **New Deployment** button (or select from the menu)

![New Deployment option in Connections view](../assets/images/image1.png)

### Step 2: Select Container Option

Select **Create a Local Docker SQL Server**.

![New SQL database options](../assets/images/image2.png)

### Step 3: Review Overview

Review the overview screen highlighting the local SQL Server container experience. Click **Get Started** when ready.

![Overview screen](../assets/images/image3.png)

### Step 4: Docker Prerequisites Check

The extension automatically checks for Docker:

- If Docker isn't installed, you'll see a message with an install link
- If Docker is installed but not running, you'll be prompted to start it

Wait for all checks to pass, then click **Next**.

![Docker prerequisite checks](../assets/images/image4.png)

### Step 5: Configure Deployment Settings

![Deployment settings panel](../assets/images/image5.png)

Configure the following:

| Setting | Value |
|---------|-------|
| **SQL Server version** | See OS note below |
| **SA Password** | Enter a strong password |
| **Profile Name** | Optional - name for your connection |
| **License terms** | Check to accept |

#### OS Note: SQL Server Version Selection

| Operating System | Recommended Version |
|-----------------|---------------------|
| Windows | SQL Server 2025 - latest |
| Linux | SQL Server 2025 - latest |
| macOS | SQL Server 2022 - latest |

> **macOS users:** SQL Server 2025 is not supported on macOS. Select SQL Server 2022.

**Advanced options** (optional):
- Container name
- Port
- Hostname

Click **Create Container** to proceed.

---

## Part 3: Load AdventureWorks Database

Once your container is running, load the sample database:

1. **Download the script**
   [AdventureWorksLT2022.sql](https://gist.github.com/croblesm/25c526d206ae1402b555837e9f17a302)

2. **Open in VS Code**
   Open the downloaded `AdventureWorksLT2022.sql` file

3. **Connect to SQL Server**
   Connect to your local SQL Server (created in Part 2)

4. **Execute the script**
   Run the script and wait for completion (~2 minutes)

> **Tip:** If other extensions are installed, they may interfere with database setup. Consider disabling non-essential extensions before proceeding.

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Docker not installed | Download from https://www.docker.com/products/docker-desktop |
| Docker not running | Open Docker Desktop and wait for it to start |
| Docker fails to start | Retry or restart your machine |
| Extension conflicts | Disable non-essential VS Code extensions |
| Script execution slow | Normal - takes approximately 2 minutes |
| Connection issues | Verify the container is running in Docker Desktop |

---

## Additional Resources

- [Container Setup Demo (YouTube)](http://aka.ms/vscode-mssql-container-demo)
- [Container Documentation](http://aka.ms/vscode-mssql-container-docs)
