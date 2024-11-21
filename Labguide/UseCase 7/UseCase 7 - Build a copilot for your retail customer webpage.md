<img src="./media/image1.png" style="width:6.1875in;height:2.39583in" />

# Level-up CSP Technical Training – Power Platform Facilitator Guide

## Build a copilot for your retail customer webpage

## Lab Guide for Retail Scenario

| Description | Develop a Virtual Assistant copilot for Contoso Electronics' website to enhance customer support by simplifying the laptop discovery process, providing tailored recommendations, and offering side-by-side device comparisons. The copilot will also inform customers about current deals, accessories, and protection plans. Additionally, it will assist with appointment scheduling for further consultation with sales associates. To streamline the post-purchase process, the copilot will provide information on Contoso’s return policies, check return eligibility, and enable customers to submit refund requests directly within the chat interface for a seamless user experience. |
|----|----|
| Prerequisites | To get the most out of this lab guide we recommend you have Work-School, Admin Tenant ID and Password. Trial access with Power Apps, Power Automate Flow, Copilot Studio, Lab Files (Refund Policy, Protection Plan, Sales and Promotions) |
| Duration | 90 mins |
| Version | 1.0 |
| Publication date  | October 2024 |

This document is provided “as-is”. Information and views expressed in
this document, including URL and other Internet Web site references, may
change without notice. You bear the risk of using it. 

This document does not provide you with any legal rights to any
intellectual property in any Microsoft product. You may copy and use
this document for your internal reference purposes. 

 

© 2024 Microsoft. All rights reserved.  

# **Objective & Scenario**

## Objective

Develop a standalone Virtual Assistant copilot for Contoso Electronics'
webpage to assist customers in discovering the best products based on
their specific needs and preferences, as well as handling post-purchase
activities like verifying return eligibility and submitting refund
requests seamlessly.

## Solution Focus Area

Contoso Electronics, a leader in consumer electronics, offers a wide
variety of devices and accessories, making it challenging for customers
to find the right product that meets their unique requirements and book
appointment for sales assistance. In addition, customers may need
assistance with returns and refunds for products that do not meet their
expectations.

Currently, customers face two main challenges:

1.  **Product Discovery:** Customers struggle with exploring the vast
    array of options, comparing specifications, protection plan and
    understanding promotions and deals, which delays purchasing
    decisions and book appointment for further sales assistance.

2.  **Return Process:** Customers experience difficulties in navigating
    Contoso’s return policies and efficiently submitting refund
    requests.

To enhance customer satisfaction and streamline both the discovery and
post-purchase processes, Contoso Electronics will deploy a Virtual
Assistant copilot on its website. This AI-powered assistant, enhanced
with knowledge sources, will assist customers from the initial product
discovery phase through to post-purchase services like returns and
refunds.

## Persona and Scenario

- **Remy Morris** - Digital Solutions Architect 

<!-- -->

- **Mark Brown** – Project lead 

<!-- -->

- **David Flores** – App developer 

<!-- -->

- **Jane Miller** – App tester 

- **Grady Archie –** Customer (Product Discovery)

- **Miriam Graham –** Customer (Refund Request)

These personas will participate in the following sequential scenarios: 

- Remy Morris, Digital Solutions Architect at Contoso Electronics,
  creates and plans digital architecture that aligns with the business
  need and articulates this framework to Mark Brown, the Project Lead at
  Contoso Electronics, and assists him in selecting the most suitable
  Power Platform tools for the implementation of the digital solutions. 

<!-- -->

- Mark Brown provides David Flores with an overview of the tools and
  processes involved in developing a virtual agent with copilot studio
  and power apps and creating a booking appointment and refund request
  flow using Power Automate. 

<!-- -->

- David successfully creates a virtual assistant, fulfilling all the
  requirements of Contoso electronics to provide virtual assistance for
  product information, booking assistance appointment and submit refund
  requests, which he then submits to Jane Miller for testing. 

<!-- -->

- After thorough testing and validation, Mark Brown officially deployed
  a virtual agent on Contoso electronics website for virtual assistance
  to the customer and streamline the refund or return process.

- Grady Archie, a returning student, visits the Contoso Electronics
  website to find a laptop for his studies, gaming, and video editing.
  He engages with the Virtual Assistant copilot and outlines his
  specific needs, including battery life, durability, and performance.
  The copilot provides him with recommendations, compares specs,
  highlights current deals on Microsoft Surface laptops, and suggests
  compatible accessories. Grady decides to purchase the Surface Laptop
  Studio 2 but opts to schedule an appointment with a sales associate
  through the copilot to finalize his decision.

- Miriam Graham, a frequent shopper, wants to return a laptop due to
  unsatisfactory battery life. She interacts with the Virtual Assistant
  copilot to check if she is eligible for a return. The copilot quickly
  accesses Contoso’s return policies and confirms her eligibility.
  Miriam then asks the copilot to assist with submitting a refund
  request. The copilot guides her through the form submission process,
  enabling her to complete the refund request within the chat window.

## Pre-requisites 

For this use case, all participants will need the following: 

- Work – School or Admin Tenant Email Id and Password.

- Microsoft Power Apps Free Trial License

- Microsoft Power Automate Free Trial License

- Microsoft Copilot Studio Free Trial License

- Refund Policy File

- Protection Plan File

- Sales and Promotion File

**Note:** Please be aware that the user interface (UI) of Power Apps,
Copilot, Power Automate, and other related tools may change over time as
Microsoft continues to update its products. However, the core concepts
and logic behind their functionality will remain consistent. The
principles you learn in this lab can still be applied, even if the UI
looks different in the future.

Lab Instructions

# Exercise 1: Signup and Build a Copilot in Microsoft Copilot Studio with New AI Capabilities

In this exercise, you will learn how to build and configure a copilot in
Microsoft Copilot Studio using its AI capabilities. You will begin by
signing into the platform, followed by creating and setting up a custom
copilot for Contoso Electronics Services. The tasks will cover
configuring security settings, enabling generative AI, and building a
knowledge base to empower the copilot to handle tasks like providing
information and booking appointments.

## Task 1: Sign In Copilot Studio

1.  Navigate
    to [https://copilotstudio.microsoft.com](https://copilotstudio.microsoft.com/) and
    click on **sign in.**

> <img src="./media/image2.png"
> style="width:6.26806in;height:2.85139in" />

2.  Enter **Email ID** (School, Work or Admin Tenant) which have access
    of Copilot Studio trial license and Power Apps trial license. For
    this lab we use Admin Tenant ID. Then click on **Next** button to
    proceed.

**Note:** To create Admin Tenant ID use the following link to set up a
new ID: [Create New
ID](https://go.microsoft.com/fwlink/?LinkId=2139833&ru=https%3A%2F%2Fwww.microsoft.com%2Fen-us%2Fdynamics-365%2Fproducts%2Fcustomer-service%3Ftsapp%3Dcustomerservice%26trialflow%3Dadmin&email=bumblebee.code%40outlook.com).
This will allow you to complete the registration and resolve any sign-in
issues.

> <img src="./media/image3.png" style="width:4.894in;height:1.96226in" />

3.  Enter the **Password** in the field and click on the **Sign in.**

> <img src="./media/image4.png"
> style="width:6.26806in;height:2.97917in" />

4.  In the **Welcome to Copilot Studio** popup, leave the country/region
    as the default value and select get started.

> <img src="./media/image5.png"
> style="width:6.26806in;height:2.96389in" />

5.  At the Welcome to Copilot Studio! popup, select **Skip**.

## Task 3: Create Contoso Electronics Services Copilot 

1.  Once logged in, make sure you are in the right environment. if not,
    please select the right environment **(Dev One).**

<img src="./media/image7.png"
style="width:6.26806in;height:2.85833in" />

2.  On the left navigation pane, find and click on **Create**. Then,
    select the **New Copilot** tile to begin the setup process.

> <img src="./media/image8.png" style="width:6.26806in;height:2.7991in" />

3.  When prompted, select **Skip to configure** to proceed without
    additional configuration options at this stage.

<img src="./media/image9.png"
style="width:6.26806in;height:2.78521in" />

4.  In the **Name** text box, type **Contoso Electronics Services**.
    This will be the name of your new copilot.

5.  In the **Description** text box, enter **“Provide information about
    laptops, refund or return policy, and facilitate booking or
    appointment.”** This description helps define the copilot’s role and
    functionality.

6.  In the **Instructions** text box, type “**Create a copilot for
    topics related to providing laptop information, processing refund
    request, and booking appointment with sales executives or for
    product returns.”** This guides the copilot in handling specific
    tasks and user interactions.

7.  Choose **English** from the language options. This will set the
    primary language for interactions with the copilot.

<img src="./media/image10.png"
style="width:6.26806in;height:2.76148in" />

8.  Finally, in the top-right corner of the screen, click on **Create**
    to finalize and deploy your new copilot.

<img src="./media/image11.png"
style="width:6.26806in;height:2.78893in" />

## Task 4: Configure Security and Generative AI

1.  In Microsoft Copilot Studio, locate and click on the **Settings**
    option in the top-right corner of the screen. This action will open
    the settings menu.

<img src="./media/image12.png"
style="width:6.26806in;height:2.82431in" />

2.  Within the settings menu, select the **Security** tab. This tab is
    specifically for configuring security options for your copilot.

3.  In the Security settings, find and select the **Authentication**
    tile. This section allows you to determine how users will
    authenticate to interact with your copilot.

<img src="./media/image13.png"
style="width:4.77797in;height:2.78333in" />

4.  Choose **No authentication** from the available options. This
    setting will allow unrestricted access to your copilot without
    requiring users to log in.

5.  Click **Save** to apply the authentication settings.

<img src="./media/image14.png"
style="width:4.75592in;height:2.7375in" />

6.  To ensure your changes have been saved, click **Save** again if
    prompted by the system.

<img src="./media/image15.png"
style="width:6.26806in;height:2.74191in" />

7.  On the left-hand side, above the Security tab, select **Generative
    AI**.

8.  For **“How should your copilot interact with people?”**, select
    **Generative AI** to **enable** this feature.

9.  For **“How strict should the content moderation be?”**, choose
    **Medium**. This setting balances content moderation with
    flexibility.

10. Click **Save** to apply these settings.

<img src="./media/image16.png"
style="width:4.77364in;height:2.81319in" />

11. After saving your settings, click **Close** to exit the settings
    window.

<img src="./media/image17.png"
style="width:6.26806in;height:2.76797in" />

12. In the Copilot pane on the left-hand side of the screen, select your
    copilot to return to the **Overview** tab. This will take you back
    to the main dashboard where you can manage your copilot.

## Task 5: Create Knowledge Base for Copilot

1.  Open Microsoft Copilot Studio and go to the **Overview** tab.

2.  Scroll down and **Disable** Allow the AI to use its own general
    knowledge (preview).

<img src="./media/image18.png"
style="width:6.26806in;height:2.75952in" />

3.  Navigate to the **Knowledge** section next to overview option and
    click on it.

4.  Click on the **+ Add Knowledge** button to begin adding new
    knowledge sources.

<img src="./media/image19.png"
style="width:6.26806in;height:2.74685in" />

5.  After selecting Add Knowledge, Select **Files** for the knowledge
    source.

<img src="./media/image20.png"
style="width:4.32235in;height:2.90833in" />

6.  Click on the **Browse** button to locate and select the **Refund
    Policy, Sales and Promotions and Protection Plan** lab file and
    click on **Open**.

<img src="./media/image21.png"
style="width:6.26806in;height:3.86944in" />

7.  Click **Add** to include this file as part of the copilot’s
    knowledge base.

<img src="./media/image22.png"
style="width:6.26806in;height:2.84306in" />

## Task 6: Publish Your Copilot

1.  After File are **Ready**, Go to **Publish** button on the right side
    of the screen. Click on the **Publish** button to start the
    publishing process.

<img src="./media/image23.png"
style="width:6.26806in;height:2.76319in" />

2.  A confirmation dialog may appear. Select **Publish** again to
    finalize and publish your copilot.

<img src="./media/image24.png"
style="width:6.26806in;height:2.32361in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Successfully created and deployed a custom copilot in Microsoft
    Copilot Studio.

2.  Configured security settings and enabled generative AI for
    intelligent interactions.

3.  Built a knowledge base to enhance the copilot's response
    capabilities.

4.  Published the copilot for real-time use in customer service tasks
    like product information, refunds, and appointment bookings.

# Exercise 2: Create and Manage Topics

This lab exercise focuses on the creation and management of various
topics using Copilot Studio. Participants will explore how to configure
a virtual assistant that responds to customer inquiries regarding
product information, laptop deals, comparisons, appointments, and
protection plans. Through practical tasks, learners will create topics
from scratch, set up trigger phrases, and utilize advanced options like
generative answers. By the end of this exercise, participants will
understand how to enhance customer interactions using dynamic responses
and structured conversations powered by AI, driving improved customer
engagement and automation.

## Task 1: Create a Topic "Product Information"

1.  Open Copilot Studio and select the copilot you've created for this
    project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/image25.png"
style="width:6.26806in;height:2.76912in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/image26.png"
style="width:6.26806in;height:2.78166in" />

4.  In the new topic canvas, at the top of the screen, enter the name of
    the topic **"Product Information"**.

<img src="./media/image27.png"
style="width:6.26806in;height:2.7761in" />

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

**Laptop Information, Information about laptop, Laptop Details, Laptop
Feature, Laptop Specification, Buy Laptop**

<img src="./media/image28.png"
style="width:6.26806in;height:2.79722in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Advanced options**, then choose **Generative
    Answer**. A Generative Answer node will be created.

<img src="./media/image29.png"
style="width:6.26806in;height:2.78611in" />

7.  In the Generative Answer node, click on the **Input** option
    variable window will open.

8.  In the **Select a variable** window, select **System** and scroll
    down to choose **Activity.Text**.

<img src="./media/image30.png"
style="width:6.26806in;height:2.77639in" />

9.  In the Generative Answer node, click on the **Edit** option in the
    **Data Source** section.

10. Enable the option **Search only selected sources**.

11. Choose the **Sales and Promotions** doc from the options displayed
    and scroll down.

12. In the **Content Moderation** section, select **Medium**.

13. Scroll up and click on the **(X)** to close Create generative answer
    properties window.

<img src="./media/image31.png"
style="width:6.26806in;height:2.76389in" />

14. Click on the **Save** button to save your configurations for the
    **"Product Information"** topic.

<img src="./media/image32.png"
style="width:6.26806in;height:2.79873in" />

## Task 2: Create “Student laptop deals” topic

1.  Open Copilot Studio and select the copilot you've created for this
    project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/image25.png"
style="width:6.26806in;height:2.76912in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/image26.png"
style="width:6.26806in;height:2.78166in" />

4.  In the new topic canvas, at the top of the screen, enter the name of
    the topic **"Laptop Deals"**.

<img src="./media/image33.png"
style="width:6.26806in;height:2.76042in" />

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

**Student laptop deals. Laptop deals, Deals, Deals about laptop, Product
deals, Latest deals, Current deals, Trending deals.  
**

<img src="./media/image34.png"
style="width:6.26806in;height:2.18264in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Advanced options**, then choose **Generative
    Answer**. A Generative Answer node will be created.

<img src="./media/image35.png"
style="width:6.26806in;height:2.31111in" />

7.  In the Generative Answer node, click on the **Input** option
    variable window will open.

8.  In the **Select a variable** window, select **System** and scroll
    down to choose **Activity.Text**.

<img src="./media/image36.png"
style="width:6.26806in;height:2.7375in" />

9.  In the Generative Answer node, click on the **Edit** option in the
    **Data Source** section.

10. Enable the option **Search only selected sources**.

11. Choose the **Sales and Promotions** doc from the options displayed
    and scroll down.

12. Scroll down, In the **Content Moderation** section, select
    **Medium**.

13. Scroll up and click on the **(X)** to close Create generative answer
    properties window.

<img src="./media/image37.png"
style="width:6.26806in;height:2.55278in" />

14. Click on the **Save** button to save your configurations for the
    **"Laptop Deals"** topic.

<img src="./media/image38.png"
style="width:6.26806in;height:2.55833in" />

## Task 3: Create a Topic “Compare laptop”

1.  Open Copilot Studio and select the copilot you've created for this
    project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/image39.png"
style="width:6.26806in;height:2.7433in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/image40.png"
style="width:6.26806in;height:2.77892in" />

4.  In the new topic canvas, at the top of the screen, enter the name of
    the topic **"Compare laptop"**.

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

> **compare laptop, compare product, laptop comparison, compare between
> laptops**

<img src="./media/image41.png"
style="width:6.26806in;height:2.76152in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Advanced options**, then choose **Generative
    Answer**. A Generative Answer node will be created.

<img src="./media/image42.png"
style="width:6.26806in;height:2.76638in" />

7.  In the Generative Answer node, click on the **Input** option
    variable window will open.

8.  In the variable window, select **System** and scroll down to choose
    **Activity.Text**.

<img src="./media/image43.png" style="width:6.26806in;height:2.773in" />

9.  In the Generative Answer node, click on the **Edit** option in the
    **Data Source** section.

10. Enable the option **Search only selected sources**.

11. Choose the **Sales and Promotions** doc from the options displayed
    and scroll down.

12. Scroll Down, In the **Content Moderation** section, select
    **Medium**.

13. Scroll up and click on the **(X)** to close Create generative answer
    properties window.

<img src="./media/image44.png"
style="width:6.26806in;height:3.82361in" />

14. Click on the **Save** button to save your configurations for the
    **"Compare Laptop"** topic.

> <img src="./media/image45.png"
> style="width:6.26806in;height:2.83002in" />

## Task 4: Create a Topic "Book Appointments"

1.  Open **Copilot Studio** and select the copilot you've created for
    this project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/image46.png"
style="width:6.26806in;height:2.75184in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/image47.png"
style="width:6.26806in;height:2.72047in" />

4.  In the new topic canvas, at the top of the screen, enter the name
    **"Book Appointments"**.

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

**Book an appointment, Schedule a meeting, Make a reservation, Set up an
appointment, Arrange a consultation, Virtual appointment, Appointment,
Schedule booking.**

<img src="./media/image48.png"
style="width:6.26806in;height:2.75964in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Send a Message Node,** a **Message Node** will be
    created. In the Message node, enter the following text:

Thank you for choosing our virtual assistant for your laptop
consultation. We are here to help you. To book a virtual appointment,
simply complete the form below.

<img src="./media/image49.png"
style="width:6.26806in;height:2.79011in" />

<img src="./media/image50.png"
style="width:6.26806in;height:2.68934in" />

7.  Below the Message node, click on the **+** sign to create a new
    node. Select **Ask with Adaptive Card**. An Adaptive Card Node will
    be created.

<img src="./media/image51.png"
style="width:6.26806in;height:2.75666in" />

8.  In the Adaptive Card node, select the **three dots** (More Options)
    and then select **Properties**.

<img src="./media/image52.png"
style="width:6.26806in;height:2.77288in" />

9.  In the Adaptive Card properties, below the **Edit JSON**. Paste the
    provided **JSON** code to create the adaptive card.

{

"\$schema": "<http://adaptivecards.io/schemas/adaptive-card.json>",

"type": "AdaptiveCard",

"version": "1.5",

"body": \[

{

"type": "TextBlock",

"text": "Virtual Assistant Booking",

"weight": "Bolder",

"size": "Large",

"horizontalAlignment": "Center"

},

{

"type": "Input.ChoiceSet",

"choices": \[

{

"title": "Virtual Showroom",

"value": "Virtual Showroom"

},

{

"title": "Customer Service",

"value": "Customer Service"

},

{

"title": "IT Support & Repair",

"value": "IT Support & Repair"

}

\],

"placeholder": "Placeholder text",

"id": "Appointmenttype",

"label": "Appointment Type",

"style": "expanded"

},

{

"type": "Input.Text",

"id": "fullName",

"placeholder": "Enter your full name",

"label": "Full Name",

"isRequired": true,

"errorMessage": "Full Name is required."

},

{

"type": "Input.Text",

"id": "contactPhone",

"placeholder": "Enter your phone number",

"label": "Phone Number",

"isRequired": true,

"errorMessage": "Phone Number is required."

},

{

"type": "Input.Text",

"id": "contactEmail",

"placeholder": "Enter your email address",

"label": "Email Address",

"isRequired": true,

"errorMessage": "Email Address is required.",

"style": "Email"

},

{

"type": "TextBlock",

"text": "Would you like to book a virtual appointment?",

"wrap": true,

"spacing": "Medium"

},

{

"type": "Input.Text",

"id": "appointmentDate",

"label": "Date",

"isRequired": true,

"errorMessage": "Date is required.",

"placeholder": "DD-MM-YYYY"

},

{

"type": "Input.ChoiceSet",

"choices": \[

{

"title": "12:00 PM",

"value": "12:00 PM"

},

{

"title": "01:00 PM",

"value": "01:00 PM"

},

{

"title": "02:00 PM",

"value": "02:00 PM"

},

{

"title": "03:00 PM",

"value": "03:00 PM"

},

{

"title": "04:00 PM",

"value": "04:00 PM"

},

{

"title": "05:00 PM",

"value": "05:00 PM"

}

\],

"placeholder": "Placeholder text",

"id": "appointmenttime",

"label": "Time",

"style": "expanded"

}

\],

"actions": \[

{

"type": "Action.Submit",

"title": "Book Appointments",

"data": {

"action": "bookAppointment"

}

}

\]

}

<img src="./media/image53.png"
style="width:6.26806in;height:2.77908in" />

10. Select **Variables** to open the Variables pane.

11. Select all the boxes on the right-hand side for the topic variables.

<img src="./media/image54.png"
style="width:6.26806in;height:2.76442in" />

12. Click on **Save** to save your configuration.

<img src="./media/image55.png"
style="width:6.26806in;height:2.79428in" />

13. Below the Adaptive card node, click on the + **sign** to create a
    new node. Select **Ask a Question**. A **Question Node** will be
    created.

<img src="./media/image56.png"
style="width:6.26806in;height:2.78109in" />

14. In question node select **Enter a Message** and enter the following
    text:

> Thank you, Full Name! Your Appointment Type appointment has been
> booked for Appointment Date at Appointment Time. Thank you for using
> our service.

<img src="./media/image57.png"
style="width:6.26806in;height:2.7741in" />

15. Replace the placeholders Full Name, Appointment Type, Appointment
    Date, and Appointment Time with the appropriate variables by
    clicking on the **{X}** icon and selecting the corresponding custom
    variables.

<img src="./media/image58.png"
style="width:6.26806in;height:2.76434in" />

16. In the Question node, select **Multiple Choice** as the identify.

17. In the **Options for user** section, enter the following choices:

    1.  **Yes**

    2.  **No**

<img src="./media/image59.png"
style="width:6.26806in;height:2.77761in" />

18. Below **Save the user's response** a new variable creates, click on
    the variable name (Var1), variable properties window will open,
    where you can rename the variable name with **AfterAppointment**.
    Click the **(X)** to close the variable properties window.

<img src="./media/image60.png"
style="width:6.26806in;height:2.75952in" />

<img src="./media/image61.png"
style="width:6.26806in;height:2.78758in" />

19. Under the **Yes** condition, click on the **+** sign and select
    **Topic Management**, then choose **Go to Another Topic**. A topic
    selection window will open—search for **Conversation Start** and
    select the **Conversation Start** topic.

<img src="./media/image62.png"
style="width:6.26806in;height:2.73864in" />

20. Under the **No** condition, click on the **+** sign and select
    **Send a Message**. A Message Node will be created. In the Message
    node, enter the following text:

> Thank you for using our service. Have a nice day.

<img src="./media/image63.png"
style="width:6.26806in;height:2.78109in" />

<img src="./media/image64.png"
style="width:6.26806in;height:2.7692in" />

21. Once all nodes are configured, click on **Save** to finalize and
    save your "**Book Appointments**" topic.

<img src="./media/image65.png"
style="width:6.26806in;height:2.78252in" />

## Task 5: Create Protection Plan Topic

1.  Open Copilot Studio and select the copilot you've created for this
    project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/image39.png"
style="width:6.26806in;height:2.7433in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/image40.png"
style="width:6.26806in;height:2.77892in" />

4.  In the new topic canvas, at the top of the screen, enter the name of
    the topic **"Protection Plan"**.

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

**Protection Plan, Laptop Protection Plan, Protection, Protect Plan**

<img src="./media/image66.png"
style="width:6.26806in;height:3.72639in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Advanced options**, then choose **Generative
    Answer**. A Generative Answer node will be created.

<img src="./media/image67.png"
style="width:6.26806in;height:3.78333in" />

7.  In the Generative Answer node, click on the **Input** option
    variable window will open.

8.  In the variable window, select **System** and scroll down to choose
    **Activity.Text**.

<img src="./media/image68.png"
style="width:6.26806in;height:3.52639in" />

9.  In the Generative Answer node, click on the **Edit** option in the
    **Data Source** section.

10. Enable the option **Search only selected sources**.

11. Choose the **Protection Plan** doc from the options displayed and
    scroll down.

12. In the **Content Moderation** section, select **Medium**.

13. Scroll up and click on the **(X)** to close Create generative answer
    properties window.

<img src="./media/image69.png"
style="width:6.26806in;height:3.14028in" />

14. Click on the **Save** button to save your configurations for the
    **"Protection Plan"** topic.

> <img src="./media/image70.png"
> style="width:6.26806in;height:3.77014in" />

## Task 6: Configure the Conversation Start Topic

1.  Navigate to Copilot Studio and select the Copilot you've created for
    this project.

2.  In the top navigation bar, select **Topics**, which is located next
    to **Knowledge**.

<img src="./media/image71.png"
style="width:6.26806in;height:2.76434in" />

3.  In the Topics section and select the **System** option to view the
    available system topics.

4.  Find and select the **Conversation Start** topic to open it.

<img src="./media/image72.png" style="width:6.26806in;height:2.804in" />

5.  Below the **Trigger** node, a message node is available. Replace the
    message with the given below content.

Hello! I am Contoso Virtual Agent. How May I Help You?

6.  Click the **Save** button to save your configuration.

<img src="./media/image73.png"
style="width:6.26806in;height:2.76291in" />

## Task 7: Configure the Conversational Boosting Topic

1.  Navigate to Copilot Studio and select the Copilot you've created for
    this project.

2.  In the top navigation bar, click on **Topics**, which is located
    next to **Knowledge**.

<img src="./media/image74.png"
style="width:6.26806in;height:2.78938in" />

3.  In the Topics section, select the **System** option to view the
    available system topics.

4.  Find and select the **Conversational Boosting** topic to open it.

<img src="./media/image75.png"
style="width:6.26806in;height:2.76638in" />

5.  In the **Generative Answer** node, click on **Edit** below the data
    source section.

6.  Toggle on the Search Only Selected Sources option.

7.  Select the **Refund Policy, Protection Plan and Sales and
    Promotions** doc knowledge base as the sources for search from.

8.  Scroll down in the Generative Answer properties window.

9.  In the Content Moderation section, select the **medium** option for
    content moderation.

10. Close the Generative Answer properties window once you're done.

11. Click on the **Save** button to save the configuration.

<img src="./media/image76.png"
style="width:6.26806in;height:3.39931in" />

## Task 8: Use Generative Answers in the System Fallback Topic

1.  In the Copilot pane on the left-hand side of the screen, select the
    copilot you've created to return to the **Knowledge** tab.

2.  Select the Topics tab located at the top of the screen.

<img src="./media/image77.png"
style="width:6.26806in;height:2.77422in" />

3.  Within the Topics tab, select the **System** option to view the
    available system topics.

4.  Find and select the **Fallback** topic to open it.

<img src="./media/image78.png"
style="width:6.26806in;height:2.76164in" />

5.  In the **Fallback** topic, locate the existing message node.

6.  Click on the three dots (•••) in the top-right corner of the message
    node and select **Delete** to remove it.

<img src="./media/image79.png"
style="width:6.26806in;height:2.74967in" />

7.  Below the Condition node, click on the + icon to add a new node.
    Select Advanced and then choose Generative answers from the options.

<img src="./media/image80.png"
style="width:6.26806in;height:2.75024in" />

8.  In the Generative answers node, for the Input field, select
    **Activity.Text** from the system variables.

<img src="./media/image81.png"
style="width:6.26806in;height:2.80698in" />

9.  Under the **Data sources** section, click on **Edit**.

10. Toggle on **Search only selected sources** to ensure that the AI
    pulls information only from specific knowledge sources.

11. From the list of available sources, select the **Refund Policy,
    Sales and Promotions and Protection Plan Doc** as the knowledge
    source.

12. Deselect the option **Allow the AI to use its own general
    knowledge** to ensure the AI only uses the specified knowledge
    source.

13. For Content moderation, select **Medium** to manage the level of
    content filtering.

14. After completing the above steps, click **Save** to save the
    generative answers configuration for the Fallback topic.

<img src="./media/image82.png"
style="width:6.26806in;height:3.35625in" />

## Task 9: Publish the Copilot

1.  In the Copilot Studio, find the **Publish** button. This button is
    typically placed on the right side of the window.

2.  Click on the **Publish** button.

3.  A confirmation window may appear; click **Publish** again to
    confirm.

<img src="./media/image83.png"
style="width:6.26806in;height:2.80061in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Successfully created and managed topics using Copilot Studio.

2.  Configured advanced nodes like generative answers and adaptive
    cards.

3.  Developed structured responses for topics like product information,
    deals, and appointments.

4.  Applied real-world use cases for enhanced customer engagement
    through Copilot.

5.  Gained a deeper understanding of how to automate and streamline
    customer service interactions using AI.

# Test the Copilot

To test the functionalities of your Copilot and Power Automate flows,
follow these steps:

Click on the three-dot right side of the window and select **Go to demo
website.** A demo website window will open start the conversation into
the website chat window.

**Note:** Testing Copilot with the same prompt multiple times may yield
varying responses due to contextual learning, dynamic data access, and
inherent randomness in its output generation.

<img src="./media/image84.png"
style="width:6.25972in;height:2.76744in" />

Once the demo website launch and message appear in chat box enter the
following trigger phrases to test the topics you created:

1.  What are some deals on student laptops right now?

<img src="./media/image85.png"
style="width:6.26806in;height:2.80208in" />

<img src="./media/image86.png"
style="width:6.26806in;height:2.67431in" />

2.  Tell me more about Surface Laptop Go 3. What are the specs & cost?

<img src="./media/image87.png"
style="width:6.26806in;height:2.96389in" />

<img src="./media/image88.png"
style="width:6.26806in;height:2.58056in" />

3.  Compare laptop surface laptop go 3 and surface laptop studio 2.

> <img src="./media/image89.png"
> style="width:6.26806in;height:2.97917in" />
>
> <img src="./media/image90.png"
> style="width:6.26806in;height:2.66111in" />

4.  I want to know about the protection plan?

<img src="./media/image91.png"
style="width:6.26806in;height:2.6625in" />

<img src="./media/image92.png"
style="width:6.26806in;height:2.80764in" />

# Exercise 3: Signup for Power App and Create Custom Table

In this exercise, you'll learn how to sign up for Microsoft Power Apps
and create a custom table by following a series of practical steps. The
exercise begins with signing into the Power Apps platform using the same
credentials as Copilot Studio and setting up the correct environment.
From there, you'll be guided through creating a new solution and
publisher within Power Apps. Once the solution is set, you will
configure it as your preferred choice. Finally, the exercise walks you
through the process of building a custom table, "Book Appointments,"
with specific columns to store appointment data. This hands-on exercise
provides essential experience with Power Apps, helping you understand
the core functionalities of creating and managing tables within a
solution.

## Task 1: Sign Up for Microsoft Power Apps

1.  Open your web browser and go to the
    <https://powerapps.microsoft.com/free/> page and from top right
    corner click on **Sign In**

<img src="./media/image93.png"
style="width:6.26806in;height:2.40694in" />

2.  Enter your same **Email ID** which use in Copilot studio. And then
    click on the **Next**.

<img src="./media/image94.png"
style="width:6.26806in;height:2.89514in" />

3.  Enter the **Password** and click on **Sign In**.

<img src="./media/image95.png"
style="width:6.26806in;height:3.16806in" />

4.  If you receive a prompt stating that you already have a Microsoft
    account associated with the entered email address, select **Sign
    in**. Enter your same **ID and Password** when prompted.

5.  After signing in, you may be prompted with an option to stay signed
    in. Select **Yes** to stay signed in for quicker access in the
    future.

<img src="./media/image96.png"
style="width:6.26806in;height:3.15486in" />

6.  Once you're signed in, look at the top-right corner of the screen.
    Choose the environment, we use **Dev One** environment for this lab,
    participants can use any development environment. This is important
    for the next steps, as you’ll need to select this environment when
    working in Power Apps.

<img src="./media/image97.png"
style="width:6.26806in;height:2.83125in" />

## Task 2: Create a Solution in Power Apps

1.  Once signed in Power Apps, In the left-hand navigation pane, find
    and select **Solutions**.

<img src="./media/image98.png"
style="width:6.26806in;height:2.50278in" />

2.  Once in the Solutions section, click on **+ New solution** to create
    a new solution.

<img src="./media/image99.png"
style="width:6.26806in;height:2.77431in" />

3.  In the **New solution** form, enter **Contoso Electronics** as the
    Display Name for your solution. This name identifies your solution
    within the environment.

4.  Next, you need to assign a publisher to your solution. Click on **+
    New publisher** to create a new one.

<img src="./media/image100.png"
style="width:6.26806in;height:2.79074in" />

5.  Fill in the following details in the publisher form:

    1.  **Display name**: Contoso

    2.  **Name**: contoso

    3.  **Prefix**: contoso

6.  After entering these details, click **Save**.

<img src="./media/image101.png"
style="width:6.26806in;height:2.975in" />

7.  Once the publisher is created, select **Contoso (contoso)** from the
    Publisher dropdown.

8.  Click on **Create** to finalize your new solution.

<img src="./media/image102.png"
style="width:6.26806in;height:2.79167in" />

9.  After creating your solution, click on **Back** in the left corner
    of the screen. This takes you back to the main Solutions page, where
    you can see your newly created solution listed.

<img src="./media/image103.png"
style="width:6.26806in;height:2.78611in" />

## Task 3: Set the Preferred Solution

1.  In the Power Apps Maker portal, navigate to the **Solutions**
    section in the left-hand menu.

2.  Locate the option **Manage** under **Current preferred solution**
    and click on it.

<img src="./media/image104.png"
style="width:6.26806in;height:2.75579in" />

3.  A list of available solutions will be displayed. Find and select
    **Contoso Electronic (contoso)** from the list.

4.  Once selected, click on **Apply** to set this solution as your
    preferred choice.

<img src="./media/image105.png"
style="width:6.26806in;height:2.78333in" />

## Task 4: Create the "Book Appointments" Table

1.  In the Power Apps Maker portal, select **Tables** from the left-hand
    navigation pane.

<img src="./media/image106.png"
style="width:6.26806in;height:2.78218in" />

2.  Click on **+ New table**, and then choose **Create new table** to
    start creating your new table.

<img src="./media/image107.png"
style="width:6.26806in;height:2.64861in" />

3.  Then select **Start from blank** to create a table.

<img src="./media/image108.png"
style="width:6.26806in;height:2.40833in" />

4.  By default, the new table will be named "**Table1**." Double click
    on table name and rename it to **Book Appointments**.

<img src="./media/image109.png"
style="width:6.26806in;height:2.52292in" />

5.  **Appointment Type Column:**

Click on the down arrow next to the first column, and then select the
edit column button.

<img src="./media/image110.png"
style="width:4.40356in;height:1.25338in" />

Change the display name to **Appointment Type** and click on **Update**.

<img src="./media/image111.png"
style="width:3.24047in;height:1.29031in" />

6.  **Full Name Column:**

Click on the **+ New column** button, change the display name to **Full
Name**, and save the column.

> <img src="./media/image112.png"
> style="width:4.39976in;height:1.71823in" />

7.  **Email Address Column:**

Click on the **+ New column** button, change the display name to **Email
Address**, and save.

<img src="./media/image113.png"
style="width:6.26806in;height:2.375in" />

8.  **Phone Number Column:**

Click on the **+ New column** button, change the display name to **Phone
Number**, and save.

> <img src="./media/image114.png"
> style="width:5.09924in;height:1.95466in" />

9.  **Date Column:**

Click on the **+ New** **column** button, change the display name to
**Date**, and save.

> <img src="./media/image115.png"
> style="width:6.26806in;height:2.50625in" />

10. **Time Column:**

Click on the **+ (add column)** button, change the display name to
**Time**, and save.

> <img src="./media/image116.png"
> style="width:6.26806in;height:2.27569in" />

11. After adding all the necessary columns, click on the **Save and
    exit** button to finalize and create the **"Book Appointments"**
    table.

<img src="./media/image117.png"
style="width:6.26806in;height:1.87778in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Successfully signed up for Microsoft Power Apps using Copilot Studio
    credentials.

2.  Created a new solution named "Contoso Electronics" with a custom
    publisher.

3.  Set the "Contoso Electronics" solution as the preferred solution in
    Power Apps.

4.  Built a custom table called "Book Appointments" with the required
    columns for managing appointments.

5.  Acquired foundational knowledge of Power Apps' environment,
    solutions, and table creation process.

# Exercise 4: Create Power Automate Flow and Integrate Actions

In this exercise, you will learn how to create a Power Automate flow and
integrate it with a Copilot action to automate the process of booking
appointments. By following the steps provided, you will configure a
custom flow that captures appointment details like date, time, and
contact information, and maps them into a Dataverse table. Once the flow
is set up, you will integrate it within Copilot Studio, allowing Copilot
to trigger the flow, gather input data from users, and complete the
appointment booking process seamlessly.

## Task 1: Create Power Automate Flow to Book an Appointment

1.  Go Back to Copilot studio Contoso Electronics Copilot, Select the
    **Actions** tab to start configuring actions for your Copilot.

<img src="./media/image118.png"
style="width:6.26806in;height:2.81389in" />

2.  Click on **+ Add an action**.

<img src="./media/image119.png"
style="width:6.26806in;height:2.81834in" />

3.  Scroll down and select **Create a new flow** a new Power Automate
    flow window will pop up. Check the environment of power automate
    from top right corner, if correct environment (Dev One) not
    selected, please select the correct environment.

<img src="./media/image120.png"
style="width:4.95098in;height:2.97708in" />

4.  Select **Run a flow from copilot** from top left corner and rename
    the flow as **Book Appointments Flow**.

<img src="./media/image121.png"
style="width:6.26806in;height:2.7694in" />

5.  Select the trigger step "**Run a flow from Copilot,"** and then
    select **+ Add an input**.

<img src="./media/image122.png"
style="width:6.26806in;height:2.79154in" />

6.  Select **Text** for the input type and configure the following
    inputs by repeating the process:

    1.  Enter **Type** in input field for Appointment Type

    2.  Enter **Date** in input field for Appointment Date

    3.  Enter **Email** in input field for Email Address

    4.  Enter **Name** in input field for Full Name

    5.  Enter **Phone** in input field for Phone Number

    6.  Enter **Time** in input field for Appointment Time

> <img src="./media/image123.png"
> style="width:6.26806in;height:2.63403in" />
>
> <img src="./media/image124.png"
> style="width:6.26806in;height:2.60355in" />
>
> <img src="./media/image125.png"
> style="width:6.26806in;height:2.76777in" />

7.  Click on the **+ icon** between the two steps in the flow and select
    **Add an action**.

<img src="./media/image126.png"
style="width:6.26806in;height:2.78685in" />

8.  In the **Search** field, type **Dataverse** and select **See more**
    for the Dataverse connector.

<img src="./media/image127.png"
style="width:6.26806in;height:2.78174in" />

9.  Select **Add a new row** action.

<img src="./media/image128.png"
style="width:6.26806in;height:2.78403in" />

10. Login with the same credential for the Oath Sign.

11. Choose **Book Appointments** for the table name.

<img src="./media/image129.png"
style="width:6.26806in;height:2.79154in" />

12. Select **Show all** to see all available fields.

<img src="./media/image130.png"
style="width:6.26806in;height:2.80184in" />

13. Use **Dynamic content** to map each input parameter to the
    corresponding field:

    1.  **Type** Dynamic Input → **Appointment Type** Parameter.

    2.  **Date** Dynamic Input → **Appointment Date** Parameter

    3.  **Email** Dynamic Input → **Email Address** Parameter

    4.  **Name** Dynamic Input → **Full Name** Parameter

    5.  **Phone** Dynamic Input → **Phone Number** Parameter

    6.  **Time** Dynamic Input → **Appointment Time** Parameter

> <img src="./media/image131.png"
> style="width:6.26806in;height:2.76785in" />
>
> <img src="./media/image132.png"
> style="width:6.26806in;height:2.68403in" />

14. Select **Respond to Copilot** action.

<img src="./media/image133.png"
style="width:4.21944in;height:2.80556in" />

15. Click on **Settings**.

16. Ensure that **Asynchronous Response** is set to **Off**.

<img src="./media/image134.png"
style="width:6.26806in;height:2.81667in" />

17. Select **Save draft**.

18. Then, click on **Publish**.

<img src="./media/image135.png"
style="width:6.26806in;height:2.80972in" />

19. Once the flow is published, close the Power Automate and return to
    Copilot Studio.

## Task 2: Create Action in Copilot for Book Appointments

1.  Go to copilot window and click on **Refresh**, (If the Copilot
    window was closed, reopen it and navigate back to the **Copilot
    Studio,** go to the **Actions** tab and click on **+ Add an
    action**.)

<img src="./media/image136.png"
style="width:4.91177in;height:2.97639in" />

2.  In the "**Choose an action**" window, select the **Book Appointments
    Flow** you created.

<img src="./media/image137.png"
style="width:4.93137in;height:2.95764in" />

3.  Click on **Next**, **next** then **Next** again, and finally
    **Finish**. The flow will now be added as an action.

<img src="./media/image138.png"
style="width:4.28646in;height:2.57251in" />

<img src="./media/image139.png"
style="width:4.08333in;height:2.43825in" />

<img src="./media/image140.png"
style="width:3.83333in;height:2.2754in" />

4.  Navigate to the **Topics** section and select the **Book
    Appointments** topic.

<img src="./media/image141.png"
style="width:6.26806in;height:2.75842in" />

5.  Below the Adaptive Card node, click on the **+** sign to create a
    new node.

6.  Select **Call an action**. Choose the **Book Appointments Flow**.
    This action will now be added below the Adaptive Card node.

<img src="./media/image142.png"
style="width:6.26806in;height:2.77917in" />

7.  In the action node, you need to map each input field to the
    appropriate variable created by the Adaptive Card:

    1.  **Type** Input: Click on the input field, then select
        **Appointmenttype** from the custom variables.

    2.  **Date** Input: Click on the input field, then select
        **appointmentDate** from the custom variables.

    3.  **Email** Input: Click on the input field, then select
        **contactEmail** from the custom variables.

    4.  **Name** Input: Click on the input field, then select
        **fullName** from the custom variables.

    5.  **Phone** Input: Click on the input field, then select
        **contactPhone** from the custom variables.

    6.  **Time** Input: Click on the input field, then select
        **appointmenttime** from the custom variables.

> <img src="./media/image143.png"
> style="width:6.26806in;height:2.80135in" />

8.  After mapping all the variables, click on the **Save** button to
    save the topic configuration.

<img src="./media/image144.png"
style="width:6.26806in;height:2.75882in" />

## Task 5: Publish the copilot

1.  From top right corner, go to publish and click on it.

<img src="./media/image145.png"
style="width:6.26806in;height:1.44306in" />

2.  Then again click publish for confirmation.

<img src="./media/image146.png"
style="width:6.26806in;height:2.04931in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Successfully created a Power Automate flow named **Book Appointments
    Flow**.

2.  Configured multiple input fields such as appointment type, date, and
    contact details.

3.  Mapped the inputs to corresponding Dataverse fields for appointment
    booking.

4.  Integrated the flow with Copilot Studio by adding it as an action.

5.  Ensured correct mapping of input variables within the Copilot topic.

6.  Published the flow and tested it within the Copilot environment for
    seamless integration.

# Test Copilot

To test the functionalities of your Copilot and Power Automate flows,
follow these steps:

Click on the three-dot right side of the window and select **Go to demo
website.** A demo website window will open start the conversation into
the website chat window.

**Note:** Testing Copilot with the same prompt multiple times may yield
varying responses due to contextual learning, dynamic data access, and
inherent randomness in its output generation.

<img src="./media/image84.png"
style="width:6.25972in;height:2.76744in" />

Once the demo website launch and message appear in chat box enter the
following trigger phrases to test the topics you created

1.  What are current student laptops deals?

<img src="./media/image147.png"
style="width:6.26806in;height:3.31736in" />

<img src="./media/image148.png"
style="width:6.26806in;height:3.45486in" />

2.  Book Appointment for further assistance

<img src="./media/image149.png"
style="width:6.26806in;height:3.17014in" />

Fill the complete form and click on the **Book Appointments**

<img src="./media/image150.png"
style="width:6.26806in;height:2.96736in" />

Ensure that the details entered in the Appointment Booking are
accurately reflected in the "Book Appointments" table in Power Apps.

<img src="./media/image151.png"
style="width:6.26806in;height:2.78333in" />

# Exercise 5: Create Power Apps Table for Refund Requests

In this exercise, you will learn how to create a custom table in Power
Apps for managing refund requests. The table will store key details such
as customer information, purchase data, and refund-related entries. By
following these steps, you'll understand how to add columns for specific
data fields like Full Name, Email, Order Number, and more. This hands-on
task will provide you with essential knowledge on table creation and
column management within Power Apps, preparing you to efficiently handle
refund processes in a structured format.

1.  Navigate to Power Apps, In the Power Apps Maker portal, select
    **Tables** from the left-hand navigation pane.

> <img src="./media/image106.png"
> style="width:6.26806in;height:2.77755in" />

2.  Click on **+ New table**, and then choose **Create new table** to
    start creating your new table.

<img src="./media/image107.png"
style="width:6.26806in;height:2.64861in" />

3.  Then select **Start from blank** to create a table.

<img src="./media/image108.png"
style="width:6.26806in;height:2.40833in" />

4.  By default, the new table will be named **"Table1."** Double click
    on Table 1 name and rename it to **Refund Requests**,

<img src="./media/image152.png"
style="width:6.26806in;height:1.54444in" />

5.  **Full Name Column:**

Click on the down arrow next to the first column, and then select the
edit column button.

<img src="./media/image153.png"
style="width:6.26806in;height:1.26273in" />

Change the display name to **Full Name** and click on **Update**.

<img src="./media/image154.png"
style="width:3.74537in;height:1.36851in" />

6.  **Date of Purchase Column:**

Click on the **+ New column** button, change the display name to **Date
of Purchase**, and save.

> <img src="./media/image155.png"
> style="width:6.26806in;height:2.30208in" />

7.  **Description Column:**

Click on the **+ New column** button, change the display name to
**Description**, and save.

> <img src="./media/image156.png"
> style="width:6.26806in;height:2.34028in" />

8.  **Email Column:**

Click on the **+ New column** button, change the display name to
**Email**, and save.

> <img src="./media/image157.png"
> style="width:6.26806in;height:2.29931in" />

9.  **Order Number Column:**

Click on the **+ New column** button, change the display name to **Order
Number**, and save.

> <img src="./media/image158.png"
> style="width:6.26806in;height:2.27431in" />

10. **Order Type Column:**

Click on the **+ New column** button, change the display name to **Order
Type**, and save.

> <img src="./media/image159.png"
> style="width:6.26806in;height:2.32847in" />

11. **Phone Number Column:**

Click on the **+ New column** button, change the display name to **Phone
Number**, and save.

> <img src="./media/image160.png"
> style="width:6.26806in;height:2.26319in" />

12. **Preferred Contact Method Column:**

Click on the **+ New column** button, change the display name to
**Preferred Contact Method**, and save.

<img src="./media/image161.png"
style="width:6.26806in;height:2.27222in" />

13. **Product Column:**

Click on the **+ New column** button, change the display name to
**Product**, and save.

> <img src="./media/image162.png"
> style="width:6.26806in;height:2.33889in" />

14. **Receipt Number Column:**

Click on the **+ New column** button, change the display name to
**Receipt Number**, and save.

<img src="./media/image163.png"
style="width:6.26806in;height:2.35417in" />

15. After adding all the necessary columns, click on the **Save and
    exit** button to finalize and create the **"Refund Request"** table.

> <img src="./media/image164.png"
> style="width:6.26806in;height:2.28958in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Successfully created a custom "Refund Requests" table.

2.  Learned how to rename default table names and columns.

3.  Gained experience adding new columns for various refund request
    details.

4.  Saved the table for future use in handling refund-related data in
    Power Apps.

# Exercise 6: Create and Manage Topics for Refund Request and Policy Information

In this exercise, you will create and manage two essential topics using
Copilot Studio for Contoso Electronics. The first topic will provide
information on the company's refund and return policies, while the
second will enable customers to submit a refund request. Through
step-by-step tasks, you will learn how to configure trigger phrases,
generative answers, and adaptive cards, which will enhance the customer
support experience by streamlining the handling of refund-related
queries. By the end of this exercise, you will have built robust
automation flows to efficiently manage refund and return inquiries.

## Task 1: Create a Topic "Refund or Return Policy Information"

1.  Open Copilot Studio and select the **Contoso Electronics Service**
    copilot.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/image39.png"
style="width:6.26806in;height:2.77761in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/image40.png"
style="width:6.26806in;height:2.75931in" />

4.  In the new topic canvas, at the top of the screen, enter the name of
    the topic **"Refund or Return Policy Information".**

<img src="./media/image165.png"
style="width:6.26806in;height:1.58194in" />

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

**Refund policy, Return policy, Can I return a product, What is your
return policy, How do I return an item, Returning a purchase,
Information about return policy,**

<img src="./media/image166.png"
style="width:6.26667in;height:2.08507in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Advanced options**, then choose **Generative
    Answer**. A Generative Answer node will be created.

<img src="./media/image167.png"
style="width:6.26806in;height:2.78742in" />

7.  In the Generative Answer node, click on the **Input** option
    variable window will open.

8.  In the variable window, select **System** and scroll down to choose
    **Activity.Text**.

<img src="./media/image168.png"
style="width:6.26806in;height:2.75331in" />

9.  In the Generative Answer node, click on the **Edit** option in the
    **Data Source** section.

10. Enable the option **Search only selected sources**.

11. Choose the **Refund Policy** Doc from the options displayed and
    scroll down.

12. In the **Content Moderation** section, select **Medium**.

13. Scroll up and click on the **(X)** to close Create generative answer
    properties window.

<img src="./media/image169.png"
style="width:6.26806in;height:3.45764in" />

14. Click on the **Save** button to save your configurations for the
    **"Refund or Return Policy Information"** topic.

<img src="./media/image170.png"
style="width:6.26806in;height:1.23958in" />

## Task 2: Create a Topic "Refund Request"

1.  Open **Copilot Studio** and select the copilot you've created for
    this project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/image171.png"
style="width:6.26806in;height:2.77761in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/image172.png"
style="width:6.26806in;height:2.77071in" />

4.  In the new topic canvas, at the top of the screen, enter the name
    **"Refund Request"**.

<img src="./media/image173.png"
style="width:6.26806in;height:2.74824in" />

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

refund request, return request, return my product, want refund, want to
return

<img src="./media/image174.png"
style="width:6.26806in;height:2.75176in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Send a Message**. A **Message Node** will be created.
    In the Message node, enter the following text:

We are here to help you. To generate the refund or return request simply
complete the form below.

<img src="./media/image175.png"
style="width:6.26806in;height:2.77467in" />

<img src="./media/image176.png"
style="width:6.26806in;height:2.7594in" />

7.  Below the Message node, click on the **+** sign to create a new
    node. Select **Ask with Adaptive Card**. An Adaptive Card Node will
    be created.

<img src="./media/image177.png"
style="width:6.26806in;height:2.74007in" />

8.  In the Adaptive Card node, select the **three dots** (More Options)
    and then select **Properties**.

<img src="./media/image178.png"
style="width:6.26806in;height:2.78125in" />

9.  In the Adaptive Card properties, below the **Edit JSON** paste the
    provided JSON code to create the adaptive card.

{

"\$schema": "<http://adaptivecards.io/schemas/adaptive-card.json>",

"type": "AdaptiveCard",

"version": "1.4",

"body": \[

{

"type": "TextBlock",

"text": "Purchase Refund and Exchange Form",

"weight": "Bolder",

"size": "Large",

"horizontalAlignment": "Center"

},

{

"type": "Input.Text",

"id": "fullName",

"placeholder": "Enter your full name",

"label": "Full Name",

"isRequired": true,

"errorMessage": "Full Name is required."

},

{

"type": "Input.Text",

"id": "email",

"placeholder": "Enter your email address",

"label": "Email",

"style": "Email",

"isRequired": true,

"errorMessage": "Email is required."

},

{

"type": "Input.Text",

"id": "phoneNumber",

"placeholder": "Enter your phone number",

"label": "Phone Number",

"style": "Tel",

"isRequired": true,

"errorMessage": "Phone Number is required."

},

{

"type": "Input.Text",

"id": "product",

"placeholder": "Enter the product name or description",

"label": "Product",

"isRequired": true,

"errorMessage": "Product is required."

},

{

"type": "Input.ChoiceSet",

"id": "contactMethod",

"label": "Preferred Contact Method",

"style": "expanded",

"choices": \[

{

"title": "Phone",

"value": "Phone"

},

{

"title": "Email",

"value": "Email"

}

\],

"isRequired": true,

"errorMessage": "Preferred Contact Method is required."

},

{

"type": "Input.ChoiceSet",

"id": "orderType",

"label": "Order Type",

"style": "expanded",

"choices": \[

{

"title": "In Store",

"value": "In Store"

},

{

"title": "Online",

"value": "Online"

}

\],

"isRequired": true,

"errorMessage": "Order Type is required."

},

{

"type": "Input.Text",

"id": "receiptNumber",

"placeholder": "Enter the receipt number",

"label": "Receipt Number",

"isRequired": true,

"errorMessage": "Receipt Number is required."

},

{

"type": "Input.Text",

"id": "orderNumber",

"placeholder": "Enter the order number",

"label": "Order Number",

"isRequired": true,

"errorMessage": "Order Number is required."

},

{

"type": "Input.Text",

"placeholder": "Enter the Purchase Date",

"id": "purchaseDate",

"label": "Purchase Date",

"isRequired": true,

"errorMessage": "Purchase Date Required."

},

{

"type": "Input.Text",

"id": "description",

"placeholder": "Provide a brief description of the issue or reason for
return/exchange",

"label": "Description",

"isMultiline": true,

"isRequired": true,

"errorMessage": "Description is required."

}

\],

"actions": \[

{

"type": "Action.Submit",

"title": "Submit",

"data": {

"action": "submitRefundExchange"

}

}

\]

}

<img src="./media/image179.png"
style="width:6.26806in;height:2.75327in" />

10. Select **Variables** to open the Variables pane.

11. Check the boxes on the right-hand side for the all-topic variables.

12. Click on **Save** to save your variable settings.

<img src="./media/image180.png"
style="width:6.26806in;height:2.80347in" />

13. Below the adaptive card node, click on the + **sign** to create a
    new node. Select **Ask a Question, a Question Node** will be
    created.

<img src="./media/image181.png"
style="width:6.26806in;height:2.78052in" />

14. In the Ask Question node message field, enter the message.

Thank you for using our service. You want to know more?

<img src="./media/image182.png"
style="width:6.26806in;height:2.79567in" />

15. In the Question node, select **Multiple Choice** as the identify.

16. In the **Options for user** section, enter the following choices:

    1.  Shop

    2.  Deals and Promotion

    3.  I’m done.

> <img src="./media/image183.png"
> style="width:6.26806in;height:2.78704in" />

17. Below **Save the user's response** a new variable creates (Var1),
    click on the variable name variable properties window will open,
    where you can rename the variable name with **Afterrefund.**

<img src="./media/image184.png"
style="width:6.26806in;height:2.79722in" />

18. Click the **(X)** to close the variable properties window.

19. Under the **Shop and Deals and Promotion** condition, click on the
    **+** sign on each condition and select **Topic Management** for
    each, then choose **Go to Another Topic**. A topic selection window
    will open—search for **Conversation Start** and select the
    **Conversation Start** topic.

<img src="./media/image185.png"
style="width:6.26806in;height:2.81675in" />

20. For **I’m done option,** click on the **+** sign and select **Topic
    Management** for each, then choose **Go to Another Topic** and
    select **End Conversation.**

<img src="./media/image186.png"
style="width:6.26806in;height:2.79869in" />

21. Once all nodes are configured, click on **Save** to finalize and
    save your **"Refund Requests"** topic.

<img src="./media/image187.png"
style="width:6.26806in;height:2.75556in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Successfully created a "Refund or Return Policy Information" topic
    with trigger phrases and generative answers.

2.  Built a "Refund Request" topic that allows users to submit refund
    forms using adaptive cards.

3.  Implemented a decision flow to guide users based on their needs.

4.  Configured system variables and integrated adaptive cards with JSON.

5.  Achieved enhanced customer experience through automated responses
    and topic management in Copilot Studio.

# Exercise 7: Create Power Automate Flow and Action for Refund Requests

In this exercise, participants will create a Power Automate flow
designed to handle refund requests, enhancing efficiency in processing
customer inquiries. The first task involves setting up a flow that
collects essential information such as the customer's name, email, phone
number, purchase date, and order details. By utilizing the Dataverse
connector, the collected data will be stored in a designated Refund
Requests table, ensuring organized management of refund inquiries.
Following this, participants will integrate the newly created flow into
the Copilot Studio by defining specific actions that streamline the
interaction with customers. This exercise not only reinforces practical
skills in Power Automate but also demonstrates how to leverage Copilot
functionalities to enhance user experience and operational efficiency.

## Task 1: Create Power Automate Flow to Refund Request Flow

1.  Select the **Actions** tab to start configuring actions for your
    Copilot.

<img src="./media/image188.png"
style="width:6.26806in;height:2.81467in" />

2.  Click on **+ Add an action**.

<img src="./media/image189.png"
style="width:6.26806in;height:2.78938in" />

3.  Scroll down and select **Create a new flow** a new Power Automate
    flow window will pop up. Check the environment from top right
    corner, if correct environment (Dev One) not selected, please select
    the correct environment.

<img src="./media/image190.png"
style="width:4.94608in;height:2.90139in" />

4.  Select **Run a flow from copilot** from top left corner and rename
    the flow as **Refund Request Flow**.

<img src="./media/image191.png"
style="width:6.26806in;height:2.77427in" />

5.  In the trigger step "**Run a flow from Copilot,"** select **+ Add an
    input**.

<img src="./media/image192.png"
style="width:6.26806in;height:2.61279in" />

6.  Select **Text** for the input type and configure the following
    inputs by repeating the process:

    1.  Enter **Name** in Input for Full Name

    2.  Enter **Email** in Input for Email

    3.  Enter **Phone Number** in Input for Phone Number

    4.  Enter **Purchase Date** in Input for Date of Purchase

    5.  Enter **Description** in Input for Description

    6.  Enter **Order Number** in Input for Order Number

    7.  Enter **Order Type** in Input for Order Type

    8.  Enter **Product** in Input for Product

    9.  Enter **Receipt Number** in Input for Appointment Type

    10. Enter **Contact Method** in Input for Preferred Contact Method

> <img src="./media/image193.png"
> style="width:6.26806in;height:2.60866in" />
>
> <img src="./media/image194.png"
> style="width:6.26806in;height:2.73819in" />
>
> <img src="./media/image195.png"
> style="width:6.26806in;height:2.59314in" />

7.  Click on the **+ icon** between the two steps in the flow and select
    **Add an action**.

<img src="./media/image196.png"
style="width:6.26806in;height:2.78525in" />

8.  In the **Search** field, type **Dataverse** and select **See more**
    for the Dataverse connector.

<img src="./media/image197.png"
style="width:6.26806in;height:2.63264in" />

9.  Select **Add a new row** action.

<img src="./media/image198.png"
style="width:6.26806in;height:2.60715in" />

10. Choose **Refund Requests** for the table name.

<img src="./media/image199.png"
style="width:6.26806in;height:2.61201in" />

11. Select **Show all** to see all available fields.

<img src="./media/image200.png"
style="width:6.26806in;height:2.59183in" />

12. Use **Dynamic content** to map each input parameter to the
    corresponding field:

    1.  **Name** Dynamic Input → **Full Name** Parameter.

    2.  **Purchase Date** Dynamic Input → **Date of Purchase**
        Parameter.

    3.  **Description** Dynamic Input → **Description** Parameter.

    4.  **Email** Dynamic Input → **Email** Parameter.

    5.  **Order Number** Dynamic Input → **Order Number** Parameter.

    6.  **Order Type** Dynamic Input → **Order Type** Parameter.

    7.  **Phone Number** Dynamic Input → **Phone Number** Parameter.

    8.  **Product** Dynamic Input → **Product** Parameter.

    9.  **Receipt Number** Dynamic Input → **Receipt Number** Parameter.

    10. **Contact Method** Dynamic Input → **Preferred Contact Method**
        Parameter.

> <img src="./media/image201.png"
> style="width:6.26806in;height:2.58701in" />
>
> <img src="./media/image202.png"
> style="width:6.26806in;height:2.67757in" />

13. Select **Respond to Copilot** action.

14. Click on **Settings**.

15. Ensure that **Asynchronous Response** is set to **Off**.

> <img src="./media/image203.png"
> style="width:6.26806in;height:2.77361in" />

16. Select **Save draft**. Then, click on **Publish**.

> <img src="./media/image204.png"
> style="width:6.26806in;height:2.78182in" />

17. Once the flow is published, close the Power Automate tab to return
    to Copilot Studio.

## Task 2: Create Action in Copilot for Refund Requests

1.  Go to copilot window and click on **Refresh**, (If the Copilot
    window was closed, reopen it and navigate back to the **Copilot
    Studio.** Go to the **Actions** tab and click on **+ Add an
    action**.)

<img src="./media/image136.png"
style="width:4.93627in;height:2.97639in" />

2.  In the "Choose an action" window, select the **Refund Requests
    Flow** you created.

<img src="./media/image205.png"
style="width:5.0098in;height:2.97847in" />

3.  Click on **Next**, **next** then **Next** again, and finally
    **Finish**. The flow will now be added as an action.

<img src="./media/image206.png"
style="width:4.94118in;height:2.93125in" />

<img src="./media/image207.png"
style="width:4.92157in;height:2.92431in" />

<img src="./media/image208.png"
style="width:4.97549in;height:2.88264in" />

4.  Navigate to the **Topics** section. Select the **Refund Request**
    topic.

<img src="./media/image209.png"
style="width:6.26806in;height:2.76924in" />

5.  Below the Adaptive Card node, click on the **+** sign to create a
    new node select **Call an action**. Choose the **Refund Requests
    Flow**. This action will now be added below the Adaptive Card node.

<img src="./media/image210.png"
style="width:6.26806in;height:2.85122in" />

6.  In the action node, you need to map each input field to the
    appropriate variable created by the Adaptive Card:

    1.  **Name** Input: Click on the input field, then select
        **fullname** from the custom variables.

    2.  **Email** Input: Click on the input field, then select **email**
        from the custom variables.

    3.  **Phone Number** Input: Click on the input field, then select
        **phoneNumber** from the custom variables.

    4.  **Product** Input: Click on the input field, then select
        **product** from the custom variables.

    5.  **Contact Method** Input: Click on the input field, then select
        **contactMethod** from the custom variables.

    6.  **Order Type** Input: Click on the input field, then select
        **orderType** from the custom variables.

    7.  **Receipt Number** Input: Click on the input field, then select
        **receiptNumber** from the custom variables.

    8.  **Order Number** Input: Click on the input field, then select
        **orderNumber** from the custom variables.

    9.  **Purchase Date** Input: Click on the input field, then select
        **purchaseDate** from the custom variables.

    10. **Description** Input: Click on the input field, then select
        **description** from the custom variables.

> <img src="./media/image211.png"
> style="width:6.26806in;height:2.75842in" />
>
> <img src="./media/image212.png"
> style="width:6.26806in;height:2.81042in" />

7.  After mapping all the variables, click on the **Save** button to
    save the topic configuration.

<img src="./media/image213.png"
style="width:6.26806in;height:2.80842in" />

## Task 3: Publish Your Copilot

1.  From the top right corner, Click on the **Publish** button to start
    the publishing process.

<img src="./media/image214.png"
style="width:6.26806in;height:2.12639in" />

2.  A confirmation dialog may appear. Select **Publish** again to
    finalize and publish your copilot.

<img src="./media/image215.png"
style="width:6.26806in;height:1.85903in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Successfully created a Power Automate flow for refund requests.

2.  Configured input parameters for customer details.

3.  Mapped inputs to corresponding fields in the Dataverse Refund
    Requests table.

4.  Integrated the flow into Copilot Studio by creating actions for
    refund requests.

5.  Published the Copilot for user accessibility.

# Final Test

Exercise 6: Test Your Copilot

To test the functionalities of your Copilot and Power Automate flows,
follow these steps:

Click on the three-dot right side of the window and select **Go to demo
website.** A demo website window will open start the conversation into
the website chat window.

**Note:** Testing Copilot with the same prompt multiple times may yield
varying responses due to contextual learning, dynamic data access, and
inherent randomness in its output generation.

<img src="./media/image216.png"
style="width:6.26667in;height:2.725in" />

<img src="./media/image217.png"
style="width:6.26667in;height:2.95833in" />

1.  What are some deals on student laptops right now?

<img src="./media/image85.png" style="width:6.26667in;height:2.8in" />

<img src="./media/image218.png"
style="width:6.26667in;height:2.96667in" />

2.  Tell me more about Surface Laptop Go 3. What are the specs & cost?

<img src="./media/image87.png"
style="width:6.26667in;height:2.96667in" />

<img src="./media/image219.png" style="width:6.26667in;height:2.95in" />

3.  Compare laptop surface laptop pro 3 and surface laptop studio 2.

<img src="./media/image89.png" style="width:6.26667in;height:2.975in" />

<img src="./media/image220.png" style="width:6.26667in;height:2.95in" />

4.  Book Appointment for further assistance

<img src="./media/image221.png"
style="width:6.26667in;height:2.975in" />

<img src="./media/image150.png"
style="width:6.26667in;height:2.96667in" />

5.  Ensure that the details entered in the Appointment Booking are
    accurately reflected in the "Book Appointments" table in Power Apps.

<img src="./media/image151.png"
style="width:6.26667in;height:2.78333in" />

6.  I want to know about the Contoso refund policy.

<img src="./media/image222.png" style="width:6.26667in;height:2.95in" />

<img src="./media/image223.png"
style="width:6.26667in;height:2.95833in" />

7.  I bought a laptop 10 days ago. Am I eligible to return it?

<img src="./media/image224.png"
style="width:6.26667in;height:2.93333in" />

<img src="./media/image225.png"
style="width:6.26667in;height:2.96667in" />

8.  I buy laptop 3 day ago; I have to submit refund request.

<img src="./media/image226.png"
style="width:6.26667in;height:2.94167in" />

<img src="./media/image227.png"
style="width:6.26667in;height:2.825in" />

9.  Ensure that the details entered in the Appointment Booking are
    accurately reflected in the "Refund Requests" table in Power Apps.

<img src="./media/image228.png"
style="width:6.26667in;height:2.76667in" />
