# Lab Setup Guide

Set up a local SQL Server with a sample database for the user research session.

**Time required:** ~10 minutes

---

## Before You Start

Make sure you have these installed:

- [Visual Studio Code](https://code.visualstudio.com)
- [Docker Desktop](https://www.docker.com/products/docker-desktop) — must be **running**

---

## Step 1: Install the SQL Server Extension

1. Open VS Code
2. Press `Ctrl+Shift+X` (Windows/Linux) or `Cmd+Shift+X` (Mac) to open Extensions
3. Search **SQL Server (mssql)**
4. Click **Install**

---

## Step 2: Create a Local SQL Server Container

1. In VS Code, find the **SQL Server** panel in the left sidebar
2. Click **New Deployment**

   ![New Deployment button](assets/images/image1.png)

3. Select **Create a Local Docker SQL Server**
4. Click **Get Started**, then **Next** after Docker checks pass
5. Configure your container:

   ![Container settings](assets/images/image5.png)

   | Setting | What to enter |
   |---------|---------------|
   | **SQL Server version** | Windows/Linux: `SQL Server 2025 - latest`<br>Mac: `SQL Server 2022 - latest` |
   | **Password** | Choose a password (you'll need this later) |
   | **License terms** | Check to accept |

6. Click **Create Container** and wait for it to finish

---

## Step 3: Create the Sample Database

1. Open the file [`scripts/AdventureWorksLT2022.sql`](scripts/AdventureWorksLT2022.sql) in VS Code
2. When prompted, connect to your local SQL Server
3. Run the script (`Ctrl+Shift+E` or click **Run**)
4. Wait ~2 minutes for it to complete

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Docker not running | Open Docker Desktop and wait for it to start |
| Can't find SQL Server panel | Make sure the extension installed correctly |
| Script runs slowly | This is normal — it takes about 2 minutes |
| Other extensions interfering | Try disabling non-essential extensions |

---

## Need Help?

- [Video walkthrough](http://aka.ms/vscode-mssql-container-demo)
- [Documentation](http://aka.ms/vscode-mssql-container-docs)
