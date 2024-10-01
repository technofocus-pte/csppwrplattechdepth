<img src="./media/f206b6dee2c05a2ab4b21406bb71a625d19df3c4.png"
style="width:6.26042in;height:2.41667in" />  

# Level-up CSP Technical Training – Power Platform Facilitator Guide  **

## Custom Copilot for Enhanced Customer Experience

## Lab Guide for Retail Scenario

| Description | This scenario extends the functionality of the Virtual Assistant copilot for Contoso Electronics, initially developed to assist customers with product discovery and post-purchase activities like return eligibility and refund requests. The enhancement introduces automated case escalation, allowing the copilot to seamlessly transfer conversations to live agents when it cannot resolve a query or when the customer requests human assistance. This ensures a more personalized and efficient customer service experience by blending automated responses with human support for complex issues. |
|:---|:---|
| Prerequisites | To get the most out of this lab guide we recommend you must develop copilot use case 2 (Build a copilot for your customer’s webpage), Microsoft dynamic 365 Customer Service trial license, Copilot Studio, Power Pages trial license and Admin Tenant ID - Password. |
| Duration | 30 mins |
| Version | 1.0 |
| Publication date  | September 2024 |

This document is provided “as-is”. Information and views expressed in
this document, including URL and other Internet Web site references, may
change without notice. You bear the risk of using it. 

This document does not provide you with any legal rights to any
intellectual property in any Microsoft product. You may copy and use
this document for your internal reference purposes. 

 

© 2024 Microsoft. All rights reserved.  



# **Objective & Scenario**

## Objective

This is an extension of **Use Case 2**, where we developed a standalone
Virtual Assistant copilot for Contoso Electronics' webpage to help
customers discover the best products based on their needs and
preferences, as well as manage post-purchase activities such as
verifying return eligibility and submitting refund requests seamlessly.
In this use case, the goal is to enhance the copilot by introducing
automated case escalation to live agents when the copilot cannot resolve
a customer’s issue or when the customer requests human support.

## 

## Solution Focus Area

In **Use Case 2**, the copilot was created and published on Contoso
Electronics' website to assist customers with product discovery and
post-purchase processes like returns and refunds. Now, the focus shifts
towards **enhancing customer support** by enabling the copilot to
smoothly escalate conversations to live agents when required. This
ensures that customers receive timely and effective assistance when the
virtual assistant alone is not sufficient.

The enhancement will focus on:

1.  **Automated Case Escalation**: Automatically transitioning the
    conversation to a live agent when the copilot cannot provide
    relevant information or fully address the customer’s concern.

2.  **Live Agent Requests**: Allowing customers to request live agent
    assistance at any point during their interaction with the copilot,
    ensuring they can access human support when needed.

## Persona and Scenario

- **Remy Morris** - Digital Solutions Architect 

<!-- -->

- **Mark Brown** – Project lead 

<!-- -->

- **David Flores** – App developer 

<!-- -->

- **Jane Miller** – App tester 

- **Contoso Electronics Support Team** – Live Agents

- **Miriam Graham –** Customer

These personas will participate in the following sequential scenarios: 

- Remy Morris designs and plans the digital architecture to meet the
  business needs. He presents this framework to Mark Brown and helps him
  select the appropriate Power Platform tools for the implementation.

- Mark Brown provides David Flores with an overview of the selected
  tools and processes. This includes enhancing the virtual agent with
  the live agent feature using Copilot, Dynamics 365, and implementing
  the bot on the Contoso Electronics webpage.

- David Flores creates the virtual assistant, ensuring it meets all the
  requirements specified by Contoso Electronics. He then submits the
  developed assistant to Jane Miller for testing.

- Jane Miller conducts thorough testing and validation of the virtual
  assistant to ensure functionality and performance.

- Upon successful testing, Mark Brown officially deploys the virtual
  assistant with live agent features on the Contoso Electronics website.

- Miriam Graham initiates interaction with the Virtual Assistant Copilot
  to inquire about the return policy for her laptop due to
  unsatisfactory battery life. If the Virtual Assistant Copilot cannot
  resolve the issue completely or if Miriam prefers to speak with a
  human, the copilot escalates the conversation to a Live Support Agent.

- The Live Support Agents handle the escalation, addressing any complex
  issues or detailed inquiries. They ensure Miriam’s refund request is
  processed smoothly and promptly.


## Pre-requisites 

For this use case, all participants will need the following: 

- Admin Tenant ID and Password.

- Microsoft Copilot Studio Free Trial License

- Microsoft Dynamic 365 Customer Service Free Trial License

- Microsoft Power Pages

- Contoso Electronics Bot Use Case 2 (Build a copilot for your
  customer’s webpage)

**Note:** Please be aware that the user interface (UI) of Power Apps,
Copilot, Microsoft 365, Power Automate, and other related tools may
change over time as Microsoft continues to update its products. However,
the core concepts and logic behind their functionality will remain
consistent. The principles you learn in this lab can still be applied,
even if the UI looks different in the future.



# **Lab Instructions**

# Exercise1: Configure Copilot with Dynamics 365

In this exercise, you will set up Dynamics 365 for customer service by
signing in, creating a new workstream, and configuring a chat channel.
This process will enable you to integrate and manage customer
interactions efficiently using Dynamics 365’s capabilities.

## Task 1: Sign in to Dynamic 365 Customer Service

1.  Open your preferred web browser and navigate to
    <https://www.microsoft.com/en-us/dynamics-365/products/customer-service>

2.  On the homepage, click the **Try for free** button to initiate the
    process of signing up for a free trial of Dynamics 365 Customer
    Service.

<img src="./media/585ca016cd1e040c27372302b76435c84c136b03.png"
style="width:6.26806in;height:3.32708in" />

3.  After clicking the button, you will be redirected to a page where
    you need to enter your admin Tenant Email ID (Same Id as Use case
    2).

Note: This lab is the extended version of **Build a copilot for your
customer’s webpage lab,** please use same credential in both the lab.

4.  Once you have entered the ID, Select the checkbox and click on Start
    your free trial to proceed.

<img src="./media/3ccdfd3011924d9b9f9f41b272436cbdc9a47e96.png"
style="width:6.26042in;height:4.95833in" />

5.  Then Enter the password required for the login and then click on
    Sign in.

<img src="./media/a24b04e1411902ff0ef5f9fc9a6af9b1a1f15eee.png"
style="width:6.26806in;height:4.05903in" />

6.  On the next screen, you will be asked to provide additional details
    to complete the setup. Select **Country (We choose United States)**
    as **region**.

7.  Enter your **Phone Number** in the provided field for verification
    purposes. This helps Microsoft ensure that the trial is being
    accessed by genuine users.

8.  Once all information is entered, click on **Submit** to finalize the
    setup.

<img src="./media/e71cc0dcf52443db80249f7e1e817a530d637af2.png"
style="width:6.26806in;height:4.19167in" />

9.  After submission, you will be redirected to the Dynamics 365
    Customer Service home page.

10. Click on **Customer Service workspace** to explore the tools
    available.

<img src="./media/4a9275529a9827221709fbb3fd1df8af50ea4de6.png"
style="width:6.26806in;height:2.98125in" />

11. Locate and click on **Customer Service admin Center** within the
    workspace to configure settings, manage users, and customize your
    customer service setup.

<img src="./media/e63de255877073609436a9e48fa9564f41deb93b.png"
style="width:6.26806in;height:2.94931in" />

## Task 2: Manage a User in Omnichannel for Customer Service

1.  Start by accessing the **Dynamics 365 Customer Service admin
    center**.

2.  In the site map on the left, locate and select **User management**
    under the **Customer support group**.

3.  On the **User management** page, find the **Users** section.

4.  Click on the **Manage** button next to **Users** to open the list of
    users within your organization.

> <img src="./media/6ef1f9bf9d45c93f3709c2100b4c7046c8be6add.png"
> style="width:6.26042in;height:2.375in"
> alt="A screenshot of a computer Description automatically generated" />

5.  To focus on users who are part of the Omnichannel for Customer
    Service, click the dropdown next to **Enabled Users**.

6.  From the dropdown menu, select **Omnichannel Users**. This filters
    the list to show only those users who are active in the Omnichannel
    environment.

> <img src="./media/9fd2e6b0247e2696a21760e85bdf72d112d83ee5.png"
> style="width:6.26042in;height:2.96875in" />

7.  Click on the Omnichannel username to open the specific settings and
    configurations for that user. In our admin tenant, the **username**
    is displayed as **MOD Administrator**. If participants are using
    their admin Tenant ID, their username may be change and shows **like
    “John”, "Admin" etc.**  
      
    <img src="./media/43ba9bbb51e092bd0bb1f1060935b436c09943db.png"
    style="width:6.26042in;height:2.90625in"
    alt="A screenshot of a computer Description automatically generated" />

8.  Once you are on the user page, locate and select the **Omnichannel**
    tab. This tab contains settings specific to Omnichannel
    functionality, allowing you to manage how the user interacts within
    the Omnichannel environment.

> <img src="./media/cda841681665a38fac65c8bf914a0e66871ba349.png"
> style="width:6.26042in;height:3.4375in"
> alt="A screenshot of a computer Description automatically generated" />

9.  On the Omnichannel tab, you will confirm the following settings. If
    the current setting differs, please adjust the value as indicated
    below:

    1.  Capacity: Set the value to 100. This defines the user's workload
        capacity within the Omnichannel environment.

    2.  Default Presence: Set this to Available. This specifies the
        user's default status when logged into the Omnichannel system.

> <img src="./media/ff83e142df4a1d4bb8248166d40b290eaa8a1d29.png"
> style="width:6.26042in;height:2.5625in"
> alt="A screenshot of a computer Description automatically generated" />

10. Click on **Save and close** to finalize the user settings and exit
    the configuration page.

> <img src="./media/5ab0c62ddb5e228cedf7f943fbcc3263afcd04d7.png"
> style="width:6.26042in;height:2.55208in"
> alt="A screenshot of a computer Description automatically generated" />

## 

## Task 3: Create a New Workstream

1.  In the left navigation bar, click on **Workstream**, then click on
    **+ New Workstream** to create a new one.

<img src="./media/597dde8c87080746ae1fc53673ce3a9c565b922e.png"
style="width:6.26806in;height:2.77569in" />

2.  Enter **Contoso Agent** in the Name field.

3.  Select **Messaging** from the Type dropdown menu.

4.  Select **Chat** from the **Channel dropdown** menu.

5.  Select **Push** and **Choose Existing** (If already selected no need
    to perform this step).

6.  From the choose existing dropdown menu, select **Fallback-chat demo
    (1 user)**.

7.  Click **Create** to finalize the new workstream. You will be
    redirect to Contoso agent workstream.

<img src="./media/9f1edc19c3b429e4b5cc9d69894c6bbdfeac07e9.png"
style="width:6.26806in;height:2.93125in" />

## Task 4: Configure a New Channel

1.  In the **Contoso Agent** workstream, click on **Set up chat**.

<img src="./media/37b977c0e00b827cd3c72fd17fb583d33829db5b.png"
style="width:6.26806in;height:2.91389in" />

2.  Enter **Contoso Live Agent** as the name of the channel. Click
    **Next**.

<img src="./media/1b134a1463270d82e58d8687f948c23036bb145d.png"
style="width:6.26806in;height:2.98819in" />

3.  Enter **Contoso Agent** in the Title field. Click **Next** again.

<img src="./media/7dfaf4a4ec565f073ecde7c0b3a88688c69aa27c.png"
style="width:6.26806in;height:2.99653in" />

<img src="./media/f65a5cafa107b71c94edeb3e7b7e9d09eb375409.png"
style="width:6.26806in;height:2.97708in" />

4.  On the User Features page, turn off **File attachment** and **Voice
    and Video Call** options, then click **Next**.

<img src="./media/bbaed24c0c953b885ac6a19f8165a8d1ecbe580b.png"
style="width:6.26806in;height:2.97639in" />

5.  Click on the **Create Channel**.

<img src="./media/caa3161a0736872129d8b3e3a7ce65b42920c91b.png"
style="width:6.26806in;height:2.98403in" />

6.  Copy the widget code and click **Done**.

<img src="./media/e8b7c58ebb460968eb282d7e07fbe43a3dcd0ecd.png"
style="width:6.26806in;height:3.14514in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Logged into Dynamics 365 Customer Service and accessed the workspace

2.  Managed users in **Omnichannel**, optimizing their capacity and
    availability.

3.  Established "Contoso Agent" with messaging and chat channel
    settings.

4.  Set up "Contoso Live Agent" with specific features and obtained the
    widget code for integration.

This setup prepares Dynamics 365 for effective customer interaction
management.

# Exercise 2: Escalate Copilot and Connect Omnichannel

In this exercise, you'll enhance the functionality of your Copilot by
configuring escalation topics and establishing a connection with
Dynamics 365. You'll also activate the Copilot channel to ensure
seamless integration and communication with the customer engagement hub.

## Task 1: Configure Escalate Topic

1.  Navigate to **Copilot Studio** and sign in with same credential
    which use for the dynamic 365 Customer Service, Select the
    **CustomerService Trial** environment from top right option.

2.  Select your **Contoso Electronics Services Copilot**.

3.  In the top navigation bar, click on **Topics** (located next to the
    knowledge base).

<img src="./media/3c8e80337ef4585a04f989e77afd8e57ae64b451.png"
style="width:6.26806in;height:2.95625in" />

4.  Scroll down to locate the **Escalate** topic and select it to open
    the configuration.

<img src="./media/f944b19a0e0fd73b4dee5d1173610ecab8352e8a.png"
style="width:6.26806in;height:2.96042in" />

5.  In the topic canvas, find the **message node**.

6.  Click on the three dots next to the message node and choose
    **Delete** to remove it.

<img src="./media/f0bcc9d749d09f8e06cd4e7e4310d12b18ef4899.png"
style="width:6.26806in;height:2.95208in" />

7.  Click on the **+ sign** below the trigger node to add a new node.

8.  Select **Topic Management** from the options.

9.  In the topic management options, select **Transfer Conversation** to
    create a new transfer node.

<img src="./media/16d35c0e168412ccfca64823141a168b55e62c01.png"
style="width:6.26806in;height:2.97153in" />

10. Once the **Transfer Conversation** node is added, click the **Save**
    button to save the configuration changes.

<img src="./media/c58d99d15fc46db5561a27f5283eaaabb4268223.png"
style="width:6.26806in;height:2.93611in" />

## Task 2: Activate the Copilot Channel

1.  Navigate to **Copilot Studio** and open your **Contoso Electronics
    Services Copilot**.

2.  Click on the **Channel** next to the action button.

<img src="./media/436f5bfd7a61814229f6290b0e0466385946c72e.png"
style="width:6.26806in;height:2.94028in" />

3.  Scroll down and select **Customer Engagement Hub**.

<img src="./media/fe6cf007b27a7dc1467d9bd2fd29783474732994.png"
style="width:6.26806in;height:2.98056in" />

4.  Click **Connect** to create a connection with Dynamics 365.

<img src="./media/609a2771a61e2a703af52d0dabe500521d320860.png"
style="width:6.26806in;height:2.97708in" />

## Task 3: Publish Your Copilot

1.  Navigate to Overview section and In Microsoft Copilot Studio, look
    for the **Publish** button on the right side of the screen.

2.  Click on the **Publish** button to start the publishing process.

<img src="./media/ea792bcf25b77cb284c82020057a9d6a8f06ce5e.png"
style="width:6.26806in;height:2.95764in" />

3.  A confirmation dialog may appear. Select **Publish** again to
    finalize and publish your copilot.

<img src="./media/b164e1810c3e71ef548071334278a3b1451512aa.png"
style="width:6.26806in;height:2.97292in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Modified the "Escalate" topic by removing the message node and
    adding a Transfer Conversation node to facilitate escalation.

2.  Established a connection between the Copilot and Dynamics 365
    Customer Engagement Hub by selecting and connecting the channel.

3.  Completed the publishing process to make the Copilot live and
    available for use.

These steps enhance the Copilot's functionality and integration with
Dynamics 365, ensuring effective escalation handling and seamless
communication.

# Exercise 3: Add and Activate Copilot Bot in Dynamic 365 Customer Service

In this exercise, you'll integrate your Copilot bot into Dynamics 365 by
adding it to the Customer Service workspace. This process involves
connecting the bot to the existing workstream and verifying its
activation to ensure it is functioning correctly.

## Task 1: Add Bot in Dynamic 365 Customer Service

1.  Navigate to **Dynamic 365 Customer service** and click on **Customer
    Service workspace** to explore the apps.

<img src="./media/7a2191f8d1b7e40a8ae1e9f0dd47cdad75e0f1b3.png"
style="width:6.26806in;height:2.96181in" />

2.  Locate and click on **Customer Service admin Center** within the
    workspace.

<img src="./media/811780dfc92fffd5c79a1711aec29389d9ee8be8.png"
style="width:6.26806in;height:2.92014in" />

3.  In the left navigation bar, click on **Workstream**, then select the
    **Contoso Agent** workstream created earlier.

<img src="./media/052169492471244785381260da94c60fdd40dae7.png"
style="width:6.26806in;height:2.94306in" />

4.  At the bottom, click **Add Bot**.

<img src="./media/fe2773f2d9dffe1f45302289af239a391ca7aaf4.png"
style="width:6.26806in;height:2.975in" />

5.  Select **Contoso Electronics Services** and click **Connect**.

<img src="./media/f83a90a5fbc6450e854d8c56c261fd11e454b240.png"
style="width:6.26806in;height:2.98403in" />

## Task 2: Check Bot Connection

1.  In the left navigation bar, click on **Bot** and check that the
    **Contoso Electronics Services** bot is Connected.

<img src="./media/b0bf1d6f50d84f4cad53de93d546b1bf4237f97e.png"
style="width:6.26806in;height:2.93889in" />

<img src="./media/51340a7ebee049105e3ab02c58b464d406e35902.png"
style="width:6.26806in;height:2.85694in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Integrated the "Contoso Electronics Services" bot into the "Contoso
    Agent" workstream by connecting it within the Customer Service admin
    center.

2.  Verified that the bot is active and functioning correctly in the Bot
    section of the Dynamics 365 interface.

This process ensures that your Copilot bot is effectively integrated and
operational within Dynamics 365, ready to handle customer interactions
through the configured workstream.

# Exercise 4: Deploy Copilot on a Power Page Website

In this exercise, you'll deploy your Copilot bot onto a Power Page
website. This involves connecting the bot with Power Pages, adding the
necessary code to the website, and previewing it to ensure everything is
functioning as expected.

## Task 1: Connect Bot with Power Pages

1.  Visit
    <https://www.microsoft.com/en-us/power-platform/products/power-pages>
    and sign in with the ID and password which we use early exercises.

<img src="./media/eff5ab48cca2d16f3f06b39fbf2df3aada3be67a.png"
style="width:6.26806in;height:2.93889in" />

2.  From the top right corner, select the correct environment
    **CustomerService Trial.**

<img src="./media/08db682e9fd9e5974db153c305160c8a8c4b3edb.png"
style="width:6.26806in;height:2.99444in" />

3.  Scroll down and select **Start a template**.

<img src="./media/d94c442394c0d5951d553bf1948d009c9a8870cd.png"
style="width:6.26806in;height:2.9625in" />

4.  Choose a template, name the website **Contoso**, and click **Done**.

<img src="./media/67858d498a202d7cb4df0fb9d91db7b16a4756ca.png"
style="width:6.26806in;height:2.99722in" />

<img src="./media/58e762307b6b31ce65d6e8025fb29114dfb06a56.png"
style="width:6.26806in;height:2.77569in" />

5.  Click **Edit Code** and then **Open Visual Studio Code**.

<img src="./media/90c85679abf456c8926287b56f0069b798422306.png"
style="width:6.26806in;height:2.94792in" />

6.  Sign in to Visual Studio Code when prompted.

<img src="./media/6eb26dc79f2548b2b426c58b595aa6214cfbaa75.png"
style="width:6.26806in;height:2.91806in" />

7.  Paste the widget code (copied earlier) at the bottom of the website
    home page code.

<img src="./media/ef7d1d4b3d60ed2de1be3c38d6af95912db99c9c.png"
style="width:6.26806in;height:2.95347in" />

8.  Save the file with **Ctrl + S**. Return to the Power Pages window
    and click **Sync**.

<img src="./media/7797f76f5f3be00ec027e4b2126420aa43f473c3.png"
style="width:6.26806in;height:3.01111in" />

9.  Click **Preview** and then **Desktop** to preview the website. The
    **Contoso Agent** bot will appear at the bottom.

<img src="./media/b7dfd23654846e4a0f8f335316003a3100934bdc.png"
style="width:6.26806in;height:2.93125in" />

<img src="./media/9c45cbe14696f0b9eb9906f4bf25c9ab4d61602a.png"
style="width:6.26042in;height:2.94849in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Logged into Power Pages, created a website using a template, and
    integrated the Copilot bot by adding the widget code to the
    website's home page code.

2.  Saved the code changes, synced with Power Pages, and previewed the
    site to ensure the "Contoso Agent" bot appears and functions
    correctly.

This deployment ensures your Copilot bot is live and operational on the
Power Page website, providing a seamless customer interaction
experience.

# Test Live Agent

In this exercise, you'll test the live agent functionality by
interacting with the Contoso Agent bot deployed on the Power Pages
website. This will involve initiating a live agent chat request from the
website and managing the interaction within the Dynamics 365 Customer
Service workspace.

1.  Go to Dynamics 365 and select **Customer Service workspace** and
    then select **Customer Service workspace** App to open and explore
    the apps.

2.  In another window, open the Power Pages app and preview the website
    created in the previous step.

3.  Open **Contoso Agent** on the Power Pages website.

4.  Type **Live agent** in the chatbot.

<img src="./media/9c45cbe14696f0b9eb9906f4bf25c9ab4d61602a.png"
style="width:6.26806in;height:2.95208in" />

<img src="./media/93590dbac3fe92881532bb35202075fa14f53ba8.png"
style="width:6.26806in;height:2.95208in" />

5.  Open a new window, go to the Dynamic 365 customer service and click
    on the customer service admin center the app window will open. In
    App window select Customer Service Workspace.

6.  The live agent chat request will be sent to the **Customer Service
    workspace,** where the live agent can accept or reject the request.
    (If request not seen there, refresh the power page preview and again
    type live agent in the Contoso chat bot).

<img src="./media/7810d5d661259fdb00f5b06fd0909e6fe4d63714.png"
style="width:6.26806in;height:2.98958in" />

7.  Live agent accepts the request and start conversation.

<img src="./media/31023645d58c16610eadcfca52e17ffa7b3dc2bf.png"
style="width:6.26806in;height:2.78403in" />

8.  Customer reply to live agent.

<img src="./media/7712799364c2ae24fae189f5c9a87e8a59e25357.png"
style="width:6.26806in;height:2.89861in" />

9.  Contoso Electronic live agent replies.

<img src="./media/f97cf2523eceb8e14643178fbc3dd75635277b47.png"
style="width:6.26806in;height:2.76458in" />

# Final Conclusion

In conclusion, the comprehensive steps undertaken in configuring and
deploying Dynamics 365 and the Copilot have led to a highly efficient
and integrated customer service solution.

1.  **Configured Dynamics 365:** Successfully signed in, created a new
    workstream, and configured a chat channel to manage customer
    interactions efficiently.

2.  **Enhanced Copilot Functionality:** Configured escalation topics
    connected the Copilot with Dynamics 365 and activated the Copilot
    channel to streamline customer service operations.

3.  **Integrated Copilot Bot:** Added and verified the Copilot bot
    within the Dynamics 365 Customer Service workspace, ensuring it was
    properly connected and active.

4.  **Deployed Copilot on Power Pages:** Connected the bot with Power
    Pages, integrated it into the website, and previewed the deployment
    to confirm its functionality.
