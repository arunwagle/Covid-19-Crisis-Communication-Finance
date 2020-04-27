# Setup

1. [Create a free IBM Cloud Account](#create-free-ibm-account)
2. [Setup IBM Services](#setup-ibm-services)
3. [Deploy Web Application](#deploy-web-application)
4. [Deploy Voice + SMS Virtual Assistant](#deploy-voice-sms-va)
5. [Deploy SMS Virtual Assistant](#deploy-sms-va)
6. [Deploy Slack Virtual Assistant](#deploy-slack-va)

## Create a free IBM Cloud Account

[Create New IBM Cloud Account](https://cloud.ibm.com/registration)

## Setup IBM Services

### Watson Assistant

1. [Create and Launch Watson Asssitant Service](https://cloud.ibm.com/docs/assistant?topic=assistant-getting-started#getting-started-prerequisites)

2. Create Web+Slack dialog skill by importing the [skill-Covid-19-Financial-Virtual-Assistant---Web%2BSlack.json](/watson-assets/WatsonAssistant/skill-Covid-19-Financial-Virtual-Assistant---Web%2BSlack.json)
Note: Refer to [How to import dialog skill](https://cloud.ibm.com/docs/assistant?topic=assistant-skill-dialog-add)

3. Create Voice+SMS dialog skill by importing the [skill-Covid-19-Financial-Virtual-Assistant---Voice-%2B-SMS.json](/watson-assets/WatsonAssistant/skill-Covid-19-Financial-Virtual-Assistant---Voice-%2B-SMS.json)

4. Create SMS dialog skill by importing the [skill-Covid-19-Financial-Virtual-Assistant---SMS.json](/watson-assets/WatsonAssistant/skill-Covid-19-Financial-Virtual-Assistant---SMS.json)

5. Once all the skills are created, you can use "Try it Out" pane to test your skill.
Note: Refer to [Try it out](https://cloud.ibm.com/docs/assistant?topic=assistant-tutorial#tutorial-test-menu-options-intent)

### Watson Discovery

1. [Create and Launch Watson Discovery Service](https://cloud.ibm.com/docs/discovery?topic=discovery-getting-started)

2. Create COVID-19 Kit
   1. Watson Discovery released **COVID-19 Kit** which has an FAQ extractor that is pre configured to extract data from the following sources. This can be extended to add more sources later.
   
   https://faq.coronavirus.gov/
   https://www.who.int/news-room/q-a-detail/q-a-coronaviruses
   https://www.health.harvard.edu/diseases-and-conditions/treatments-for-covid-19
   https://www.health.harvard.edu/diseases-and-conditions/if-you-are-at-higher-risk
   https://www.health.harvard.edu/diseases-and-conditions/if-youve-been-exposed-to-the-coronavirus
   https://www.health.harvard.edu/diseases-and-conditions/coronavirus-outbreak-and-kids
   https://www.health.harvard.edu/diseases-and-conditions/coronavirus-resource-center
   https://www.dol.gov/agencies/whd/flsa/pandemic
   https://www.dol.gov/agencies/whd/fmla/pandemic
   https://www.dol.gov/coronavirus/unemployment-insurance
    
   
   2. Create a collection by selecting COVID-19 Kit. 
   3. Customize to add the IRS source. This has information on the relief act passed by the goverment
   https://www.irs.gov/newsroom/economic-impact-payments-what-you-need-to-know
   
3. Choose a **Sync frequency** to "once a day"

4. Create Search Skill "Covid-19 FAQ Search Skill" in Watson Assistant. Select Title = "extracted_metadata.title", Body = "text" and URL = "metadata.source.url"
   Note [Refer to](https://cloud.ibm.com/docs/assistant?topic=assistant-skill-search-add)
   
### Speech to Text
[Create Speech To Text Service](https://cloud.ibm.com/docs/services/speech-to-text?topic=speech-to-text-gettingStarted#getting-started-tutorial)

### Text to Speech
[Create Text To Speech Service](https://cloud.ibm.com/docs/services/text-to-speech?topic=text-to-speech-gettingStarted#getting-started-tutorial)

### Voice Agent with Watson


## Deploy Web Application

When opening a new issue in the `Code-and-Response/Project-Sample` issue tracker, please provide as much
detail about your environment as possible.

See [How to create a Minimal, Complete, and Verifiable example](https://stackoverflow.com/help/mcve).

## Deploy Voice + SMS Virtual Assistant

Once an issue has been opened, it is not uncommon for there to be discussion
around it. Some contributors may have differing opinions about the issue,
including whether the behavior being seen is a bug or a feature. This discussion
is part of the process and should be kept focused, helpful, and professional.

Short, clipped responses—that provide neither additional context nor supporting
detail—are not helpful or professional. To many, such responses are simply
annoying and unfriendly.

Contributors are encouraged to help one another make forward progress as much
as possible, empowering one another to solve issues collaboratively. If you
choose to comment on an issue that you feel either is not a problem that needs
to be fixed, or if you encounter information in an issue that you feel is
incorrect, explain *why* you feel that way with additional supporting context,
and be willing to be convinced that you may be wrong. By doing so, we can often
reach the correct outcome much faster.

## Deploy SMS Virtual Assistant

In the vast majority of cases, issues are resolved by opening a Pull Request.
The process for opening and reviewing a Pull Request isa similar to that of
opening and triaging issues, but carries with it a necessary review and approval
workflow that ensures that the proposed changes meet the minimal quality and
functional guidelines.

## Deploy Slack Virtual Assistant
