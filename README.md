# NUS-KIRO-IGNITE
Solution for SMEs to transform their existing Website to be AI Agent ready without much efforts

##Problem Statemement##
The web has been built primarily for human interaction, while the next generation of applications will increasingly be accessed by AI agents. Today, agents often have to scrape the DOM, interpret screenshots, and simulate clicks and form inputs—making interaction fragile, slow, and highly dependent on page structure.

With WebMCP, websites can expose structured, machine-readable tools and page states that AI agents can understand and interact with directly. This inspired us to ask: How can we make the billions of existing websites ready for this agentic web without forcing developers to rebuild them?

For example, current Republic Polytechnical pages, Student has to follow below steps:

1. Visit https://www.rp.edu.sg
2. Click on Lifelong Learning link
3. Click on Explore Course button
4. Select the course which is of interest
5. Click on "Register Interest" button
6. Fill in the details and click on "Submit" button


With WebMCP, the existing website can expose a structured tool interface to an AI agent. The agent can understand the available inputs, provide the required values, interact with the form, and execute the desired action - without manually hard-wiring the DOM elements or writing custom interaction scripts.

In essence, WebMCP turns “web pages built for humans” into “web pages ready for AI agents.”

##Solution
Our proposal is automating existing portals to become WebMCP ready for Agents to interact directly with the Website.

We are leveraging Kiro Powers which are modular capability packages for the Kiro AI-powered IDE that dynamically load specialized tools, steering files, and Model Context Protocol (MCP) servers only when relevant to your current task.

We have created KIRO Power named "NUS-KIRO-IGNITE" which will transform an existing portal to be WebMCP ready. It will read  exsiting web pages and enable WebMCP via Declarative API.

###Activation signals

Keywords:WebMCP
Typical prompts:Convert existing forms to be agent ready

###Examples

Prompt: Convert this html to WebMCP ready using Declarative API Expected outcome: Forms will have Tools tag added

Scenario Detection & Steering File Selection Enable WebMCP → enable-webmcp.md

Load when user mentions:

"WebMCP", "enable WebMCP", "webmcp"

###KIRO Powers structure is as following:

NUS-KIRO-IGNITE
|
 --- powers.md
 --- steering.md
    |
     - enable-webmcp.md

NUS-KIRO-IGNITE contains one steering file "enable-webmcp.md" which performs following operation:

**Phase 1: Prerequisites Check**

Before enabling Application Signals, verify:

The """HTML""" file is present
It is a valid """HTML"""
Check Form element present

**Phase 2: Enabling WebMCP**

Check the URL https://developer.chrome.com/docs/ai/webmcp/declarative-api
Use the Declarative API to transform standard HTML forms into WebMCP tools by adding annotations
Modify the """HTML""" file forms to become Tools
