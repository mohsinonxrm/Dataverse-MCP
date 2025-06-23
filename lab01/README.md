# 🛠️ Lab 01 - Setting up your Dataverse environment & install the Dataverse MCP Local Proxy
In this lab, you will learn how to setup a Dataverse environment so that you can use the Dataverse MCP Server. Also, you will learn how to install the Dataverse Model Context Protocol server.

## 🌎 Provision Dataverse environment
To use these labs, you need to make sure to have created an environment with Dataverse enabled. You can create an environment via [Power Platform Admin Center](https://aka.ms/ppac). When creating the environment, make sure to set the `Add a Dataverse data store?` toggle to **Yes**.

After the creation of the environment, select the cog wheel (⚙️) at the top right and select **Session details**. Copy the Tenant ID and store it somewhere safe - you will need this later.

Wait until the environment is created before you move on to the next step.

## ➕ Create a connection to Dataverse on your environment
Navigate to https://make.powerautomate.com – just open another tab in the browser with Dataverse maker portal. If necessary, change to the correct environment by selecting it from the top right again. 

Select `More` and pin `Connections` by selecting the thumbtack to make sure the connections are pinned to the left navigation.

![Pin connections](./assets/pin-connections.png)

Select `Connections` on the left navigation.

![Connections](./assets/connections.png)

Click **+ New connection** at the top, type `Dataverse` into the search box

![New connection](./assets/new-connection.png)

Select the one with the green Dataverse icon. 

![Create connection Dataverse](./assets/create-connection-dataverse.png)

Select create in the pop up:

![Create Dataverse](./assets/create-dataverse.png)

Select your user to complete. You will see something like this: 

![Connection created](./assets/connection-created.png)

> [!TIP]
> Note the user name in the Connection Name – should be same as one you used already to provision Dataverse.

Select the username to open the connection.

![Select username](./assets/select-username.png)

Copy the Connection URL from the address bar and store it somewhere safe - you will need this later too.

![Copy connection URL](./assets/connection-url.png)

## ⚙️ Configure Dataverse MCP
First off, please install .NET SDK 8.0 with this Power Shell command.

1.	Install the .NET SDK 8.0 either from Downloads  or with this Power Shell command.

    ```powershell
    winget install Microsoft.DotNet.SDK.8
    ```

Go back to the Terminal window (or start new one as administrator) and run following command:

```powershell
dotnet tool install --global --add-source https://api.nuget.org/v3/index.json Microsoft.PowerPlatform.Dataverse.MCP
```

![dotnet tool installed successfully](./assets/dotnet-tool-install.png)

Great job! You’ve successfully completed configuration of Dataverse MCP server!

## ⏭️ Continue with Lab 02
👉 Go to [Lab 02](../lab02/README.md)

![🛠️ Lab 01 - Setting up your Dataverse environment & install the Dataverse MCP Local Proxy](https://m365-visitor-stats.azurewebsites.net/?resource=https://github.com/microsoft/Dataverse-MCP/tree/main/lab01)
