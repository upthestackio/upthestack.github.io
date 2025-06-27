# Kollect MCP Server

I have been building a little Cloud Inventory tool recently that grabs the inventory of your cloud based resources from AWS, Microsoft Azure, Google Cloud and then I also added some other useful platforms to gather an inventory for, Kubernetes, HashiCorp Terraform state files and HashiCorp Vault. I also have plans and a branch currently working to gather more information about Red Hat OpenShift. As well as the inventory we can also hunt for snapshots across these environments as well as explore costs.

We are using those platform APIs to gather them in one local API to quickly visualise the resources you have. Then I thought what would be interesting is the ability to interact with this centralised set of API endpoints and our inventory of data.

## MCP Servers

All the rage right now in the AI space,

***MCP is an open protocol that standardizes how applications provide context to LLMs. Think of MCP like a USB-C port for AI applications. Just as USB-C provides a standardized way to connect your devices to various peripherals and accessories, MCP provides a standardized way to connect AI models to different data sources and tools.***

This is the description used at [modelcontextprotocol.io](https://modelcontextprotocol.io/introduction)

It allows you to use an MCP client which really can be many different tools, for the purpose of this quick post, we are using Claude Desktop and VS Code as our client. You then have your MCP server, you can have many MCP servers for different tasks, think about that analogy used about USB, many USB devices do different things but they all connect via the USB port on your machine. Then some form of data source, in our case we want to hit the api with our inventory data.

![High level overview](/assets/blog/kollect-mcp-server/kollect-mcp-server-overview.png)

When you have all the above in place it then takes the context gathered from the /api endpoint and then uses that plus the natural language you have entered into the left client and then puts that to a large language model (LLM) and provides you feedback on that.

I am not going to go through the code base of this here, but it is worth noting that Kollect as a tool has been removed from a public repository due to some interactions and I honestly cannot be bothered with that engagement. The MCP server though can be found (as its own repository here)[https://github.com/MichaelCade/kollect-mcp-server] you will notice that I am leveraging a Go implementation of the MCP created by (mark3labs)[https://github.com/mark3labs/mcp-go] My intention is likely to build this server into the Kollect code base but for now it can be a boilerplate bit of code for me outside.

## Run Kollect

I think before we get into the MCP you have to have the Kollect tool running first and gathering information into one of those 3 API endpoints before we start the MCP Server, This is the order I tested things in so I am sticking with that.

This is not really a post about Kollect but you can run Kollect against all of your platforms using the --inventory all flag from the command line. You can also use --snapshots which will grab all snapshots from all available platforms.

or if you use --browser you can navigate and choose the platforms and function you wish to populate.

This will run on localhost:8080

and depending on your choosing you will have data in all or some of these endpoints

/api/data - Inventory Data from all or one platforms
/api/snapshots - Snapshots from ?PlatformType=aws,azure,gcp,kubernetes,all
/api/cost - Cost information from ?PlatformType=aws,azure,gcp,all

## Configure your Client

I will start with Claude Desktop, today is the first day I downloaded and installed Claude Desktop on my mac. You are going to want to find your claude_desktop_config.json, you can do this in Claude Desktop by heading to settings > developer and then edit config, open this file in your favourite text editor.

We then need to define where your MCP binary is, same process for all. You will see below the long path where my kollect-mcp-server binary is located, the kollect-server there is just a name for your MCP server.
```
{
  "mcpServers": {
    "kollect-server": {
      "command": "/Users/michaelcade/kollect-mcp-server/kollect-mcp-server",
      "args": [],
      "env": {}
    }
  }
}
```
Once you have the above, close Claude Desktop and reopen if the binary is there then you shouldnt see any errors, I have seen enough of them today. But things are working now.

![A running Kollect MCP Server in the wild](/assets/blog/kollect-mcp-server/claude-mcp-server-running.png)

## Kollect + MCP Interactions and Response

Ok So hopefully this is somewhat making sense, and the above steps have gone well. Now its time to get some insight from the MCP Server coupled with AI influence of an LLM. I don't show this but I have turned off web search in my configuration.

![My Claude Desktop with Kollect-MCP-Server](/assets/blog/kollect-mcp-server/claude-desktop-mcp-options.png)

So now we have our MCP running in Claude Desktop and Kollect is also running and we have data in our /api/data lets ask a question? Lets ask "How many EC2 instances do I have in my environments?" When the client knows it wants to use the MCP server it will prompt you here for permission to run it.

![Allow Kollect-MCP-Server](/assets/blog/kollect-mcp-server/kollect-mcp-claude-warning.png)

I selected Allow once, you can then see it provided me with a pretty good answer to my question.

![My first question Kollect-MCP-Server](/assets/blog/kollect-mcp-server/kollect-mcp-claude-answer.png)

We can also ask it to create a web report of all resources across all platforms.

![Web Report in Claude Desktop](/assets/blog/kollect-mcp-server/web-report.png)

You can then proceed to ask questions about costs and snapshots if those endpoints have been populated with data, maybe in the future we can make this a little more dynamic in that if we ask we can actually instruct kollect to go and get the information.

I also mentioned VS Code, if you are on mac you can get the following context with command + shift + P and then if you go through that configuration you be able to add the same as what we did with Claude Desktop although when you look at the settings.json it is slightly different.

![Add MCP to VS Code](/assets/blog/kollect-mcp-server/vs-code-add-mcp.png)

here is the settings.json found in your .vscode folder
```
"mcp": {
        "servers": {
            "kollect-server": {
                "type": "stdio",
                "command": "/Users/michaelcade/kollect-mcp-server/kollect-mcp-server",
                "args": []
            }
        }
```
Now using GitHub Copilot you can continue asking questions about your inventory.

![snapshots](/assets/blog/kollect-mcp-server/snapshots.png)

![costs](/assets/blog/kollect-mcp-server/costs.png)

I think that is enough ramblings for now, I expect this will be useful to me later on when I completely forget what I have built this morning.

Thanks for watching, smash that like button and hit that subscribe button.
