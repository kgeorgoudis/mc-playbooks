# ansible-automation

### Description
Recently I wrote the tasks of this playbook in order to automate a workflow 
between 2 systems. System A is an ansible control node and System B is 
Marketing Cloud

In my real scenario, several tasks in this playbook are processing files 
and then the playbook triggers the marketing cloud automation in order to start

I'm no marketing cloud expert, but thanks to the urls bellow 
I have managed to successfully trigger the automation :thumbsup:

### Improve ObjectID task

The ObjectID is necessary for the trigger task

~~I tried to get the ObjectID from the XML SOAP response using 
the [community.general.xml](https://docs.ansible.com/ansible/latest/collections/community/general/xml_module.html) 
xpath but no luck :pensive: So I used regex_search ansible filter~~

Update: commit 08f420ab44243f4563ed1b950fedf0a7528d8c36 changed the way to get ObjectID using the 
[community.general.xml](https://docs.ansible.com/ansible/latest/collections/community/general/xml_module.html) module

### Reference urls:

- [Interact with Automation Studio](https://developer.salesforce.com/docs/atlas.en-us.noversion.mc-apis.meta/mc-apis/interacting_with_automation_studio_via_the_web_service_soap_api.htm)
- [Postman Salesforce Developers](https://www.postman.com/salesforce-developers/workspace/salesforce-developers/collection/14448118-2835a976-010c-4548-92f8-f42c0382758e?ctx=documentation)
