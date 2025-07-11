# 🛠️ Lab 01 - Setting up your Dataverse environment & install the Dataverse MCP Local Proxy
In this lab, you will learn how to setup a Dataverse environment so that you can use the Dataverse MCP Server. Also, you will learn how to install the Dataverse Model Context Protocol server.

## 🌎 Provision Dataverse environment
To use these labs, you need to make sure to have created an environment with Dataverse enabled. You can create an environment via [Power Platform Admin Center](https://aka.ms/ppac). When creating the environment, make sure to set the `Add a Dataverse data store?` toggle to **Yes**.

After the creation of the environment, go to [https://make.powerapps.com](https://make.powerapps.com), select the environment you just created, select the cog wheel (⚙️) at the top right and select **Session details**. Copy the Tenant ID and store it somewhere safe - you will need this later.

Wait until the environment is created before you move on to the next step.

## ➕ Create a connection to Dataverse on your environment

1. Go to [Power Automate](https://make.powerautomate.com). If necessary, change to the correct environment by selecting it from the top right.
1. Select **Connections** on the left navigation pane, and then select **+ New connection** on the command bar.
1. Type *Dataverse* in the search box, and then select the green colored **Microsoft Dataverse** connector.

    ![](./assets/power-automate-connector.png)

1. Complete the instructions on your screen.
1. Note the user name in the connection **Name**, this should be the same name that you used to create the environment earlier.
1. Select the connection to open it and copy the entire URL from the browser and save it. You need this URL for Claude desktop and VS Code MCP configuration.

    ![](./assets/copy-entire-browser-url.png)

## ⚙️ Configure Dataverse MCP

These steps install the Dataverse MCP server local proxy that is used by the MCP client, such as Claude desktop or VS Code GitHub Copilot.

1. Install the .NET SDK 8.0 either from Downloads or with this PowerShell command.

   `winget install Microsoft.DotNet.SDK.8`

1. In the Terminal window you opened earlier, run this command to install the Microsoft.PowerPlatform.Dataverse.MCP local proxy.

   `dotnet tool install --global --add-source https://api.nuget.org/v3/index.json Microsoft.PowerPlatform.Dataverse.MCP`

Great job! You’ve successfully completed configuration of Dataverse MCP server!

## ⏭️ Continue with Lab 02
👉 Go to [Lab 02](../lab02/README.md)

![🛠️ Lab 01 - Setting up your Dataverse environment & install the Dataverse MCP Local Proxy](https://m365-visitor-stats.azurewebsites.net/?resource=https://github.com/microsoft/Dataverse-MCP/tree/main/lab01)
